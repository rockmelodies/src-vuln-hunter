# Authentication Bypass by Primary Weakness

_2 reports — High/Critical, disclosed_

- **Missing server identity policy enforcement in SSH connection reuse allows host key verification bypass via pool poisoning** — `curl` · `High` [↗](https://hackerone.com/reports/3640932)
  - `CVE-2022-27782` ssh_config_matches() in lib/url.c decides whether an existing SSH connection can be reused by a new transfer handle.
- **Incorrect Parsing of IPv6 Zone ID in curl** — `curl` · `High` [↗](https://hackerone.com/reports/3319767)
  - I'm Zehui Miao from NISL@THU.
