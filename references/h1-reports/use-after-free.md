# Use After Free

_17 reports — High/Critical, disclosed_

- **Use-After-Free in SMB connection reuse (req->path dangling pointer after needle destruction)** — `curl` · `High` [↗](https://hackerone.com/reports/3591956)
  - A heap-use-after-free occurs in smb_send_open() at lib/smb.c when curl processes two SMB URLs targeting the same host.
- **Use-after-free in `curl_easy_ssls_export()` during callback re-entrancy** — `curl` · `High` [↗](https://hackerone.com/reports/3682666)
  - curl_easy_ssls_export() iterates the SSL session list and invokes a caller-provided callback for each entry.
- **Title: Use-After-Free in cURL Test Suite via Improper Cleanup of Global Handle** — `curl` · `High` [↗](https://hackerone.com/reports/3452725)
  - /*************************************************************************** * ***************************************************************************/ /*
- **Stack use-after-scope in HTTP/3 POST request processing via CURLOPT_POSTFIELDS** — `curl` · `High` [↗](https://hackerone.com/reports/3279804)
  - A stack use-after-scope vulnerability exists in libcurl's HTTP/3 request processing when using CURLOPT_POSTFIELDS with stack-allocated buffers.
- **Use-After-Free in OpenSSL Keylog Callback via SSL_get_ex_data() in libcurl** — `curl` · `High` [↗](https://hackerone.com/reports/3242005)
  - A Use-After-Free (UAF) vulnerability exists in libcurl when the OpenSSL SSL_CTX_set_keylog_callback is set.
- **sys_fsc2h_ctrl kernel stack free** — `PlayStation` · `High` [↗](https://hackerone.com/reports/2900606)
  - It is possible to cause a kernel stack free in the syscall sys_fsc2h_ctrl.
- **UAF on JSEthereumProvider** — `Brave Software` · `Critical` [↗](https://hackerone.com/reports/1977252)
  - There is a UAF (Use After Free) vulnerability in the renderer implementation of the Ethereum wallet.
- **Use-after-free in setsockopt IPV6_2292PKTOPTIONS (CVE-2020-7457)** — `PlayStation` · `High` [↗](https://hackerone.com/reports/1441103)
  - `CVE-2020-7457` The PS5 is vulnerable to https://hackerone.com/reports/826026 which easily grants kernel access to an attacker.
- **CVE-2021-22901: TLS session caching disaster** — `curl` · `High` [↗](https://hackerone.com/reports/1180380)
  - `CVE-2021-22901` lib/vtls/openssl.c ossl_connect_step1 sets up the ossl_new_session_cb sessionid callback with SSL_CTX_sess_set_new_cb, and adds association from data_idx and connectdata_idx to current conn and data respectively: SSL_CTX_set_session_cache_mode(backend->ctx, SSL_SES
- **Node.js: use-after-free in TLSWrap** — `Node.js` · `High` [↗](https://hackerone.com/reports/988103)
  - `CVE-2020-8265` Node.js: use-after-free in TLSWrap Node v14.11.0 (Current) is vulnerable to a use-after-free bug in its TLS implementation.
- **Use after free and out of bounds read in xmlrpc_decode()** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/477896)
  - `CVE-2019-9020` Malformed input can lead to use after free and out of bounds memory errors.
- **efree() on uninitialized Heap data in imagescale leads to use-after-free** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/478367)
  - `CVE-2016-10166` The core bug: https://bugs.php.net/bug.php?id=77269 This bugfix actually involves two vulnerabilities: a call to efree on uninitialized data and another free() based vulnerability.
- **Use-After-Free In IPV6_2292PKTOPTIONS leading To Arbitrary Kernel R/W Primitives** — `PlayStation` · `High` [↗](https://hackerone.com/reports/826026)
  - Due to missing locks in option IPV6_2292PKTOPTIONS of setsockopt , it is possible to race and free the struct ip6_pktopts  buffer, while it is being handled by ip6_setpktopt.
- **Exim use-after-free vulnerability while reading mail header involving BDAT commands** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/296991)
  - `CVE-2017-16943` Original article is [here](https://devco.re/blog/2017/12/11/Exim-RCE-advisory-CVE-2017-16943-en/) To explain this bug, we need to start with the memory management of exim.
- **mod_http2, memory corruption on early pushes (CVE-2019-10081)** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/677557)
  - `CVE-2019-10081` HTTP/2 very early pushes, for example configured with H2PushResource, could lead to an overwrite of memory in the pushing request's pool, leading to crashes.
- **CVE-2017-10966: Heap-use-after-free in Irssi <1.0.4** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/247028)
  - `CVE-2017-10966` 35 days after reading https://irssi.org/2017/05/12/fuzzing-irssi/, I was able to trigger a heap-use-after-free in irssi 1.0.2.
- **CVE-2017-12858: Heap UAF in _zip_buffer_free() / Double free in _zip_dirent_read()** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/260414)
  - `CVE-2017-12858` libzip is a C library for reading, creating, and modifying zip archives.
