# Type Confusion

_2 reports — High/Critical, disclosed_

- **Incorrect Type Conversion in interpreting IPv4-mapped IPv6 addresses and below `curl` results in indeterminate SSRF vulnerabilities.** — `curl` · `Critical` [↗](https://hackerone.com/reports/2493548)
  - `CVE-2023-24329` Octal Type Handling of Errors in IPv4 Mapped IPv6 Addresses in curl allows unauthenticated remote attackers to perform indeterminate SSRF, RFI, and LFI attacks on many programs that rely on curl.
- **Insufficient Type Check leading to Developer ability to delete Project, Repository, Group, ...** — `GitLab` · `High` [↗](https://hackerone.com/reports/960244)
  - Similar bug to #858671, but this time with annotations mutation: DeleteAnnotation in ***app/graphql/mutations/metrics/dashboard/annotations/base.rb***
