 Architecture – Poland 🇵🇱

## Overview
Primary Home Assistant instance acting as the central smart home system.

Handles automation, storage integration, device management, and monitoring.

Runs in a Proxmox environment and integrates smart devices within the local network.

---

## Infrastructure

### Host
- Proxmox VE
- Home Assistant running as VM

### Storage
- UGREEN NAS (main data storage)
- Network shares (NFS / SMB)

### Access
- Local: http://homeassistant.local:8123
- Remote (via reverse proxy): https://ha.pl.ignacek.com
- VPN: WireGuard

---

## Network

- Local network: 192.168.x.x

### Connectivity
- Wi-Fi (main devices)
- Zigbee (low-power sensors via Zigbee2MQTT)
- Matter / Thread (modern IoT devices)

### Remote Access
- Reverse proxy (HTTPS)
- VPN (WireGuard)

---

## System Role

- Main smart home controller
- Device integration hub
- Automation engine
- Monitoring and logging

---

## Devices (Overview)

### Lighting
- Philips Hue lighting system
- Aqara Ceiling Light T1M
- Colorful Ceiling Light 36W
- Indoor room lighting (Wohnzimmer, Küche, Flur, Badezimmer)
- TV / cinema accent lighting
- Outdoor lighting (Garten, Eingangstür, Altana)

### Smart Switches & Plugs
- Aqara Light Switch H2 EU
- Shelly relays and switches
- Smart outlets for household devices
- Power-controlled plugs for appliances and lighting

### Covers / Garage / Openings
- Smart roller shutters (multiple rooms and zones)
- Smart garage door opener
- Window and door automation

### Sensors & Safety
- Motion sensors
- Illuminance sensors
- PIR / wave radar sensors
- Smoke detectors (multiple floors)
- Door / window state monitoring

### Heating / Climate
- Aqara Retrofit Valves T1
- Smart radiator valves
- Boiler heating element control

### Tablet / Dashboard
- Lenovo tablet dashboard
- Screen control
- Motion detection
- Kiosk mode control

### Zigbee / Thread / IoT Infrastructure
- Zigbee2MQTT
- SLZB-06 coordinator
- Matter / Thread capable network components

### Network & Access Infrastructure
- UniFi network
- Dedicated firewall / access rules for services
- IoT Wi-Fi networks
- Reverse proxy / remote access components

### Media & Entertainment
- Hue Sync Box
- TV lighting integration
- Cinema lighting zones

### Utility / Appliance Control
- Washing machine outlet
- Dryer outlet
- Fridge control
- Additional smart power outlets
