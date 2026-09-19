# Use of Hard-coded Cryptographic Key

_2 reports — High/Critical, disclosed_

- **Exposure of Hard-coded Private Keys and Credentials in curl Source Repository (CWE-321)** — `curl` · `Critical` [↗](https://hackerone.com/reports/3295650)
  - Multiple private/test RSA keys and example credentials were discovered embedded in the public curl source repository and associated documentation.
- **Slack DTLS uses a private key that is in the public domain, which may lead to SRTP stream hijack** — `Slack` · `High` [↗](https://hackerone.com/reports/531032)
  - The Janus server in use by Slack is configured using a certificate and private key that were previously distributed by default.
