# Automations – Mettmann 🇩🇪

## Overview
This Home Assistant instance uses automations for lighting, security, device control, scheduling, and notifications.

---

## Lighting Automation

### Motion-based Lighting
- Kitchen: motion → light ON, no motion → OFF (with presence lock)
- Upstairs bathroom: automatic ON/OFF
- Aqara night light automation

### TV Lighting
- TV light ON
- TV light OFF
- Additional TV lighting automation

### Hue
- Hue automation (general)
- Hue automation OFF
- Hue automation (iPhone zone trigger)

### Outdoor / Misc Lighting
- Altana light (manual trigger)
- Christmas tree (seasonal automation)

---

## Tablet & Dashboard Automation

### Motion Control
- Tablet Lenovo: motion → screen ON
- No motion → screen OFF

### Screen Control
- Manual screen ON/OFF automation

### Battery Management
- Tablet battery charging ON/OFF
- Lenovo battery (Shelly control)

### Remote Control
- Lenovo remote actions

---

## Security & Presence

### Security Mode
- Away mode → motion triggers alarm
- Geofencing automation (presence detection)

### Windows / Doors
- Window close automation
- Window close automation (secondary)

---

## Smart Devices

### Cleaning
- Roomba automation

### Heating / Boiler
- Boiler ON
- Boiler OFF

---

## Garage Automation

- Garage auto ON
- Garage auto OFF
- Garage iOS control
- Garage iOS close

---

## Scheduling & Logic

### Shift System
- Shift plan based on anchor (Saturday 06:00)

---

## Notifications

### Birthdays 🎂
- Birthday today → notification + Alexa
- Birthday today (morning) → phone + Alexa
- Birthday tomorrow reminder

---

## Media / Scenes

- Cinema mode OFF (Pablo Kino)
- Cinema window close

---

## System

- Home Assistant backup (manual trigger)

---

## Key Automation Patterns

- Motion → action (lighting, tablet)
- Motion + condition (lux / presence)
- Time-based scheduling (shift system)
- Event-based notifications (birthdays)
- Device state automation (battery, garage)

---

## Notes

- Automations are designed to be lightweight and responsive
- Focus on real-life usability (tablet UI, presence detection)
- Combination of manual triggers + full automation
