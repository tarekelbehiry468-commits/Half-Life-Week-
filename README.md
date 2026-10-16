# Starbie

![Starbie fully assembled 3D render](Renders/Starbie%20Render.png)

Starbie is a tiny motion-controlled digital pet created as the Week 1 beginner hardware project for [Hack Club Half Life](https://halflife.hackclub.com/). It sits on a desk, shows an animated pet on a 0.96-inch OLED, and reacts when the board is tilted, moved, or shaken.

## How it works

A Seeed Studio XIAO ESP32-C3 drives the display, reads an MPU6050 motion sensor, and optionally reads temperature and humidity from a DHT11. The firmware stores joy, energy, and fullness in the ESP32's non-volatile preferences. Two buttons and a tilt-controlled radial menu provide interaction.

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
- Two MX switches and keycaps
- One 10 kΩ resistor
- The custom Starbie PCB

The estimated cost is **$24.73 per kit** before shipping and taxes.

## Build and use

1. Order the PCB using [`PCB/production/Starbie Gerbers V1.0.zip`](PCB/production/Starbie%20Gerbers%20V1.0.zip).
2. Solder the XIAO ESP32-C3, OLED, MPU6050, DHT11, 10 kΩ resistor, and two MX switches into their labeled PCB footprints. The modules and switches mount through plated holes and are held by their soldered pins.
3. Fit the two keycaps and inspect the board for reversed modules, missed joints, or solder bridges before applying power.
4. Connect the board over USB-C and upload the Arduino sketch using the firmware steps below.
5. Press Button 1 to open or confirm the radial menu, tilt the board to choose an action, and press Button 2 to show or hide the pet stats.

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

## 3D design files

- [`PCB/Starbie.glb`](PCB/Starbie.glb) — viewable populated-board assembly
- [`Renders/Starbie.blend`](Renders/Starbie.blend) — Blender source used for the assembled render
- [`PCB/libs/3D Models/`](PCB/libs/3D%20Models/) — STEP models used by the PCB assembly
- [`Renders/Starbie Render.png`](Renders/Starbie%20Render.png) — complete populated-board render
- [`Renders/Starbie Front.png`](Renders/Starbie%20Front.png) and [`Renders/Starbie Back.png`](Renders/Starbie%20Back.png) — PCB front and back renders

![Starbie PCB front render](Renders/Starbie%20Front.png)

![Starbie PCB back render](Renders/Starbie%20Back.png)

## Repository layout

- `Firmware/` — Arduino firmware, instructions, and browser simulator
- `PCB/` — KiCad design sources and custom libraries
- `PCB/production/` — Gerber and drill fabrication outputs
- `PCB/libs/3D Models/` — component STEP models used in the assembly
- `Renders/` — assembled, front, and back renders plus the Blender source
- `Week 1 Guide.md`, `Week 1 Care Package.zip`, and `GuidePics/` — original design walkthrough, library bundle, and images
- `BOM.csv` — machine-readable bill of materials
- `BOM.md` and `JOURNAL.md` — Half Life platform mirrors

## Source, credit, and license

This repository imports the Starbie design from [SharKingStudios/Starbie](https://github.com/SharKingStudios/Starbie). The original board identifies Logan Peterson as its designer. The imported source is provided under the MIT License; see [`LICENSE`](LICENSE).

For a Forge-specific gap review, see [`FORGE_CHECKLIST.md`](FORGE_CHECKLIST.md).
