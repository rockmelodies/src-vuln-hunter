# Improper Authorization

_15 reports — High/Critical, disclosed_

- **Email verification bypass via request  to endpoint "accounts.insightly.com/signup/provisionuser"** — `Insightly` · `Critical` [↗](https://hackerone.com/reports/2718253)
  - The vulnerability occurs in the "EmailAddress" parameter in the member creation area and affects all users.
- **Unauthenticated access to internal API at██████████.███.edu  [HtUS]** — `U.S. Dept Of Defense` · `High` [↗](https://hackerone.com/reports/1627980)
  - GET /api/person/Default.GetAllPersons HTTP/1.1 Host: appg3entcalapi.azurewebsites.net Dnt: 1 Upgrade-Insecure-Requests: 1 User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.0.0 Safari/537.36 Accept: text/html,application/xhtm
- **Subscription check bypass of NordVPN service ** — `Nord Security` · `High` [↗](https://hackerone.com/reports/2012443)
  - The reporter identified an issue in one of the NordVPN's infrastructure backend services responsible for checking if the user has a valid subscription.
- **[HTA2] Authorization Bypass on https://██████ leaks confidential aircraft/missile information** — `U.S. Dept Of Defense` · `Critical` [↗](https://hackerone.com/reports/736391)
  - There is an authorization bypass on https://██████ which allows a remote, unauthenticated attacker to bypass the "██████Single Sign-On" and view the application as an authenticated user.
- **Stealing Users OAuth authorization code via redirect_uri** — `pixiv` · `High` [↗](https://hackerone.com/reports/1861974)
  - Path traversal in OAuth redirect_uri which can lead to users authorization code being leaked to any malicious user.
- **Account takeover - improper validation of jwt signature (with regards  to experiation date claim)** — `Linktree` · `High` [↗](https://hackerone.com/reports/1760403)
  - Some backend services did not properly validate JWTs.
- **Hijack all emails sent to any domain that uses Cloudflare Email Forwarding** — `Cloudflare Public Bug Bounty` · `Critical` [↗](https://hackerone.com/reports/1419341)
  - The Email Routing feature enables Cloudflare users to create any number of custom email addresses and route all incoming messages to the user's preferred inboxes.
- **Claiming the listing of a non-delivery restaurant through OTP manipulation** — `Eternal` · `Critical` [↗](https://hackerone.com/reports/1330529)
  - **Summary:** Am able to claim any restaurant which is not claimed before.
- **Improper authorization allows disclosing users' notification data in Notification channel server** — `LY Corporation` · `High` [↗](https://hackerone.com/reports/1314162)
  - LINE Channel authentication provides separate authentication tokens for each LINE Channel.
- **[Transportation Management Services Solution 2.0] Improper authorization at  tmss.gsa.gov leads to data exposure of all registered users** — `U.S. General Services Administration` · `Critical` [↗](https://hackerone.com/reports/1175980)
  - I hope you are having a great Tuesday :) **Where:** https://tmss.gsa.gov/ **Who:** Unathenticated users **Why:** Improper Access Control at /tmssserver/api/public/customerregistration/{:id}/userId/
- **[dubmash] Lack of authorization checks - Update Sound Titles** — `Reddit` · `High` [↗](https://hackerone.com/reports/1102365)
  - During the security testing, it has been observed that the UpdateSound api is vulnerable to IDOR.
- **Email address of any user can be queried on Report Invitation GraphQL type when username is known** — `HackerOne` · `High` [↗](https://hackerone.com/reports/792927)
  - Email id of all hackerone users disclosure There is an flaw , with that i can get all hackerone users email id
- **Improper Authorization** — `Stripo Inc` · `High` [↗](https://hackerone.com/reports/751299)
  - i found an vulnerability on https://my.stripo.email/cabinet/#/users/orog_id , generally every user have an organisation and the organisation contain projects ,
- **Account Takeover via billing** — `Chaturbate` · `Critical` [↗](https://hackerone.com/reports/394329)
  - The hacker found that when subscribing to a fanclub the parameters could be manipulated to purchase a fanclub subscription for another user.
- **Shopify admin authentication bypass using partners.shopify.com** — `Shopify` · `Critical` [↗](https://hackerone.com/reports/270981)
  - @uzsunny reported that by creating two partner accounts sharing the same business email, it was possible to be granted "collaborator" access to any store without any merchant interaction.
