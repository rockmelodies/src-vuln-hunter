# Cross-Site Scripting (XSS)

_1 reports — High/Critical, disclosed_

- **[Meetup][World ID][OIDC] Insufficient Filtering of "state" Parameter in Response Mode form_post leads to XSS and ATO** — `Tools for Humanity` · `Critical` [↗](https://hackerone.com/reports/2515808)
  - A lack of proper validation in the state parameter of the World ID OIDC authentication logic allowed the injection of HTML characters into the response body when using form_post as the OIDC response mode.
