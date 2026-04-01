<h1 align="center">Z906 ESPHOME config for HA</h1>
<p align="center">A simple ESPHOME YAML configuration for controlling the  <b>Logitech Z906</b> speaker system via <b>IR</b> and Home Assistant.
</p>
<p align="center">
  <img src="https://img.shields.io/badge/ESPHome-compatible-blue?style=for-the-badge&logo=esphome" alt="ESPHome">
  <img src="https://img.shields.io/badge/Home%20Assistant-compatible-41BDF5?style=for-the-badge&logo=home-assistant" alt="Home Assistant">
  <img src="https://img.shields.io/github/created-at/Adrian-Cxll/Z906-ESPHome-remote?style=for-the-badge" alt="Created At">
  <img src="https://img.shields.io/github/last-commit/Adrian-Cxll/Z906-ESPHome-remote?style=for-the-badge" alt="Last Commit">
  <img src="https://img.shields.io/github/stars/Adrian-Cxll/Z906-ESPHome-remote?style=for-the-badge" alt="Stars">
  <img src="https://img.shields.io/github/license/Adrian-Cxll/Z906-ESPHome-remote?style=for-the-badge" alt="License">
  <img alt="GitHub Downloads (all assets, latest release)" src="https://img.shields.io/github/downloads/Adrian-Cxll/Z906-ESPHome-remote/latest/total?style=for-the-badge">
</p>

<br><br>

This script allows you to fully replace your Z906 remote. Using an ESP8266/ESP32 and an IR transmitter, you can control your Logitech speakers directly from Home Assistant.

The IR codes were captured using a Flipper Zero.

---

### Why Use This?
 
- your remote control has stopped working
- you want to switch TV-inputs seamlessly via Smart Home integration

**IMPORTANT:** This will not work if your IR-Receiver stopped working.

 ---
 
### Available Functions

- Power
- volume up
- volume down
- mute
- effect
- level
- input
- input[1-5] individually
- aux
- test

### Requirements

- ESP8266 or ESP32
- IR transmitter
- Home Assistant with ESPHome add-on
- Logitech Z906

### Wiring

| ESP GPIO (pin) | component      |
| -------------  | ------------- |
| D2   (pin: 4)  | IR LED Anode + 100Ω |
| GND  | IR LED Kathode |


### Notes

- The IR LED must be precisely aimed at the IR receiver. Depending on the LED, the beam may be very narrow.
- If you want to place the ESP further away, usa a transistor circuit and power the IR with 5V.
- You can use other μC, but you have to specify the correct model at the top of the YAML.
- If you want to switch inputs, remember that GPIO is not equal to the pin value in YAML! (e.g. GPIO=2 == pin: 4)
