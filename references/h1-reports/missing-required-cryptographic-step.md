# Missing Required Cryptographic Step

_2 reports — High/Critical, disclosed_

- **Missing AES-GCM Authentication Tag Validation and Improper Deprecation Handling** — `Node.js` · `High` [↗](https://hackerone.com/reports/3463949)
  - In Node.js' crypto module, the createDecipheriv states that "the authTagLength option defaults to 16 bytes and must be set to a different value if a different length is used." ([here](https://nodejs.org/api/crypto.html#class-decipheriv:~:text=the%20authTagLength%20option%20de
- **Constant-time comparison is not always implemented; critical areas are vulnerable to key-timing attacks** — `Monero` · `Critical` [↗](https://hackerone.com/reports/363680)
  - In my most superficial of reviews, constant-time comparison appears to not be globally implemented (at a glance, only implemented within the ref10 implementation).
