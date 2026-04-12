## Helpers (Input Entities)

Helpers are used to control system logic, UI behavior, scheduling, and integrations.

---

### UI & Dashboard

- `input_boolean.kiosk_mode` – enables / disables tablet kiosk mode

---

### Presence & State

- `input_boolean.abreise_check` – indicates departure / away state

---

### Alexa / Audio Control

- `input_select.alexa_pokoj` – selects target Alexa speaker
- `input_number.alexa_glosnosc` – controls volume level

---

### Scheduling (Shift System)

- `input_select.schicht` – current shift
- `input_datetime.schicht_kotwica` – anchor time for shift calculation
- `input_select.schicht_kotwica_typ` – type of shift anchor

---

### System

- `input_button.sysstem_bacpup_button_helfer` – manual backup trigger
