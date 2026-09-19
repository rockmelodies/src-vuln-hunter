# NULL Pointer Dereference

_8 reports — High/Critical, disclosed_

- **important: Apache HTTP Server: Crash resulting in Denial of Service in mod_proxy via a malicious request (CVE-2024-38477)** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/2585375)
  - `CVE-2024-38477` I reported this vulnerability through the official Apache HTTP Server security email on April 1, 2024, and received a fix along with a CVE number on July 1, 2024.
- **NULL Pointer dereference in idn.c** — `curl` · `Critical` [↗](https://hackerone.com/reports/2171309)
  - A NULL Pointer dereference vulnerability is present in idn.c source code.
- **[WiiU/Switch] nullptr dereference in the ENL framework** — `Nintendo` · `High` [↗](https://hackerone.com/reports/1540907)
  - Nintendo uses its own private library called ENL, it can do matchmaking using NEX (networking library for Nintendo game servers) and communication between players is done using PIA (UDP peer-to-peer networking library) This library is used in many Nintendo games including:
- **[MK8DX] Improper metadata parsing** — `Nintendo` · `Critical` [↗](https://hackerone.com/reports/1688309)
  - This vulnerability impacts: The competition/tournaments ([SimpleSearchObject](https://github.com/kinnay/NintendoClients/wiki/Matchmake-Extension-Protocol-(MK8D)#simplesearchobject-structure)) contains a 'metadata' field, it is used by the game to store tournament data such as:
- **Denial of Service: nghttp2 use of uninitialized pointer** — `Node.js` · `Critical` [↗](https://hackerone.com/reports/335608)
  - While investigating https://hackerone.com/reports/335533 and while following the same reproduction steps, I uncovered a bug in nghttp2 that causes use of an uninitialized pointer for an altsvc frameresulting in crash.
- **CVE-2017-10965: Null pointer dereference in Irssi <1.0.4 ** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/247027)
  - `CVE-2017-10965` 34 days after reading https://irssi.org/2017/05/12/fuzzing-irssi/, I was finally able to trigger a null pointer dereference in irssi 1.0.2.
- **null pointer dereference and segfault in tile-count-merge** — `Mapbox` · `High` [↗](https://hackerone.com/reports/245221)
  - This crash was triggered with 642f773  while fuzzing tile-count-merge with AFL on Debian 8 x64.
- **null pointer dereference in Sass::Eval::operator()(Sass::Map*)** — `LibSass` · `High` [↗](https://hackerone.com/reports/221287)
  - Feeding @P#{(20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
