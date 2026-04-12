# Architecture – Mettmann 🇩🇪

## Overview
Lightweight Home Assistant setup focused on dashboards, UI automation, and local device control.

Runs in a Proxmox environment and integrates smart devices within the local network.

---

## Infrastructure

### Host
- Proxmox VE (Mini PC)
- Home Assistant running on VM 

### Access
- Local: http://homeassistant.local:8123
- Remote (via reverse proxy): https://ha.de.ignacek.com
- VPN: WireGuard

---

## Network

- Local network: 192.168.x.x
- Connectivity:
  - Wi-Fi (main devices)
  - Zigbee (low-power sensors)
  - Matter / Thread (modern IoT devices)
- Remote access:
  - Reverse proxy (HTTPS)
  - VPN (WireGuard)

---

## Connectivity Architecture

Devices → Home Assistant (local network)  
Zigbee / Matter → Coordinator / Thread Border Router → Home Assistant  
Remote user → VPN or HTTPS proxy → Home Assistant

---
## Devices (Overview)

### Lighting (Philips Hue & Smart Lighting)
- Hue Go
- Hue Play
- Hue Play Gradient Lightstrip
- Hue Lightstrip Plus
- Hue Surimu panels
- Hue Infuse ceiling lights
- Hue Tento panel
- Ambient & room lighting (Wohnzimmer, Schlafzimmer, Küche, Flur, Badezimmer)

### Smart Lighting & Effects
- TV LED lighting
- Play Gradient Tube
- Computerbereich & gaming lighting
- RGB ambient lighting (desk, komoda)

### Blinds / Covers
- Aqara Roller Shade Driver (multiple zones)

### Sensors
- Motion sensors (Hue / Zigbee)
- Illuminance sensors
- Presence detection

### Tablet / Dashboard
- Lenovo Tab M11 (Fully Kiosk)
- Motion detection
- Screen control (on/off)
- Kiosk mode

### Smart Devices
- Roomba
- Boiler
- Smart plugs & switches (Shelly / Zigbee / Tuya)

### Climate
- Smart radiator valves (living room, bedroom, kitchen)

### Media & Audio
- Samsung TV
- Denon AVR
- Alexa devices (Echo, Echo Pop, Echo Dot)



