# Use of Inherently Dangerous Function

_2 reports — High/Critical, disclosed_

- **Unexpected input validation of octal literals in nodejs v15.12.0 and below returns defined values for all undefined octal literals.** — `Node.js` · `Critical` [↗](https://hackerone.com/reports/1141623)
  - `CVE-2021-28918` Unexpected input validation of octal literals in the nodejs implementation of V8 JavaScript engine V8 9.0.257.13 and below returns defined values for all undefined octal literals where otherwise should return undefined.
- **URL Spoof / Brave Shield Bypass** — `Brave Software` · `High` [↗](https://hackerone.com/reports/255991)
  - Improper URL parsing in Brave allows an attacker to spoof the hostname shield settings are applied to.
