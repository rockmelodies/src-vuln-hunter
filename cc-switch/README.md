# cc-switch 支持说明

`src-hunter` 原生适配 [cc-switch](https://github.com/farion1231/cc-switch)（Claude Code 多 provider 配置切换器）。你可以在不同 provider / 模型之间来回切，skill 会自动按**上下文档位**调节加载策略，不会因为切到 64K/128K 的小上下文模型而爆 context。

## 一句话原理

cc-switch 切换时改写 `ANTHROPIC_BASE_URL` / `ANTHROPIC_AUTH_TOKEN` / `ANTHROPIC_MODEL` 等环境变量；`src-hunter` 读 `ANTHROPIC_BASE_URL` + `ANTHROPIC_MODEL` 判断当前是哪个档位，从而决定「一次读多大文件、走 00-index 路由还是整读 playbook」。**skill 本身不含任何 provider 密钥，也不做跨 provider 请求。**

## 快速开始

1. **装 skill**（Marketplace 或 git clone，见根 `README.md`）。
2. **配 cc-switch**：在 cc-switch 里新增/选择一个 Anthropic 兼容 provider，`Base URL` 与模型名参考 [`cc-switch/providers.md`](providers.md)。
3. **开始前确认档位**：对模型说一句，或让它 `env | grep ANTHROPIC`，确认取到的是哪个 provider / model。
4. **开挖**：正常触发 `src-hunter`。档位 >200K 走全量加载；≤64K 自动最小加载。

## 三个档位的行为差异

| 档位 | 判定 | 加载策略 | 适合 |
|---|---|---|---|
| **A** | Claude 官方 / 其他 ≥200K | 整读单文件 playbook | 重推理 hunt |
| **B** | GLM / Qwen / Kimi / Gemini | 00-index 路由 + 目标子文件，单 Read ≤30KB | 均衡 |
| **C** | DeepSeek ≤64K | 严格最小加载，单 Read ≤15KB | 廉价批量 recon |

## 常见坑

- **切了模型没生效**：cc-switch 写入的 `~/.claude/settings.json` 只在新会话生效；当前会话变量未变。重开会话再验证 `env | grep ANTHROPIC`。
- **小模型读大文件断了思路**：payload 库按 category 拆好，别整读 100KB+ 的 `waf-bypass.md`，用 `grep`/`sed -n` 定位命中段再读。
- **弱模型指令漂移**：B/C 档下把 Phase 强制 checkpoint 当作硬规则反复确认，必要时降级为"单步一确认"。
- **端点到不了 / 401**：先确认是 provider 端点挂还是 API Key 错，与 skill 无关。