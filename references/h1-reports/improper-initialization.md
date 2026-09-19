# Improper Initialization

_1 reports — High/Critical, disclosed_

- **Timeout-based race conditions make Uint8Array/Buffer.alloc non-zerofilled** — `Node.js` · `High` [↗](https://hackerone.com/reports/3405778)
  - `CVE-2025-55131` A flaw in Node.js's buffer allocation logic can expose uninitialized memory when allocations are interrupted, when using the vm module with the timeout option.
