# Information Exposure Through an Error Message

_3 reports — High/Critical, disclosed_

- **Lack of rate limiting in https://███/PKI/PassReset.aspx leads to PII disclosure and potential account takeover** — `U.S. Dept Of Defense` · `Critical` [↗](https://hackerone.com/reports/2748003)
  - The password reset functionality of AFPC Secure is intended to be used by users who do not have a PKI credential for AFPC secure.
- **Able to log in with default ██████g creds at  https█████████████████████.mil ** — `U.S. Dept Of Defense` · `High` [↗](https://hackerone.com/reports/710813)
  - was able to use ████████████████████████ to log into this instance of Adobe Experience Manager, though it does not seem to be in used at the moment while navigating to https█████████████████████████.mil, I performed some fuzzing and found that /repository was available which as
- **information disclosure of secret_key_base via encoding charcters** — `GitLab` · `High` [↗](https://hackerone.com/reports/460545)
  - @paresh_parmar discovered an error page that was disclosing the value of the secret_key_base key of customers.gitlab.com to unauthenticated users, which would have allowed an attacker to arbitrarily decrypt signed cookies.
