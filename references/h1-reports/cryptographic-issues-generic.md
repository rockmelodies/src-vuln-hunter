# Cryptographic Issues - Generic

_18 reports — High/Critical, disclosed_

- **elections.k8s.io uses weak session secret key, may place elections at risk** — `Kubernetes` · `High` [↗](https://hackerone.com/reports/1387366)
  - Hi there, I have been working on a new tool to detect misconfigured session signing across bug bounty programs, called CookieMonster.
- **HashDoS in V8** — `Node.js` · `High` [↗](https://hackerone.com/reports/3131758)
  - `CVE-2025-27209` The V8 release used in Node.js v24.0.0 has changed how string hashes are computed using rapidhash.
- **Improper error handling in async cryptographic operations crashes process** — `Node.js` · `High` [↗](https://hackerone.com/reports/2817648)
  - `CVE-2025-23166` The C++ method SignTraits::DeriveBits() may incorrectly call ThrowException() based on user-supplied inputs when executing in a background thread, crashing the Node.js process.
- **Signature Verification /// golang.org/x/crypto/ssh** — `Sifchain` · `High` [↗](https://hackerone.com/reports/1276384)
  - Crypto package are vulnerable to Improper Signature Verification " An attacker can craft an ssh-ed25519 or sk-ssh-...@openssh.com public key, such that the library will panic when trying to verify a signature with it.
- **[HTAF4-213] [Pre-submission] CVE-2018-2879 (padding oracle attack in the Oracle Access Manager) at https://█████████** — `U.S. Dept Of Defense` · `High` [↗](https://hackerone.com/reports/728110)
  - `CVE-2018-2879` We were able to identify CVE-2018-2879 in Oracle Access Manager, used on the https://██████ Link to the CVE: https://nvd.nist.gov/vuln/detail/CVE-2018-2879 This vulnerability is rated critical, and may allow unauthenticated attacker with network access via HTTP to compromise Orac
- **Apple Pay cryptogram replay and amount tampering** — `RBKmoney` · `High` [↗](https://hackerone.com/reports/996540)
  - During Apple Pay in-app or on-site payments the device generates a payment cryptogram, which contains a transaction ID, encrypted payment data, etc.
- **Some build dependencies are downloaded over an insecure channel (without subsequent integrity checks)** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/1039504)
  - Build jobs [mingw64 / openssl-1.1.1d](https://github.com/OpenVPN/openvpn/blob/master/.travis.yml#L87) and [mingw32 / openssl-1.0.2u](https://github.com/OpenVPN/openvpn/blob/master/.travis.yml#L91) download dependencies from build.openvpn.net and www.oberhumer.comover an i
- **RCE (Remote code execution) in one of DoD's websites ** — `U.S. Dept Of Defense` · `Critical` [↗](https://hackerone.com/reports/874924)
  - `CVE-2017-1000486` The targeted website is vulnerable to CVE-2017-1000486, by only running command was (whoami) to prove that the RCE exist has been run successfully on the target The target uses a vulnerable version of primefaces : Primetek Primefaces 5.x, that is vulnerable to a weak encryption f
- **█████████ - Insecure download cookie generation allows bypass of CAC authentication, access to deleted and locked files** — `U.S. Dept Of Defense` · `Critical` [↗](https://hackerone.com/reports/496326)
  - To download a file, ████ directs users to /██████████/Download.aspx and sets a cookie authenticating the download.
- **[Twitter Open Source] Releases were & are built/executed/tested/released in the context of insecure/untrusted code** — `X / xAI` · `High` [↗](https://hackerone.com/reports/505007)
  - [CWE-829: Inclusion of Functionality from Untrusted Control Sphere](https://cwe.mitre.org/data/definitions/829.html) [CWE-494: Download of Code Without Integrity Check](https://cwe.mitre.org/data/definitions/494.html) Twitter maintains several Open Source Projects under the [Twit
- **Critical vulnerability in JSON Web Encryption (JWE) - RFC 7516 Invalid Curve attack** — `Internet Bug Bounty` · `High` [↗](https://hackerone.com/reports/213437)
  - We found an issue in the JWE specification where it fails to warn the implementers about Invalid Curve attack.
- **RCE on https://█████/ Using CVE-2017-9248** — `U.S. Dept Of Defense` · `Critical` [↗](https://hackerone.com/reports/491668)
  - `CVE-2017-9248` Summary: https://█████████/ is hosting an unpatched version of the Telerik DialogHandler Telerik.Web.UI.DialogHandler.aspx allowing for the machine key to be brute forced.
- **WordPress Automatic Update Protocol Does Not Authenticate Updates Provided by the Server** — `WordPress` · `High` [↗](https://hackerone.com/reports/228854)
  - When the WordPress automatic update process is initiated (likely via wp-cron.php), this is the path the code takes: The only integrity check that is provided is that the Content-MD5 header sent by the WordPress server is [checked against the MD5 checksum of the file](https://
- **Samlify is vulnerable to signature wrapping** — `Node.js third-party modules` · `High` [↗](https://hackerone.com/reports/356284)
  - I would like to report a signature wrapping weakness in samlify It allows an attacker to modify a SAML token received from the IdP before validating it with the service provider **module name:** samlify **version:** 2.3.7 **npm page:** https://www.npmjs.com/package/samlify
- **Timing Attack in Google Authenticator - Per User Prompt** — `Ian Dunn` · `High` [↗](https://hackerone.com/reports/277534)
  - *Google Authenticator - Per User Prompt* contains a timing attack vulnerability in how it validates the application password for a user account.
- **NexTable: Credentials exposure** — `Eternal` · `High` [↗](https://hackerone.com/reports/120941)
  - There was an issue with how the NexTable was storing passwords for merchants.
- ** SSL/TLS Vulnerability at khanacademy.org** — `Khan Academy` · `High` [↗](https://hackerone.com/reports/207457)
  - `CVE-2016-2183` CVE - 2011 - 3389 Description : The SSL protocol, as used in certain configurations in Microsoft Windows and Microsoft Internet Explorer, Mozilla Firefox, Google Chrome, Opera, and other products, encrypts data by using CBC mode with chained initialization vectors, which allows m
- **Twitter iOS fails to validate server certificate and sends oauth token** — `X / xAI` · `High` [↗](https://hackerone.com/reports/168538)
  - `CVE-2016-10511` Twitter on iOS newest two versions (6.62 and 6.62.1) are affected, other versions not tested.
