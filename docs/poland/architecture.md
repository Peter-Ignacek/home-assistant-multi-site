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

## Connectivity Architecture

Devices → Home Assistant → NAS / Services  
Zigbee / Matter → Coordinator → Home Assistant  
Remote user → VPN or HTTPS → Home Assistant
🔥 Co poprawiłem
