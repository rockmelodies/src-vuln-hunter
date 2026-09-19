# Inclusion of Sensitive Information in an Include File

_1 reports — High/Critical, disclosed_

- **Critical Information Disclosure via /talos/api/v1/files/upload** — `Bykea` · `Critical` [↗](https://hackerone.com/reports/3228011)
  - @sameer_ali discovered a vulnerability in the file upload functionality where uploaded files were first stored on the server before being sent to S3.
