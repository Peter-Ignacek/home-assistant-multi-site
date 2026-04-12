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
- Remote (via proxy): https://ha.de.ignacek.com

---

## Network

- Local network: 192.168.x.x
- Devices connected via Wi-Fi
- Remote access via reverse proxy

---

## Devices

### Smart Devices
- Shelly (switches / relays)

### Sensors
- Motion sensors (PIR)
- Illuminance sensors (lux)

---

## Integrations

- MQTT (device communication)
- Home Assistant Automations
- Shelly integration (native or MQTT)

---

## Automation Flow (Example)

Motion detected  
→ Check illuminance level  
→ If dark → turn on light / wake tablet screen  
→ After timeout → turn off

---

## Key Features

- Motion-based automation
- Light level (lux) conditional logic
- Tablet dashboard integration
- Remote access via domain

---

## Notes

- Designed as a lightweight system (UI + automation)
- No heavy storage or media services
- Focus on responsiveness and simplicity
### Core & System
- Home Assistant Supervisor
- System Monitor
- Backup
- HACS
- MQTT

### Smart Home & Devices
- Shelly (via native / MQTT)
- Philips Hue
- Tuya
- SwitchBot Cloud
- Matter / Thread
- ESPHome

### Media & Entertainment
- Apple TV
- Samsung Smart TV
- Google Cast
- Denon HEOS
- Logitech Harmony Hub
- Music Assistant
- Tautulli

### Voice & AI
- Alexa Media Player
- Google TTS
- OpenAI

### Network & IoT
- FRITZ!Box Tools
- FRITZ!SmartHome
- Bluetooth
- iBeacon Tracker
- UPnP/IGD

### Sensors & Data
- Netatmo
- Met.no (Weather)
- Sun (Sonne)

### Other Services
- OneDrive
- Remote Calendar
- Shopping List / To-do
- IPP (Printing)
- Fully Kiosk Browser

---

## Helpers (Input Entities)

Helpers are used to control logic, states, and UI behavior.

### System
- `input_button.system_backup` – manual backup trigger
- `input_button.sysstem_bacpup_button_helfer` – backup helper

### Automation Logic
- `input_boolean.abreise_check` – departure state
- `input_boolean.kiosk_mode` – tablet kiosk mode toggle

### Alexa / Audio
- `input_select.alexa_pokoj` – speaker selection
- `input_number.alexa_glosnosc` – volume control

### Scheduling (Shift System)
- `input_select.schicht` – current shift
- `input_datetime.schicht_kotwica` – shift anchor time
- `input_select.schicht_kotwica_typ` – shift type

### Misc
- `input_number.numer` – test / numeric input
