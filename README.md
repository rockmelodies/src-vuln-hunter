**中文** · [English](README.en.md)

# src-hunter · 蒸馏版

给 SRC、众测、Bug bounty 用的 Claude Code skill。你给它一个目标，它按固定流程推进漏洞挖掘：

```text
intake → recon → enum → hunt → report
```

每阶段有强制 checkpoint，未通过不进下一阶段；payload / playbook / 案例全部按需 Read，不准凭记忆生成。

> 本仓库是 [MyuriKanao/src-hunter-skill](https://github.com/MyuriKanao/src-hunter-skill) 的**蒸馏版**：保留全部攻击方法论与 payload，把 48 MB 的 HackerOne 原始 JSON 报告库压缩成 1.2 MB 的可检索 case card，并原生适配 **cc-switch** 多 provider 切换。原作者 MIT 授权，此处保留署名。

## 相比原版做了什么

| 维度 | 原版 v1.2.1 | 本版 v2.0.0 |
|---|---|---|
| 仓库体积 | 66 MB / 3175 文件 | ~4 MB / ~280 文件 |
| H1 案例库 | 2887 份原始 JSON + 141 份全文（48 MB） | 2743 份蒸馏为 case card（1.2 MB）：标题·程序·严重度·CVE·一句话根因·链接 |
| cc-switch | 无 | 按上下文预算 A/B/C 三档自动调节加载 |
| 方法论 / payload | 完整 | 完整保留，未删减 |

蒸馏原则：**保留"大脑"（playbook / payload / 方法论 / 指纹库），砍掉"脂肪"（原始 JSON 与报告全文复述）**。对 64K/128K 上下文模型不再爆 context，命中率不降反升。

## 安装

Marketplace：

```bash
/plugin marketplace add rockmelodies/src-vuln-hunter
/plugin install src-hunter@src-hunter
```

Git：

```bash
git clone https://github.com/rockmelodies/src-vuln-hunter.git ~/.claude/skills/src-hunter
```

## cc-switch 多 provider

原生适配 [cc-switch](https://github.com/farion1231/cc-switch)。切到 DeepSeek / GLM / Qwen / Kimi 等 Anthropic 兼容端点也能跑，skill 读 `ANTHROPIC_BASE_URL` + `ANTHROPIC_MODEL` 自动判定档位（A ≥200K / B ≤128K / C ≤64K）并调节加载策略。

- 快速上手：[`cc-switch/README.md`](cc-switch/README.md)
- 端点 / 模型对照表：[`cc-switch/providers.md`](cc-switch/providers.md)

## 目录结构

```text
SKILL.md                 五阶段工作流控制（含档位自适应）
cc-switch/               cc-switch provider 配置说明
references/
  methodology/    五阶段流程、攻击优先级、绕过工具集、证据规则
  playbooks/      19 类攻击 playbook，每类含真实 H1 案例与 payload
  industry/       银行/金融、电信/ISP 垂直场景 playbook
  dictionaries/   国产组件指纹与默认凭据
  payloader/      结构化 payload、WAF/EDR 绕过、工具命令
  h1-reports/     2743 份 H1 案例蒸馏索引（按 weakness 分组 case card）
  templates/      CVSS 4.0 报告模板
  tools/          jshookmcp 工具索引
```

playbook 是主要入口，全部按黑盒视角编写（默认你只有 URL，没有源码）。

## 触发关键词

- bug bounty、HackerOne、SRC 挖洞、漏洞赏金、众测
- WAF bypass、绕过 WAF
- 如何测试某个 endpoint / API / 参数
- 任意账号、任意修改、任意删除、密码重置
- 默认凭据、Actuator、暴露的管理后台

显式调用：

```text
/src-hunter <target>
```

## Playbook 列表

| Playbook | H1 案例数 |
|---|---:|
| arbitrary-x-authz（IDOR / 任意账户 / 提权） | 465 |
| rce（反序列化 / SSTI / XXE / 框架） | 385 |
| xss | 335 |
| info-disclosure | 319 |
| oauth-saml-jwt | 240 |
| logic-flaws（CSRF / 点击劫持 / 支付） | 234 |
| path-traversal / LFI / RFI | 163 |
| sqli | 147 |
| dos | 138 |
| ssrf-cache-host | 108 |
| unauth-access | 46 |
| http-smuggling / CRLF | 38 |
| api-rest / WebSocket | 15 |
| file-upload | 8 |
| mobile | 8 |
| race-conditions | 5 |
| llm-prompt-injection | 1 |
| graphql | 1 |
| intranet-postexp（内网 / 后渗透速查） | — |

## 红线

每个 playbook 末尾写有具体边界。最常踩的点：

- **样本控制**：SQLi 证明到库名/版本即停；IDOR、Mongo/ES 拉 1–3 条样本就够。
- **测试账号自演**：越权、密码重置、JWT、redirect_uri、XSS 盲打全用自己两个号互测，不碰陌生人账号。
- **只读不写**：RCE 只跑 `id`/`whoami`；Redis/Mongo 未授权只 `info`/`ping`；任意读看到 `root:x:` 一行即停。
- **不真做副作用**：不真发短信、不真扣款、不真退款、不覆盖文件。
- **DoS/并发**：单次 ≤60s，串行 5 次足够；竞态 50–100，绝不 1000+。
- **不留物**：webshell/heapdump/dump 源码本地保存，报告后立即删除。
- **凭据拿到不用**：泄露的 AWS/Stripe/DB 凭据只验证，不用于任何真实操作。
- **报告脱敏**：手机号/邮箱/token 留前 2 + 后 2。
- **OOB 验证**：不用公共 DNSLog 平台，自架 interactsh 或用厂商 SSRF 测试平台。
- **没抓包就没发现**：所有断言都要有 HTTP 包/截图/视频。

## 数据来源与授权

- 数据整理自公开资料：HackerOne hacktivity 已披露 High/Critical 报告、WooYun 历史统计残余、`3516634930/Payloader`。
- 本项目只整理、翻译、重组公开资料，不包含专有数据，不抓取需认证内容。
- 基于 [MyuriKanao/src-hunter-skill](https://github.com/MyuriKanao/src-hunter-skill)（MIT）蒸馏改造，保留原 MIT 授权与署名。

## License

MIT，见 [LICENSE](LICENSE)。
