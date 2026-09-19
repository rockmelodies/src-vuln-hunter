# Missing Authorization

_2 reports — High/Critical, disclosed_

- **Unrestricted access to quiesce functionality in dss.api.playstation.com REST API leads to unavailability of application** — `PlayStation` · `High` [↗](https://hackerone.com/reports/993722)
  - ---- Unrestricted access to the quiesce function via a PUT request to https://dss.api.playstation.com/api/application/state makes the application unreachable for an uncertain amount of time.
- **Access token stealing.** — `PlayStation` · `High` [↗](https://hackerone.com/reports/821896)
  - https://my.playstation.com/auth/response.html suffers from a misconfiguration which leads to access token stealing.
