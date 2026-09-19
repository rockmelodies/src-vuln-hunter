# Off-by-one Error

_2 reports — High/Critical, disclosed_

- **urlapi: off-by-one in custom scheme validation skips last character** — `curl` · `High` [↗](https://hackerone.com/reports/3598358)
  - In lib/urlapi.c, the set_url_scheme() function has an off-by-one error when validating custom scheme names.
- **Exim off-by-one RCE vulnerability** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/322935)
  - `CVE-2018-6789` I found an off-by-one in Exim MTA utility function.
