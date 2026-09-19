# Use of Cache Containing Sensitive Information

_1 reports — High/Critical, disclosed_

- **Cache Deception Allows Account Takeover** — `Expedia Group Bug Bounty` · `High` [↗](https://hackerone.com/reports/1698316)
  - I'm able to extract user's session (HASESSIONV3) as it is disclosed in a cacheable page, allowing me to access the ha.crumb token located in /traveler/profile/edit GET /traveler/profile/edit HTTP/2 Host: www.abritel.fr Cookie: HASESSIONV3=<use the token here> User-Agent: Mo
