# Out-of-bounds Read

_15 reports — High/Critical, disclosed_

- **Heap-buffer-overflow in `Curl_ssl_push_certinfo_len()` — sole bounds check is `DEBUGASSERT`** — `curl` · `High` [↗](https://hackerone.com/reports/3684614)
  - Curl_ssl_push_certinfo_len() in lib/vtls/vtls.c uses DEBUGASSERT(certnum < ci->num_of_certs) as its **only** bounds check before writing a heap pointer into ci->certinfo[certnum].
- **Heap Out-of-Bounds Read in lib/http2.c via Malformed PUSH_PROMISE Headers** — `curl` · `High` [↗](https://hackerone.com/reports/3506159)
  - Summary A heap-based out-of-bounds read vulnerability exists in libcurl's HTTP/2 implementation.
- **Heap Buffer Over-Read via Malicious SMB Server READ_ANDX Response** — `curl` · `High` [↗](https://hackerone.com/reports/3470095)
  - I discovered a heap buffer over-read vulnerability in libcurl's SMB protocol implementation.
- **Adam and the  Deadly  Injections** — `h1-ctf` · `Critical` [↗](https://hackerone.com/reports/1217702)
  - Hi team adding the flag here I will do the writeup in the below comments before the deadline itself Thanks Akshansh
- **RCE on CS:GO client using unsanitized entity ID in EntityMsg message** — `Valve` · `Critical` [↗](https://hackerone.com/reports/584603)
  - Title: RCE on CS:GO client using unsanitized entity ID in EntityMsg message Scope: csgo.exe Weakness: Out-of-bounds Read Severity: Critical (9.6) Link: https://hackerone.com/reports/584603 Date: 2019-05-19 17:49:21 +0000 By:
- **CS:GO Server -> Client RCE through OOB access in CSVCMsg_SplitScreen + Info leak in HTTP download** — `Valve` · `Critical` [↗](https://hackerone.com/reports/1070835)
  - Title: CS:GO Server -> Client RCE through OOB access in CSVCMsg_SplitScreen + Info leak in HTTP download Scope: csgo.exe Weakness: Out-of-bounds Read Severity: Critical (9.6) Link: https://hackerone.com/reports/1070835 Date: 2021-01-04
- **OOB reads in network message handlers leads to RCE** — `Valve` · `Critical` [↗](https://hackerone.com/reports/807772)
  - In Source engine games there are many network messages sent from the server to the client that take an entity index.
- **Out of Bounds Memory Read in exif_scan_thumbnail** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/675578)
  - `CVE-2019-11041` I have found and reported an out of bounds memory read in PHP [exif_scan_thumbnail] When PHP EXIF extension is parsing EXIF information from an image, e.g.
- **Out of Bounds Memory Read in exif_process_user_comment** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/675580)
  - `CVE-2019-11042` I have found and reported an out of bounds memory read in PHP [exif_process_user_comment] When PHP EXIF extension is parsing EXIF information from an image, e.g.
- **null pointer dereference in imap_mail** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/456727)
  - `CVE-2018-19935` in imap_mail if message args is null, in _php_imap_mail no check wheater message can get, so crash.
- **Tcpdump before 4.9.3 has a buffer over-read in print-dccp.c:dccp_print_option() (CVE-2018-16229)** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/724253)
  - `CVE-2018-16229` Tcpdump before 4.9.3 has a buffer over-read in print-dccp.c:dccp_print_option().
- **Tcpdump before 4.9.3 has a buffer over-read in print-802_11.c (CVE-2018-16227)** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/724243)
  - `CVE-2018-16227` Versions of tcpdump before 4.9.3 are vulnerable to a buffer over-read in print-802_11.c.
- **`base64-url` below 2.0 allocates uninitialized Buffers when number is passed in input** — `Node.js third-party modules` · `High` [↗](https://hackerone.com/reports/321692)
  - I would like to report an uninitialized Buffer allocation issue in base64-url.
- **`npmconf` (and `npm` js api) allocate and write to disk uninitialized memory content when a typed number is passed as input on Node.js 4.x** — `Node.js third-party modules` · `High` [↗](https://hackerone.com/reports/320269)
  - I would like to report a Buffer allocation issue in npmconf (and npm package js api).
- **`base64url` allocates uninitialized Buffers when number is passed in input on Node.js 4.x and below** — `Node.js third-party modules` · `High` [↗](https://hackerone.com/reports/321687)
  - I would like to report an uninitialized Buffer allocation issue in base64url.
