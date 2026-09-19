# Cleartext Transmission of Sensitive Information

_5 reports — High/Critical, disclosed_

- **Insecure WebSocket Usage in curl Documentation and Examples (CWE-319: Cleartext Transmission of Sensitive Information)** — `curl` · `High` [↗](https://hackerone.com/reports/3295652)
  - The curl source repository contains official documentation and example code that demonstrate WebSocket connections using the insecure ws:// protocol instead of the secure wss://.
- **Plaintext leakage of DNS requests in Windows 1.1.1.1 WARP client** — `Cloudflare Public Bug Bounty` · `High` [↗](https://hackerone.com/reports/1941390)
  - `CVE-2023-2754` The Cloudflare WARP client for Windows assigns loopback IPv4 addresses for the DNS Servers, since WARP acts as local DNS server that performs DNS queries in a secure manner, however, if a user is connected to WARP over an IPv6-capable network, te WARP client did not assign loopba
- **Leak of Google Sheets API credentials** — `Azbuka Vkusa` · `High` [↗](https://hackerone.com/reports/965314)
  - —
- **Reflected XSS and sensitive data exposure, including payment details, on lioncityrentals.com.sg** — `Uber` · `High` [↗](https://hackerone.com/reports/340431)
  - lioncityrentals.com.sg employed a Wordpress installation that possessed a vulnerable plugin, Formidable Forms, which was vulnerable to reflected XSS, and exposed sensitive form data.
- **Login form on non-HTTPS page** — `Rockstar Games` · `High` [↗](https://hackerone.com/reports/214571)
  - Summary: ======= A page on a microsite is not fully protected by an SSL certificate.
