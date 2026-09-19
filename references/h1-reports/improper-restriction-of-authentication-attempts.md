# Improper Restriction of Authentication Attempts

_17 reports — High/Critical, disclosed_

- **Improper Restriction of Authentication Attempts in cURL** — `curl` · `Critical` [↗](https://hackerone.com/reports/3030158)
  - The authentication mechanism in cURL does not properly restrict the number of failed authentication attempts, allowing an attacker to brute-force credentials.
- **Password reset endpoint is not brute force protected** — `Nextcloud` · `High` [↗](https://hackerone.com/reports/1987062)
  - `CVE-2023-35172` Oversight of https://github.com/nextcloud/security-advisories/security/advisories/GHSA-v243-x6jc-42mp (https://hackerone.com/reports/1841665, but I can't judge the content there as it is not yet public).
- **Basic auth header on WebDAV requests is not bruteforce protected** — `Nextcloud` · `High` [↗](https://hackerone.com/reports/1879549)
  - `CVE-2023-32319` I hope you are doing well.
- **weak protection against brute-forcing on login api leads to account takeover ** — `Palo Alto Software` · `Critical` [↗](https://hackerone.com/reports/766875)
  - Weak protection against brute-forcing on login API: https://api.outpost.co/api/v1/login leads to account takeover on https://www.teamoutpost.com/
- **Brute Force of fabric-ca server admin account** — `Linux Foundation Decentralized Trust` · `High` [↗](https://hackerone.com/reports/411364)
  - Above conditions result in brute force to CA server admin account
- **Full account takeover in ███████ due lack of rate limiting in forgot password** — `U.S. Dept Of Defense` · `High` [↗](https://hackerone.com/reports/1059758)
  - Then bruteforce the ███.(You can use burp intruder) 5.
- **No rate limit lead to otp brute forcing** — `MTN Group` · `High` [↗](https://hackerone.com/reports/1060541)
  - There is no rate limit protection in the endpoint https://mtnonline.com/nim/submit , Which could lead to brute force otp code.
- **Grinchs website takendown with various other exploits** — `h1-ctf` · `Critical` [↗](https://hackerone.com/reports/1069034)
  - This is my first HackerOne CTF challenge writeup.
- **Lack of rate limitation on careers site allows the attacker to brute force the verification code** — `TikTok` · `High` [↗](https://hackerone.com/reports/1075827)
  - An attacker could have potentially attempted to brute force the verification code needed to reset a candidate's password by leveraging a lack of rate limiting on the TikTok careers portal.
- **Grinch-Networks taken down - hacky holidays CTF ** — `h1-ctf` · `Critical` [↗](https://hackerone.com/reports/1069189)
  - Day 1: flag{48104912-28b0-494a-9995-a203d1e261e7} Day 2: flag{b7ebcb75-9100-4f91-8454-cfb9574459f7} Day 3: flag{b705fb11-fb55-442f-847f-0931be82ed9a} Day 4: flag{972e7072-b1b6-4bf7-b825-a912d3fd38d6} Day 5: flag{2e6f9bf8-fdbd-483b-8c18-bdf371b2b004} Day 6: flag{18b130a7-3a79-4c70
- **A specially crafted value for the 'Cache-Digest' header causing crash in  chat.makerdao.com** — `BlockDev Sp. Z o.o` · `Critical` [↗](https://hackerone.com/reports/972936)
  - `CVE-2020-9490` A specially crafted value for the 'Cache-Digest' header causing crash
- **[H1-2006 2020]  Includes 1 free content discovery** — `h1-ctf` · `Critical` [↗](https://hackerone.com/reports/894198)
  - Got it!
- **load scripts DOS vulnerability** — `BlockDev Sp. Z o.o` · `High` [↗](https://hackerone.com/reports/826238)
  - `CVE-2018-6389` load scripts DOS vulnerability
- **Authorization for wp-admin directory are vulnerable to brute force.** — `Stripo Inc` · `High` [↗](https://hackerone.com/reports/788420)
  - The domain https://my.stripo.email in the directory /wp-admin are not blocking amount of request in the authorization form, this leads to bruteforce attack.
- **Bruteforce in admin panel** — `Nextcloud` · `High` [↗](https://hackerone.com/reports/341074)
  - Hello there, Admin panel of your website (https://nextcloud.com/wp-login.php) is vulnerable to bruteforce attacks as their is no rate-limiting.
- **The login of Hotor Not is Vulnerable to bruteforce.** — `Bumble` · `High` [↗](https://hackerone.com/reports/744692)
  - I was able to validate that The Login of HotorNot is Vulnerable to BruteForcing .
- **The Uber Promo Customer Endpoint Does Not Implement Multifactor Authentication, Blacklisting or Rate Limiting** — `Uber` · `High` [↗](https://hackerone.com/reports/293359)
  - The https://cn-sjc1.uber.com/rt/users/apply-clients-promotions customer endpoint used to apply Uber promotions does not implement multifactor authentication, IP address blacklisting for multiple failed attempts, or IP address-based rate limiting to prevent brute force bearer toke
