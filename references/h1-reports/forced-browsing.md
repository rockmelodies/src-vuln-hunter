# Forced Browsing

_2 reports — High/Critical, disclosed_

- **One Click Account Hijacking via Unvalidated Deeplink** — `TikTok` · `High` [↗](https://hackerone.com/reports/1500614)
  - A WebView Hijacking vulnerability was found on the TikTok Android application via an un-validated deeplink on an un-sanitized parameter.
- **[Android org.torproject.android] Possible to force list of bridges** — `Tor` · `High` [↗](https://hackerone.com/reports/252626)
  - Do the following thing from ADB to emulate the activity start: adb am start -n org.torproject.android/.OrbotMainActivity -a android.intent.action.VIEW -d bridge://xxx
