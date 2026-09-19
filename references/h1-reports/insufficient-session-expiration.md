# Insufficient Session Expiration

_4 reports — High/Critical, disclosed_

- **Can use the Reddit android app as usual even though revoking the access of it from reddit.com** — `Reddit` · `Critical` [↗](https://hackerone.com/reports/1632186)
  - For the last 4 days, I kept testing reddit web.
- **Web Server Predictable Session ID on EdgeSwitch ** — `Ubiquiti Inc.` · `High` [↗](https://hackerone.com/reports/774393)
  - `CVE-2020-8234` In EdgeSwitch legacy web interface the SIDSSL cookie for admin can be guessed, enabling the attacker to obtain high privileges and get a root shell by a Command injection.
- **Узнаем несколько цифр номера телефона юзера (можно флудить смс), всего раз узнав его remixsid и его ид юзера, и установка оффлайна юзерам.** — `VK.com` · `High` [↗](https://hackerone.com/reports/390126)
  - Недостаточные проверки сессии.
- **Session replay vulnerability in www.urbandictionary.com** — `Urban Dictionary` · `High` [↗](https://hackerone.com/reports/216294)
  - I considered titling this bug "*Session tokens not expiring*", which is what you need to tell your development team.
