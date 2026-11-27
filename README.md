# Shaurya Goel

**Electrical & Computer Engineering @ USC · Class of 2028**
*PCBs, embedded firmware, and the drones, robots and handhelds built around them.*

I design circuit boards, write the firmware that runs on them, and build the hardware they live in. Currently leading an indoor drone swarm at Terra Labs and running additive manufacturing at USC's Baum Family Maker Space. Looking for summer 2027 hardware engineering internships.

[Website](https://shauryaee.dev) | [LinkedIn](https://www.linkedin.com/in/shaurya-goel-8a3a72270/) | Email: [goelshau@usc.edu](mailto:goelshau@usc.edu)

---

## Experience

### **Terra Labs** | Electrical Engineer → Project Lead
*Los Angeles, CA · Jan 2026 – Present*
* **Wisp (Project Lead, Aug 2026 – Present):** Leading a 10-person team building a ~15-drone indoor swarm tracked by a custom Ultra-Wideband positioning system. Details in [Projects](#wisp-indoor-drone-swarm).
* **Glyph (Electrical Engineer, Jan – May 2026):** Built the embedded electrical system for a drink-serving Unitree Go2 robot dog. Details in [Projects](#glyph-drink-serving-robot-dog).

### **Baum Family Maker Space, USC** | Additive Manufacturing Operations Lead
*Los Angeles, CA · Jan 2025 – Present*
* **Lab Operations:** Keep 15+ industrial Stratasys print jobs a week running with under 1 day/month of downtime and under 1-week turnaround, through hands-on repairs and preventive servicing.
* **Training:** Trained and certified 150+ users on oscilloscopes, multimeters, waveform generators, power supplies, soldering and lab safety.

### **Aero Design Team, USC** | General Member
*Los Angeles, CA · Jan 2025 – May 2025*
* **Glider Strobe:** Designed a 6 g strobe light for a competition glider when no commercial option met the weight limit. Details in [Projects](#glider-strobe-light).

---

## Projects

### Wisp: Indoor Drone Swarm
*Terra Labs · Project Lead · Aug 2026 – Present*

A swarm of about 15 palm-sized drones that fly indoors, tracked by an Ultra-Wideband (UWB) positioning system instead of infrared motion capture. The MVP, a UWB-tracked drone that flies to any commanded point in space, is flying; the full swarm is in progress.

* **Architecture:** Chose UWB TDoA over the other evaluated approaches for its simpler build and fleet-size-independent scaling. Wrote the PRD and BOM within a $3,500 budget.
* **Positioning PCB:** Designed in KiCad around an ESP32-S3-MINI-1 and a Qorvo DWM3000 radio linked over SPI. One design works as either a tag or an anchor.
* **Bring-Up:** Reflowed 20 boards at a 90% first-pass yield, then debugged and reworked the rest with an oscilloscope.
* **Results:** Holds position within **9 cm** with **50 Hz** position updates.
* **Leadership:** Set direction for a 10-person team, manage the GitHub org, and report to the club's executive board.

### Player1: LED-Matrix Handheld Game Console
*Personal Project · Jun 2026 – Present*

A handheld game console with a 24×24 RGB LED screen. A playable browser version runs on [shauryaee.dev](https://shauryaee.dev).

* **Display:** Drives 576 LEDs from an ESP32-S3 in ESP-IDF, split into 4 strands of 144 LEDs to reach a **~215 Hz** refresh rate.
* **Games:** Game rendering and controller input, plus video playback from a microSD card loaded through a companion mobile app.
* **Cartridges:** An open `.p1` game format: a few-KB file bundling WebAssembly code, assets and a 24×24 menu icon, run in a sandbox limited to drawing, buttons, sound and saves, so anyone can write a game in any language that compiles to WebAssembly.

### Player1 Power Board: USB-C PD Battery Management
*Personal Project · 2026*

A custom battery management PCB for Player1's 2S Li-ion pack.

* **Charging:** TI USB-C Power Delivery IC and buck-boost charger on board. Fast-charges at up to **45 W** and runs in reverse as a power bank.
* **No Firmware:** The PD IC configures the charger over I2C on its own, so charging needs no firmware.
* **Protection:** A standalone monitor IC handles cell protection and autonomous balancing.

### Glyph: Drink-Serving Robot Dog
*Terra Labs · Electrical Engineer · Jan 2026 – May 2026*

A Unitree Go2 robot dog that navigates to people and serves carbonated, flavored drinks. I built the embedded electrical system.

* **Pump Circuit:** MOSFET-gated 12 V circuit for 4 peristaltic pumps that mixes each drink from a carbonated base and 3 syrups, ready **6 seconds** after a cup is detected.
* **Firmware:** C++ in ESP-IDF on an ESP32-C6 running 3 FreeRTOS tasks: an IMU-driven fluid animation on 572 WS2812B LEDs, time-of-flight cup detection with a 4-state dispense state machine, and UART to a Jetson running ROS 2 Nav2.
* **Debugging:** Resolved I2C address conflicts so both sensors share one bus, and patched third-party libraries for ESP-IDF v5.5.

### Glider Strobe Light
*Aero Design Team · Jan 2025 – May 2025*

No commercial strobe met our competition glider's weight limit, so I made one.

* **Hardware:** Schematic, PCB layout, firmware and prototype in **2 weeks**. An ATtiny85 drives 2 A LED flashes through a MOSFET.
* **Weight:** **6 g** total.

---

## Skills

* **Hardware:** PCB design in KiCad, board assembly and bring-up, SMD and micro-soldering, oscilloscope debugging
* **Firmware:** ESP-IDF, FreeRTOS, I2C, UART, SPI
* **Software:** C, C++, Python

## Publication

S. Goel, "Experimental Analysis of Wireless Power Transfer Efficiency," *International Journal of Computer Trends and Technology (IJCTT)*, vol. 72, no. 1, pp. 12–18, 2024.
