# Improper Certificate Validation

_12 reports — High/Critical, disclosed_

- **Silent TLS Trust Model Hijacking via `CURL_CA_BUNDLE` Environment Variable Leads to MITM** — `curl` · `Critical` [↗](https://hackerone.com/reports/3418776)
  - curl is vulnerable to silent Man-in-the-Middle (MITM) attacks due to its design, which implicitly trusts the CA certificate path specified in the CURL_CA_BUNDLE environment variable.
- **SameSite restrictions are lifted, and SameSite:Strict cookie are being sent.** — `Brave Software` · `High` [↗](https://hackerone.com/reports/3253725)
  - `CVE-2018-12402` hello, Brave team.
- **Apple SecTrust legacy path accepts untrusted certificates on pre-10.14 macOS/iOS when built with USE_APPLE_SECTRUST** — `curl` · `High` [↗](https://hackerone.com/reports/3374554)
  - When libcurl is built with USE_APPLE_SECTRUST and runs on Apple OS versions that lack SecTrustEvaluateWithError (macOS <10.14 / iOS <12), the legacy verification path miscompares OSStatus to SecTrustResultType and never checks the SecTrust result.
- **curl allows SSH connection even if host is not in known_hosts** — `curl` · `High` [↗](https://hackerone.com/reports/2961050)
  - Curl does _not_ fail if the SSH host identity cannot be verified due to the host not being included in the .ssh/known_hosts file.
- **Undici does not use CONNECT or otherwise validate upstream HTTPS certificates when using a proxy** — `Node.js` · `High` [↗](https://hackerone.com/reports/1583680)
  - `CVE-2022-32210` **Summary:** When using Undici with its ProxyAgent, it does not use CONNECT or correctly verify the upstream server's HTTPS certificate.
- **Undici ProxyAgent vulnerable to MITM ** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/1599063)
  - Full GitHub advisory summarizing the issue is here: https://github.com/nodejs/undici/security/advisories/GHSA-pgw7-wx7w-2w33 The original Node.js HackerOne report is here: https://hackerone.com/bugs?report_id=1583680 This was fixed & disclosed in Undici v5.5.1.
- **Acronis True Image 2021 (windows) does not validate server hostname on a login TLS connection** — `Acronis` · `High` [↗](https://hackerone.com/reports/1070533)
  - Acronis True Image prior to 2021 Update 4 for Windows, Acronis True Image prior to 2021 Update 5 for Mac did not properly validate SSL certificate.
- **Acronis True Image  (Windows) does not validate server certificate on a TLS connection** — `Acronis` · `High` [↗](https://hackerone.com/reports/1056144)
  - Acronis True Image prior to 2021 Update 4 for Windows, Acronis True Image prior to 2021 Update 5 for Mac did not implement SSL certificate validation.
- **Only OpenSSL handles a CRL when passed in via CApath ** — `curl` · `High` [↗](https://hackerone.com/reports/713975)
  - Code in vtls/nss.c interprets CApath option differently than OpenSSL-using code, user can be mislead to unsecure use of curl/libcurl easily.
- **Remotely trigger an assertion on a TLS server with a malformed certificate string** — `Node.js` · `Critical` [↗](https://hackerone.com/reports/746733)
  - `CVE-2019-15604` Connecting to a NodeJS TLS server with a client certificate that has a type 19 string in its subjectAltName will crash the TLS server if it tries to read the peer certificate.
- **Silent omission of certificate hostname verification in LibreSSL and BoringSSL** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/329645)
  - `CVE-2018-8970` LibreSSL and BoringSSL implemented X509_VERIFY_PARAM_set1_host differently than OpenSSL.
- **The Microsoft Store Uber App Does Not Implement Certificate Pinning** — `Uber` · `Critical` [↗](https://hackerone.com/reports/293358)
  - The Microsoft Store Uber App (Windows Phone Architecture) does not properly implement certificate pinning.
