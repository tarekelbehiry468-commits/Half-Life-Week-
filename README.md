# Starbie

![Starbie PCB front render](Renders/Starbie%20Front.png)

Starbie is a tiny motion-controlled digital pet built for [Hack Club Half Life](https://halflife.hackclub.com/). It sits on a desk, shows an animated pet on a 0.96-inch OLED, and reacts when the board is tilted, moved, or shaken.

## How it works

A Seeed Studio XIAO ESP32-C3 drives the display, reads an MPU6050 motion sensor, and optionally reads temperature and humidity from a DHT11. The firmware stores joy, energy, and fullness in the ESP32's non-volatile preferences. Four buttons and a tilt-controlled radial menu provide interaction.

- **Button 1:** open or confirm the radial menu.
- **Button 2:** show or hide the pet stats.
- **Tilt:** move through the radial menu.
- **Shake:** wake and play with the pet.

The default actions are nap, play, feed, and pet. The settings and sprite near the top of the Arduino sketch are intended to be beginner-editable.

## Hardware

The full parts list is in [`BOM.csv`](BOM.csv). The main parts are:

- Seeed Studio XIAO ESP32-C3
- 0.96-inch I2C OLED
- MPU6050 motion sensor
- DHT11 temperature/humidity sensor
- Four MX switches and keycaps
- One 10 kΩ resistor
- The custom Starbie PCB

The estimated cost is **$26.29 per kit** before shipping and taxes.

## Firmware

The Arduino sketch is at [`Firmware/Starbie/Starbie.ino`](Firmware/Starbie/Starbie.ino). Detailed setup and customization notes are in [`Firmware/README.md`](Firmware/README.md).

Quick start:

1. Install the ESP32 board package in Arduino IDE.
2. Select **XIAO_ESP32C3**.
3. Install Adafruit GFX, Adafruit SSD1306, Adafruit MPU6050, and the DHT sensor library.
4. Open `Firmware/Starbie/Starbie.ino`.
5. Select the board's serial port and upload.

A browser-based interaction preview is included at [`Firmware/simulator.html`](Firmware/simulator.html).

## PCB and fabrication

KiCad project sources are in [`PCB/`](PCB/):

- `Starbie.kicad_sch` — schematic
- `Starbie.kicad_pcb` — PCB layout
- `Starbie.kicad_pro` — KiCad project
- `libs/` — project-specific symbols and footprints

Ready-to-manufacture Gerber and drill files are in [`PCB/production/`](PCB/production/). Upload `Starbie Gerbers V1.0.zip` to a PCB manufacturer and review its preview before ordering. The extracted files are included alongside the archive for inspection.

## Repository layout

- `Firmware/` — Arduino firmware, instructions, and browser simulator
- `PCB/` — KiCad design sources and custom libraries
- `PCB/production/` — Gerber and drill fabrication outputs
- `Renders/` — front and back PCB renders
- `BOM.csv` — machine-readable bill of materials
- `BOM.md` and `JOURNAL.md` — Half Life platform mirrors

## Source and license

This repository imports the Starbie design from [SharKingStudios/Starbie](https://github.com/SharKingStudios/Starbie). The imported source is provided under the MIT License; see [`LICENSE`](LICENSE).
