# Resource Injection

_4 reports — High/Critical, disclosed_

- **[Xenoblade Chronicles X: Definitive Edition] Unrestricted RPCs allow DoS and writing arbitrary flags remotely** — `Nintendo` · `Critical` [↗](https://hackerone.com/reports/3062122)
  - As part of its peer-to-peer protocol, the game allows peers in a mission to send RPC (remote procedure call) commands to each other.
- **Content injection in Jira issue title enabling sending arbitrary POST request as victim** — `GitLab` · `High` [↗](https://hackerone.com/reports/1533976)
  - `CVE-2022-1940` The issue described here leads to the same outcome as my previous report, https://hackerone.com/reports/1409788 .
- **Arbitrary POST request as victim user from HTML injection in Jupyter notebooks** — `GitLab` · `High` [↗](https://hackerone.com/reports/1409788)
  - An attacker can create a Jupyter notebook that will make arbitrary POST requests as the victim user.
- **Zero-amount miner TX + RingCT allows monero wallet to receive arbitrary amount of monero** — `Monero` · `Critical` [↗](https://hackerone.com/reports/501585)
  - By mining a specially crafted block, that still passes daemon verification an attacker can create a miner transaction that appears to the wallet to include sum of XMR picked by the attacker.
