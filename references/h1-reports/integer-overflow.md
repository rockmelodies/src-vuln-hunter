# Integer Overflow

_7 reports — High/Critical, disclosed_

- **Cookie Max-Age Integer Overflow Vulnerability** — `curl` · `Critical` [↗](https://hackerone.com/reports/3516186)
  - The cookie parsing code in lib/cookie.c contains an integer overflow vulnerability when processing the Max-Age attribute of HTTP cookies.
- **integer Overflow in MQTT Protocol Handling Allows Bypassing Message Size Limit** — `curl` · `High` [↗](https://hackerone.com/reports/3508500)
  - A logic error involving an integer overflow (specifically, an unsigned integer underflow) exists in the lib/mqtt.c file within the mqtt_publish function.
- **MQTT Protocol Violation & Integer Overflow in libcurl** — `curl` · `High` [↗](https://hackerone.com/reports/3484319)
  - **Vulnerability Type:** CWE-190 **Component:** lib/mqtt.c **Function:** mqtt_decode_len libcurl does not correctly enforce the MQTT v3.1.1 specification limit for the “Remaining Length” field when decoding incoming packets.
- **Integer overflow vulnerability ** — `Glovo` · `Critical` [↗](https://hackerone.com/reports/1562515)
  - In one of my previous reports i send parameter tampering report vulnerability.
- **Integer overflow in CipherUpdate** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/1113025)
  - `CVE-2021-23840` I reported an integer overflow to the OpenSSL security list on Dec 13, 2020 and it was fixed in OpenSSL 1.1.1j.
- **CVE-2017-8798 - miniupnp getHTTPResponse chunked encoding integer signedness error** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/227344)
  - `CVE-2017-8798` An integer signedness error was found in miniupnp's miniwget allowing an unauthenticated remote entity typically located on the local network segment to trigger a heap corruption or an access violation in miniupnp's http response parser when processing a specially crafted chunk
- **Integer overflow leading to buffer overflow** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/424447)
  - `CVE-2018-18311` There exists an integer overflow in Perl_my_setenv @ util.c : 2070 2070: void Perl_my_setenv(pTHX_ const char *nam, const char *val) { ...
