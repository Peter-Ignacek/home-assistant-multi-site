## Helpers (Input Entities)

Helpers are used for system state control, scheduling logic, and manual triggers.

---

### System

- `input_button.system_backup` – manual trigger for Home Assistant backup

---

### UI & Dashboard

- `input_boolean.kiosk_mode` – enables / disables kiosk mode for dashboard devices

---

### House Mode / State

- `input_select.hausmodus` – global house mode (e.g. home / away / night)

---

### Scheduling & Logic

#### Waste Collection (Test Setup)
- `input_boolean.wywoz_smieci_test` – enables test scenario for waste collection
- `input_select.wywoz_smieci_test_kiedy` – defines collection timing
- `input_select.wywoz_smieci_test_frakcja` – defines waste type

---

### Misc

- `input_number.numer` – generic numeric helper (test / utility)
