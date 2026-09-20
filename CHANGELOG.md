# Changelog

本项目的所有值得注意的变更都会记录在此文件中。

格式基于 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.1.0/)，版本号遵循 [Semantic Versioning](https://semver.org/lang/zh-CN/)。

## [2.1.0] - 2026-09-20

### 新增

- **供应链安全审计**：新增 `references/methodology/06-supply-chain-audit.md`，蒸馏自 `skill-security-audit` 技能——安装/启用第三方 skill / MCP / 脚本前的五维审计（静态危险模式、权限边界、网络行为、商业化附加层检测、风险分级），含 PUA 实战范式与报告模板。
- `SKILL.md` 新增供应链审计触发词与路由入口；`README` 同步更新。

## [2.0.0] - 2026-09-20

基于 [MyuriKanao/src-hunter-skill](https://github.com/MyuriKanao/src-hunter-skill)（MIT）的**蒸馏版**首发。

### 新增

- **cc-switch 多 provider 支持**：读 `ANTHROPIC_BASE_URL` / `ANTHROPIC_MODEL` 判定上下文预算档位（A ≥200K / B ≤128K / C ≤64K），自动调节加载策略。
- `cc-switch/providers.md`：Anthropic / DeepSeek / Kimi / GLM / Qwen / Gemini 端点与模型对照表、分阶段省钱推荐。
- `cc-switch/README.md`：快速上手 + 三档行为差异 + 常见坑。
- `references/h1-reports/`：2887 份 HackerOne 原始报告蒸馏为 **2743 张 case card**（标题·程序·严重度·CVE·一句话根因·链接），按 weakness 分组可检索。

### 变更

- 仓库体积 66 MB / 3175 文件 → **~4 MB / ~283 文件**（约 17×）。
- `SKILL.md` 重写：保留 5 阶段强制 checkpoint 方法论，新增「运行环境自适应（cc-switch / 上下文预算）」章节。
- `README.md` / `README.en.md` 双语重写，标注蒸馏差异与 cc-switch 接入方式。

### 移除

- `references/h1-reports/raw/`（39 MB 原始 JSON 报告，冗余于 case card）。
- `references/payloader/raw/`（1.7 MB 机器源 JSON，已渲染进 `by-category/*.md`）。

### 保留

- 全部 19 类攻击 playbook、结构化 payload 库、WAF/EDR 绕过变体、国产组件指纹与默认凭据、银行/电信行业 playbook、CVSS 4.0 报告模板、jshookmcp 工具索引——**未删减**。

## [1.2.1] - 上游版本

上游 [MyuriKanao/src-hunter-skill](https://github.com/MyuriKanao/src-hunter-skill) 1.2.1 及其之前的版本历史见上游仓库；本仓库从 2.0.0 起独立演进。
