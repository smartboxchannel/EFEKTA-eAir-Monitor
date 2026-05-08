# EFEKTA eAir Monitor

![EFEKTA eAir Monitor](https://raw.githubusercontent.com/smartboxchannel/EFEKTA-eAir-Monitor/refs/heads/main/IMAGES/01.png)

# EFEKTA eAir Monitor — Zigbee CO₂ Sensor with e-ink Display

[![Zigbee 3.0](https://img.shields.io/badge/Zigbee-3.0-blue.svg)](https://zigbeealliance.org/)
[![Home Assistant](https://img.shields.io/badge/Home%20Assistant-Compatible-18bcf2.svg)](https://www.home-assistant.io/)
[![DIY](https://img.shields.io/badge/DIY-Device-orange.svg)](http://efektalab.com/eAir/)

**DIY Zigbee air quality monitor** based on Sensirion SCD41 sensor featuring a 2.9-inch energy-efficient e-ink display. Perfect for Home Assistant and other smart home systems (Zigbee2MQTT, ZHA, etc.).

> ⚠️ **Important!** This device **does NOT work** with Tuya systems or the SmartLife app.

![Device Overview](https://raw.githubusercontent.com/smartboxchannel/EFEKTA-eAir-Monitor/refs/heads/main/IMAGES/device_overview.jpg)

## 📟 Display Information

The e-ink screen shows:
- Battery level
- Weekday and date
- Zigbee network connection status
- Current CO₂ level

Plus a **48-hour CO₂ history graph**.

![Display UI](https://raw.githubusercontent.com/smartboxchannel/EFEKTA-eAir-Monitor/refs/heads/main/IMAGES/display_ui.jpg)

## ⚙️ Features

| Feature | Description |
|---------|-------------|
| **Measurement Modes** (switchable) | • Fast – every 1 minute<br>• Medium – every 5 minutes<br>• Slow – every 10 minutes |
| **Color Inversion** | Switch between black-on-white and white-on-black |
| **Power** | 2× AA batteries (not included) |
| **Sensor** | Sensirion SCD41 |
| **Temperature Range** | 0 ~ +50 °C |

## 🔗 Zigbee Details

### Zigbee2MQTT Exposed Entities

- `co2` – Measured CO₂ level (ppm)
- `battery` – Remaining charge (%) – updates every 6h or by button press
- `battery_low` – Flag for low battery
- `lifetime` – Device uptime since manufacture
- `power_mode` – Current measurement mode (fast/medium/slow)
- `invert_color` – Toggle display color scheme
- `forced_recalibration` – Manual FRC (fresh air, 10 min)
- `manual_forced_recalibration` – Manual FRC using another trusted CO₂ sensor (15 min co-location)
- `automatic_self_calibration` – ASC, 1-week cycle (enabled by default)
- `sensor_reset` – Factory reset of CO₂ sensor

> ℹ️ After sending any command, you must **press the button on the device** to wake it and apply the command.

### Network Joining & Removal

- **Join network**: Press and hold button → after ~1 sec display shows "searching" → keep holding (5-8 sec) to start joining. Device exits search after 15 sec if no open network found.
  > Place device 1-2 meters from coordinator/router with good signal.

- **Leave network**: Press and hold button for 10 sec → display confirms leaving → device erases all network settings.

## 🛠️ Technical Specifications

| Parameter | Value |
|-----------|-------|
| Model | eAir Monitor |
| Protocol | Zigbee 3.0 |
| Dimensions | 10.0 × 4.3 × 2.2 cm |
| CO₂ Sensor | SENSIRION SCD41 |
| Operating temp. | 0 ~ +50 °C |
| Power | 2× AA batteries (not included) |


