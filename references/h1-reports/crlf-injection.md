# CRLF Injection

_5 reports — High/Critical, disclosed_

- **CRLF Injection / Protocol Smuggling in libcurl via CURLOPT_USERNAME (IMAP)** — `curl` · `Critical` [↗](https://hackerone.com/reports/3479984)
  - I have discovered a CRLF injection vulnerability in the IMAP protocol implementation of libcurl.
- **HTTP/3 Protocol Smuggling and Header Injection via CRLF in QPACK value conversion** — `curl` · `Critical` [↗](https://hackerone.com/reports/3479203)
  - A fundamental design flaw exists in how libcurl handles HTTP/3 (QUIC) response headers across all supported backends (ngtcp2, quiche, openssl-quic).
- **Protocol Smuggling / CRLF Injection via Gopher Protocol allows Arbitrary Command Injection** — `curl` · `High` [↗](https://hackerone.com/reports/3477023)
  - Summary: I have discovered that the Gopher protocol implementation in curl fails to properly sanitize newline characters (%0d%0) in the selector path.
- **Grafana RCE via SMTP server parameter injection** — `Aiven Ltd` · `Critical` [↗](https://hackerone.com/reports/1200647)
  - This report is similar to [#1180653](https://hackerone.com/reports/1180653), except with different parameter injection entrypoint.
- **'net/http': HTTP Header Injection in the set_content_type method** — `Ruby` · `High` [↗](https://hackerone.com/reports/1168205)
  - The set\_content\_type's parameter is not filtered to prevent the injection from altering the entire request.
