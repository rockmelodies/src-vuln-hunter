# Buffer Underflow

_5 reports — High/Critical, disclosed_

- **Buffer overflow in strcpy** — `curl` · `Critical` [↗](https://hackerone.com/reports/2823554)
  - The vulnerability in the program is a classic case of a buffer overflow, triggered by the unsafe use of the strcpy() function, which lacks bounds checking.
- **Negative size parameter in mb_split** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/476178)
  - `CVE-2019-9025` mb_split doesn't correctly detect the length when the $string has an unfinished multibyte character at the end of the string.
- **CVE-2019-11043: a buffer underflow in fpm_main.c can lead to RCE in php-fpm** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/722327)
  - `CVE-2019-11043` The vulnerability exists in php-fpm because of missing bounds check in fpm_main.c.
- **[H1-2006 2020]  Got the flag** — `h1-ctf` · `Critical` [↗](https://hackerone.com/reports/887744)
  - Hey got the flag, will update the writeup soon BountyPay CTF Challenge Completed!
- **tcpdump: CVE-2018-14879 - buffer overflow in tcpdump.c:get_next_file()** — `Internet Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/724217)
  - `CVE-2018-14879` The release of tcpdump 4.9.3 brought many bug fixes, including one I submitted, CVE-2018-14879.
