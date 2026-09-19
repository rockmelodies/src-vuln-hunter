# Stack Overflow

_14 reports — High/Critical, disclosed_

- **Buffer Overflow in cURL Internal printf Function** — `curl` · `Critical` [↗](https://hackerone.com/reports/3462525)
  - A critical buffer overflow vulnerability exists in the curl_msprintf() function in cURL's internal printf implementation.
- **Stack Buffer Overflow in cURL Cookie Parsing Leads to RCE** — `curl` · `High` [↗](https://hackerone.com/reports/3340109)
  - I discovered a critical stack-based buffer overflow vulnerability in cURL's cookie parsing mechanism that can lead to remote code execution.
- **Stack-based Buffer Overflow in TELNET NEW_ENV Option Handling** — `curl` · `High` [↗](https://hackerone.com/reports/3230082)
  - Stack-based Buffer Overflow in TELNET NEW_ENV Option Handling A stack-based buffer overflow vulnerability exists in the libcurl TELNET handler.
- **[CS:GO] Unchecked texture file name with TEXTUREFLAGS_DEPTHRENDERTARGET can lead to Remote Code Execution** — `Valve` · `High` [↗](https://hackerone.com/reports/550625)
  - Title: [CS:GO] Unchecked texture file name with TEXTUREFLAGS_DEPTHRENDERTARGET can lead to Remote Code Execution Scope: csgo.exe Weakness: Stack Overflow Severity: High (8.0) Link: https://hackerone.com/reports/550625 Date: 2019-04-29 1
- **GoldSrc: Buffer Overflow in DELTA_ParseDelta function leads to RCE** — `Valve` · `Critical` [↗](https://hackerone.com/reports/484745)
  - The bug is triggered by 2 packets.
- **[GoldSrc] Remote Code Execution using malicious WAD list in BSP file** — `Valve` · `Critical` [↗](https://hackerone.com/reports/675710)
  - TEX_InitFromWad function calls COM_FileBase to get file name from a path into a buffer on the stack.
- **mb_strtolower (UTF-32LE): stack-buffer-overflow at php_unicode_tolower_full (CVE-2020-7065)** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/838127)
  - `CVE-2020-7065` PHP bug report (made public by the maintainers at the time of writing): https://bugs.php.net/bug.php?id=79371 Mitre CVE page: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-7065 Link to the release notes: https://www.php.net/ChangeLog-7.php#7.4.4 One of impacts is that t
- **Buffer overflow In hl.exe's launch -game argument allows an attacker to execute arbitrary code locally or from browser** — `Valve` · `High` [↗](https://hackerone.com/reports/832750)
  - Half Life 1 allows users to set various launch arguments when running the game from the command line, one of them is "**-game**" which specifies the game/mod to be launched.
- **VLC 4.0.0 - Stack Buffer Overflow (SEH)** — `VLC (European Commission - DIGIT)` · `High` [↗](https://hackerone.com/reports/489102)
  - Incorrect calculation of Buffer Size in rist module for VLC leading to Stack Overflow with SEH chain overwrite.
- **Perl $ENV Key Stack Buffer Overflow** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/272497)
  - `CVE-2017-12814` The CPerlHost::Add method in win32\perlhost.h is vulnerable to a stack buffer overflow.
- **Malformed playlist.txt in GoldSrc games leads to Access Violation & arbitrary code execution** — `Valve` · `High` [↗](https://hackerone.com/reports/504951)
  - A crafted playlist.txt can be used to exploit a stack overflow vulnerability in GameUI.dll that can lead to arbitrary code execution.
- **Stack overflow in XML Parsing** — `Notepad++` · `High` [↗](https://hackerone.com/reports/480883)
  - A stack buffer overflow vulnerability has been detected in XML parsing functionality on Notepad++.
- **Stack overflow in UnbindFromTree (browser can be crashed remotely)** — `Tor` · `High` [↗](https://hackerone.com/reports/264481)
  - I reported this bug to Mozilla approximately [9 months ago](https://bugzilla.mozilla.org/show_bug.cgi?id=1322307) and all versions of Firefox back to at least ESR45 and including current Nightly 57 builds are still vulnerable to this unpatched flaw.
- **mirb only: stack-buffer-overflow (OOB write) in main()** — `shopify-scripts` · `High` [↗](https://hackerone.com/reports/219870)
  - Triggered in 7e28510 (7 April 2017) with mirb only.
