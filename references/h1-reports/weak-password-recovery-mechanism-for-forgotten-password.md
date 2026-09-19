# Weak Password Recovery Mechanism for Forgotten Password

_4 reports — High/Critical, disclosed_

- **Cookie steal through content Uri** — `Brave Software` · `Critical` [↗](https://hackerone.com/reports/876192)
  - A misconfiguration in a content provider is allowing Brave for Android to download internal files to Downloads folder, making them accessible to other apps.
- **Reset any password** — `pixiv` · `High` [↗](https://hackerone.com/reports/703972)
  - When I try to reset the password, the verification code of the mailbox is 6 digits, and there is no limit on the number of submissions, so I can reset the password of any user.
- **(Possible) staff account takeover via reset token bruteforce at helpdesk.bistudio.com** — `BOHEMIA INTERACTIVE a.s.` · `Critical` [↗](https://hackerone.com/reports/332632)
  - As stated in a brief exchange with @rvn in my other report ##312433, I might have found a logic flaw in the way https://helpdesk.bistudio.com handles the reset flow and tokens.
- **Password Reset Token Not Expired ** — `Infogram` · `High` [↗](https://hackerone.com/reports/283550)
  - Here in this scenario, I've found that the there's a kind of server side invalidation of Password Reset tokens.
