# Information Exposure Through Sent Data

_4 reports — High/Critical, disclosed_

- **Alt-Svc bypasses credential leak protection (CVE-2018-1000007)** — `curl` · `High` [↗](https://hackerone.com/reports/3485826)
  - `CVE-2018-1000007` I found a bug where curl's Alt-Svc implementation fails to strip sensitive authentication headers (Authorization and Cookies) when remapping a connection to a different host or port.
- **Proxy-Authorization header is leaked to origin server after redirect from proxied to direct connection** — `curl` · `High` [↗](https://hackerone.com/reports/3480713)
  - curl leaks the Proxy-Authorization header to the origin server after following an HTTP redirect that transitions from a proxied connection to a direct connection (e.g.
- **Authorization Header Leak via --location-trusted in Curl** — `curl` · `High` [↗](https://hackerone.com/reports/2946924)
  - Curl's --location-trusted Option Leaks Authorization Header Across Domains The --location-trusted option in Curl forwards the Authorization header when following cross-origin redirects, exposing Basic Authentication credentials to untrusted hosts.
- ** Remote memory disclosure vulnerability in libcurl on 64 Bit Windows** — `curl` · `High` [↗](https://hackerone.com/reports/1444539)
  - libcurl (latest) contains a vulnerability that enables attackers to remotely read memory beyond the bounds of a buffer in the style of the infamous "heartbleed" vulnerability.
