[中文](README.md) · **English**

# src-hunter · Distilled

A Claude Code skill for SRC, crowdsourced testing, and bug bounty. Give it a target and it drives the hunt through a fixed workflow:

```text
intake → recon → enum → hunt → report
```

Every phase has a mandatory checkpoint — you don't advance until it passes. Payloads / playbooks / cases are read on demand, never generated from memory.

> This is a **distilled fork** of [MyuriKanao/src-hunter-skill](https://github.com/MyuriKanao/src-hunter-skill): all attack methodology and payloads are kept, while the 48 MB of raw HackerOne report JSON is compressed into a 1.2 MB searchable case-card index, and **cc-switch** multi-provider switching is supported natively. Original author is MIT-licensed and credited here.

## What changed vs. upstream

| Dimension | Upstream v1.2.1 | This v2.0.0 |
|---|---|---|
| Repo size | 66 MB / 3175 files | ~4 MB / ~280 files |
| H1 case library | 2887 raw JSON + 141 full-text files (48 MB) | 2743 distilled case cards (1.2 MB): title · program · severity · CVE · one-line root cause · link |
| cc-switch | none | auto-adapts loading by A/B/C context-budget tiers |
| Methodology / payloads | full | full, untouched |

Distillation principle: **keep the brain (playbooks / payloads / methodology / fingerprints), cut the fat (raw JSON and verbatim report prose)**. No more context blow-ups on 64K/128K models, without losing hit rate.

## Install

Marketplace:

```bash
/plugin marketplace add rockmelodies/src-vuln-hunter
/plugin install src-hunter@src-hunter
```

Git:

```bash
git clone https://github.com/rockmelodies/src-vuln-hunter.git ~/.claude/skills/src-hunter
```

## cc-switch multi-provider

Works natively with [cc-switch](https://github.com/farion1231/cc-switch). Switch to DeepSeek / GLM / Qwen / Kimi and other Anthropic-compatible endpoints — the skill reads `ANTHROPIC_BASE_URL` + `ANTHROPIC_MODEL` to auto-detect its tier (A ≥200K / B ≤128K / C ≤64K) and adjusts loading accordingly.

- Quick start: [`cc-switch/README.md`](cc-switch/README.md)
- Endpoint/model reference: [`cc-switch/providers.md`](cc-switch/providers.md)

## Layout

```text
SKILL.md                 five-phase workflow (with tier adaptation)
cc-switch/               cc-switch provider config guide
references/
  methodology/    phases, attack priority, bypass toolkit, evidence rules, supply-chain audit
  playbooks/      19 attack playbooks, each with real H1 cases + payloads
  industry/       banking/finance, telecom/ISP vertical playbooks
  dictionaries/   Chinese vendor fingerprints & default credentials
  payloader/      structured payloads, WAF/EDR bypass, tool commands
  h1-reports/     2743 distilled H1 case cards grouped by weakness
  templates/      CVSS 4.0 report template
  tools/          jshookmcp tool index
```

Playbooks are the main entry point, all written from a black-box perspective (you only have a URL, no source).

## Trigger keywords

- bug bounty, HackerOne, SRC hunting, crowdsourced testing
- WAF bypass
- how to test an endpoint / API / parameter
- take over any account / modify any / reset password
- default credentials, Actuator, exposed admin panel

Explicit invocation:

```text
/src-hunter <target>
```

## Red lines

Every playbook ends with concrete boundaries. The most common:

- **Sample control**: prove DB name/version, don't dump; IDOR / Mongo / ES grab 1–3 records.
- **Self-testing accounts**: authz, password reset, JWT, redirect_uri, blind XSS — always test with your own two accounts.
- **Read-only**: RCE only runs `id`/`whoami`; Redis/Mongo unauth only `info`/`ping`; arbitrary read stops at one `root:x:` line.
- **No real side effects**: never really send SMS, charge, refund, or overwrite files.
- **DoS/concurrency**: single repro ≤60s, 5 serial attempts; races 50–100, never 1000+.
- **Leave nothing behind**: webshells/heapdumps/dumped source stay local and get deleted after reporting.
- **Leaked creds are not used**: only verify, never operate.
- **Anonymize PII**: keep first 2 + last 2 chars.
- **OOB**: self-host interactsh, never public DNSLog platforms.
- **No packet, no finding**: every claim backed by HTTP packet / screenshot / video.

## Attribution & license

- Data compiled from public sources: HackerOne hacktivity disclosed High/Critical reports, WooYun archival statistics, `3516634930/Payloader`.
- Distilled from [MyuriKanao/src-hunter-skill](https://github.com/MyuriKanao/src-hunter-skill) (MIT), original license and attribution retained.

MIT, see [LICENSE](LICENSE).
