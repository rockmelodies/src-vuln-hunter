# Client-Side Enforcement of Server-Side Security

_4 reports — High/Critical, disclosed_

- **Ability to  bypass Admin override on Cloudflare WARP Android** — `Cloudflare Public Bug Bounty` · `High` [↗](https://hackerone.com/reports/2043885)
  - `CVE-2023-3747` Zero Trust Administrators have the ability to disallow end users from disabling WARP on their devices.
- **Ability to bypass locked Cloudflare WARP on wifi networks.** — `Cloudflare Public Bug Bounty` · `High` [↗](https://hackerone.com/reports/1635748)
  - `CVE-2022-3512` Using warp-cli command "add-trusted-ssid", a user was able to disconnect WARP client and bypass the "Lock WARP switch" feature resulting in Zero Trust policies not being enforced on an affected endpoint.
- **I found another way to bypass Cloudflare Warp lock!** — `Cloudflare Public Bug Bounty` · `High` [↗](https://hackerone.com/reports/1605847)
  - `CVE-2022-3321` It was possible to bypass [Lock WARP switch feature](https://developers.cloudflare.com/cloudflare-one/connections/connect-devices/warp/warp-settings/#lock-warp-switch) on WARP iOS mobile client by enabling both "Disable for cellular networks" and "Disable for Wi-Fi networks" swit
- **Completely remove VPN profile from locked WARP iOS cient.** — `Cloudflare Public Bug Bounty` · `High` [↗](https://hackerone.com/reports/1633231)
  - `CVE-2022-3337` It was possible for a user to delete VPN profile from WARP mobile client on iOS platform despite the [Lock WARP switch](https://developers.cloudflare.com/cloudflare-one/connections/connect-devices/warp/warp-settings/#lock-warp-switch) feature being enabled on Zero Trust Platform
