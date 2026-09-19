# ASI05: Unexpected Code Execution (RCE)

_1 reports — High/Critical, disclosed_

- **MQTT CONNACK Packet Type Bypass leads to RCE via Malicious Broker** — `curl` · `Critical` [↗](https://hackerone.com/reports/3712343)
  - mqtt_verify_connack() in lib/mqtt.c never checks that the received packet type is actually a CONNACK (0x20).
