# Password in Configuration File

_2 reports — High/Critical, disclosed_

- **Git repo on https://██████.mil/ discloses API password** — `U.S. Dept Of Defense` · `High` [↗](https://hackerone.com/reports/765825)
  - I found a .git repository on https://███████.mil/.git which discloses an API password for Yubikey on 2 different domains, together with full source code.
- **Insecure Zendesk SSO implementation by generating JWT client-side** — `Trint Ltd` · `High` [↗](https://hackerone.com/reports/638635)
  - app.trint.com implements SSO to Zendesk, it does this by using JWT as described at https://support.zendesk.com/hc/en-us/articles/203663816-Enabling-JWT-JSON-Web-Token-single-sign-on This functionality has not been implemented securely because the JWT generation happens in the cli
