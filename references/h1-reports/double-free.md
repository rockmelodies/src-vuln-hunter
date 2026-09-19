# Double Free

_5 reports — High/Critical, disclosed_

- **Double fdrop on a socket through sys_netcontrol** — `PlayStation` · `High` [↗](https://hackerone.com/reports/3320669)
  - The netcontrol syscall has the following prototype: int netcontrol(int if_index, int cmd, void* buf, size_t buflen)
- **CVE-2022-28738: Double free in Regexp compilation** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/1549636)
  - `CVE-2022-28738` Due to a bug in the Regexp compilation process, creating a Regexp object with a crafted source string could cause the same memory to be freed twice.
- **SOCK_RAW sockets reachable from Webkit process allows triggering double free in IP6_EXTHDR_CHECK** — `PlayStation` · `High` [↗](https://hackerone.com/reports/943231)
  - Memory corruption can be achieved by sending fragmented IPv6 packets to loopback interface due to poor and inconsistent use of IP6_EXTHDR_CHECK.
- **Invalid write (or double free) triggers curl command line tool crash** — `curl` · `High` [↗](https://hackerone.com/reports/875775)
  - Whilst fuzzing libcurl built from git commit a158a09, a crash triggered by an invalid write (or maybe a double/invalid free) was found.
- **Linux kernel: CVE-2017-6074: DCCP double-free vulnerability** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/347282)
  - `CVE-2017-6074` CVE-2017-6074 [1] is a double-free vulnerability I found in the Linux kernel.
