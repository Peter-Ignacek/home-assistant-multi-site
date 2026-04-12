# Architecture – Mettmann 🇩🇪

## Overview
Lightweight Home Assistant setup focused on dashboards, UI automation, and local device control.

Runs in a Proxmox environment and integrates smart devices within the local network.

---

## Infrastructure

### Host
- Proxmox VE (Mini PC)
- Home Assistant running as VM or LXC

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


