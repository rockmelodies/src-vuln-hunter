# Missing Encryption of Sensitive Data

_3 reports — High/Critical, disclosed_

- **Waketime Payment Gateway Vulnerability** — `WakaTime` · `High` [↗](https://hackerone.com/reports/2097517)
  - Summary: Waketime's payment gateway does not encrypt data in transit, which could allow an attacker to intercept and capture card information.
- **ChaCha20-Poly1305 with long nonces** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/506040)
  - `CVE-2019-1543` This report relates to CVE-2019-1543, https://www.openssl.org/news/secadv/20190306.txt, which I reported to the OpenSSL maintainers a few days ago.
- **Yarn transfers npm credentials over unencrypted http connection** — `Node.js third-party modules` · `High` [↗](https://hackerone.com/reports/640904)
  - `CVE-2019-5448` **module name:** yarn **version:** 1.16.0 **npm page:** https://www.npmjs.com/package/yarn 166 703 downloads in the last day 849 928 downloads in the last week 3 772 290 downloads in the last month
