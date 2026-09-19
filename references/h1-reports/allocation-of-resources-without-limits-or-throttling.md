# Allocation of Resources Without Limits or Throttling

_3 reports — High/Critical, disclosed_

- **HTTP/2 CONTINUATION Flood Vulnerability** — `curl` · `High` [↗](https://hackerone.com/reports/3125820)
  - `CVE-2023-44487` // lib/http2.c (simplified snippet) while(recv_frame) { if(frame.type == NGHTTP2_CONTINUATION) { if(!h2->header_recvbuf) h2->header_recvbuf = Curl_add_buffer_init(); // Initialize buffer Curl_add_buffer(h2->header_recvbuf, frame.data, frame.length); // No limit } } Impact: Remot
- **Memory Leak in libcurl via Location Header Handling (CWE-770)** — `curl` · `High` [↗](https://hackerone.com/reports/3158093)
  - This report details a memory leak vulnerability in libcurl that occurs when processing HTTP 3xx redirect responses containing a Location: header.
- **Prototype pollution attack (lodash)** — `Node.js third-party modules` · `High` [↗](https://hackerone.com/reports/712065)
  - `CVE-2020-8203` I would like to report a prototype pollution vulnerability in lodash.
