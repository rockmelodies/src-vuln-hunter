# Array Index Underflow

_6 reports — High/Critical, disclosed_

- **[MK8DX] Improper metadata validation 2** — `Nintendo` · `High` [↗](https://hackerone.com/reports/1812732)
  - This vulnerability impacts: The competition/tournaments ([SimpleSearchObject](https://github.com/kinnay/NintendoClients/wiki/Matchmake-Extension-Protocol-(MK8D)#simplesearchobject-structure)) contains a 'metadata' field, it is used by the game to store tournament data such as:
- **Array Index Underflow--http rpc** — `Monero` · `High` [↗](https://hackerone.com/reports/825091)
  - parserse_base_utils.h:197 const unsigned char tmp = isx[(int)*++it]; Int type will cause the array subscript to appear negative and read wrong data, Solution: const unsigned char tmp = isx[(unsigned char)*++it]; [add details for how we can reproduce the issue]
- **Signedness issue in ClassInfo message handler leads to RCE on CS:GO client** — `Valve` · `Critical` [↗](https://hackerone.com/reports/876719)
  - Title: Signedness issue in ClassInfo message handler leads to RCE on CS:GO client Scope: csgo.exe Weakness: Array Index Underflow Severity: Critical (9.6) Link: https://hackerone.com/reports/876719 Date: 2020-05-17 20:31:35 +0000 By:
- **https://██████ vulnerable to CVE-2020-3187 - Unauthenticated arbitrary file deletion in Cisco ASA/FTD** — `U.S. Dept Of Defense` · `Critical` [↗](https://hackerone.com/reports/987090)
  - `CVE-2020-3187` Hi team , while testing i found a host ip https://█████████ which belong to DoD (██████████.mil) running web services interface of Cisco ASA/FTD and it is vulnerable to CVE-2020-3187 - Unauthenticated arbitrary file deletion in Cisco ASA/FTD.
- **Unchecked weapon id in WeaponList message parser on client leads to RCE** — `Valve` · `Critical` [↗](https://hackerone.com/reports/513154)
  - Let's look at WeaponList message parser code in the HLSDK: int CHudAmmo::MsgFunc_WeaponList(const char *pszName, int iSize, void *pbuf ) { BEGIN_READ( pbuf, iSize );
- **Your page has 2 blocking CSS resources. This causes a delay in rendering your page.** — `Node.js` · `Critical` [↗](https://hackerone.com/reports/365968)
  - This report was not deemed to be a security vulnerability and the reporter was asked to open an issue upstream to fix publicly.
