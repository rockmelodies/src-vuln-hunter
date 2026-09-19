# Reliance on Untrusted Inputs in a Security Decision

_2 reports — High/Critical, disclosed_

- **[High] MITM via Insecure CA Path Handling in cURL (--capath, CURLOPT_CAPATH) (CWE-494: Download of Code Without Integrity Check)** — `curl` · `High` [↗](https://hackerone.com/reports/3120969)
  - `CVE-2022-32221` The --capath option in cURL and CURLOPT_CAPATH in libcurl accept any directory path without validation.
- **Helpdesk Takeover at dmc.datastax.com** — `DataStax` · `High` [↗](https://hackerone.com/reports/759454)
  - DNS record [dmc.datastax.com](dmc.datastax.com) is pointing to stale [dmc-support.zendesk.com](dmc-support.zendesk.com) domain on Zendesk which is available for takeover.
