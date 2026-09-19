# cc-switch 多 Provider 参考表

`src-hunter` skill 是 **provider 无关** 的——通过 cc-switch 切到任意 Anthropic 兼容端点都能跑。下表给出常见 provider 的 `ANTHROPIC_BASE_URL` 与模型名，用于在 cc-switch 里新增/校验 provider 配置。

> [!NOTE]
> 端点与模型名可能随 provider 调整。优先以 **cc-switch 内置预设** 和你当前 provider 的官方文档为准；下表用于快速对照。

## Provider → 端点 / 模型

| Provider | `ANTHROPIC_BASE_URL` | 主模型（`ANTHROPIC_MODEL`） | 小快模型（`ANTHROPIC_SMALL_FAST_MODEL`） | 上下文档位 |
|---|---|---|---|---|
| Anthropic 官方 | `https://api.anthropic.com`（默认，不填） | `claude-opus-5` / `claude-sonnet-5` | `claude-haiku-4-5` | A（≥200K） |
| DeepSeek | `https://api.deepseek.com/anthropic` | `deepseek-chat`（V3）/ `deepseek-reasoner`（R1） | `deepseek-chat` | C（≤64K） |
| Moonshot Kimi | `https://api.moonshot.cn/anthropic` | `kimi-k2-0905-preview` / `kimi-k2-turbo-preview` | `kimi-k2-turbo-preview` | B（≤128K） |
| 智谱 GLM | `https://open.bigmodel.cn/api/anthropic` | `glm-4.6` / `glm-4.5` | `glm-4.5-air` | B（≤128K） |
| 阿里 Qwen | `https://dashscope.aliyuncs.com/api/v2/apps/claude-code-proxy` | `qwen3-coder-plus` / `qwen3-max` | `qwen-plus` | B（≤128K） |
| Google Gemini | 走中转/兼容网关（见 cc-switch 预设） | `gemini-2.5-pro` | `gemini-2.0-flash` | B |

## 环境变量说明

cc-switch 切换 provider 时本质是改写 Claude Code 的这几个变量（写入 `~/.claude/settings.json` 的 `env` 块，或进程环境）：

| 变量 | 作用 |
|---|---|
| `ANTHROPIC_BASE_URL` | Anthropic 兼容 API 端点；官方可不设 |
| `ANTHROPIC_AUTH_TOKEN` | 该 provider 的 API Key |
| `ANTHROPIC_MODEL` | 主模型名（skill 的档位判定看它） |
| `ANTHROPIC_SMALL_FAST_MODEL` | haiku 级小模型，用于廉价快任务 |

`src-hunter` 只读取 `ANTHROPIC_BASE_URL` / `ANTHROPIC_MODEL` 做**上下文档位判定**，不依赖其余变量，也不会替你在不同 provider 间做任何网络请求。

## 分阶段推荐（省钱 + 提效）

| 阶段 | 推荐 provider | 原因 |
|---|---|---|
| recon / enum（重复劳动） | DeepSeek / Qwen 小模型 | 便宜；按清单机械化执行，不需要强推理 |
| hunt（关键判断） | Claude / GLM / Kimi 大模型 | 需要长链路推理 + payload 精确性 |
| report（格式产出） | 中档即可 | 模板驱动，忠于证据即可 |

## 切模型后的自检

切到新 model 后先做一次 10s 自检，再开始 target：

1. `env | grep ANTHROPIC` 确认 `BASE_URL` / `MODEL` 已生效；
2. 让模型回答一个既定事实（如"列出 Phase 1 四项 checkpoint"）确认指令遵循能力；
3. 按 `SKILL.md`「运行环境自适应」确定档位，调整加载策略后再进入 Phase 1。