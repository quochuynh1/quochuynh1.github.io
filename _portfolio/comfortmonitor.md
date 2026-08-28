---
title: "Lecture Theatre Occupancy and Comfort Monitor"
excerpt: "RP2040-based occupancy and comfort monitoring system with VOC, temperature/humidity, light, and IR beam-break sensing, BLE data transmission, and a live web dashboard — CC3501 Embedded Systems, Assignment 2 (Project 12), 2026."
header:
  teaser: comfortmonitor.png
collection: portfolio
---

**Course:** CC3501 Embedded Systems — Assignment 2, 2026 — James Cook University, Cairns  
**Team:** Group project with Elijah and Joe; supervised by Luke and Laurence  
**Tools & Equipment:** KiCad, JLCPCB, Raspberry Pi Pico (RP2040, C/C++, Pico SDK), oscilloscope, multimeter, soldering station

![Cover Photo](/images/comfortmonitor/comfortcover.png){: style="border-radius: 8px"}

## Objective

Design and build an embedded system for Project 12 that monitors occupancy and environmental comfort in a lecture theatre, combining multiple sensor inputs into a single comfort score and broadcasting live data over Bluetooth Low Energy (BLE) to a web dashboard.

## What I Did

- Interfaced a range of I2C and 1-Wire sensors to the RP2040 — an AGS10 VOC sensor for air quality, an HDC1080 for temperature and humidity, a BH1750 for ambient light, and a DS18B20 for supplementary temperature sensing — writing and debugging individual drivers before integrating them into a single firmware pipeline
- Designed a secondary doorframe PCB using paired IR beam-break sensors to detect direction of travel, incrementing or decrementing an occupancy count as people entered or exited the theatre
- Designed the main PCB in KiCad to host the RP2040, sensor headers, RN4871 BLE module, and ILI9341 TFT display, with a power management circuit combining a MCP73833 battery charger, TPS63031 buck-boost regulator, and SPX3819 LDO, with Schottky diode OR-ing between USB and battery supply; debugged schematic errors and generated JLCPCB manufacturing files (Gerbers, BOM, CPL), sourcing components via LCSC
- Traced and resolved a USB power surge fault on the assembled PCB by isolating a short circuit using multimeter resistance measurements, and resolved GPIO/BOOTSEL pin conflicts that were interfering with firmware flashing
- Implemented a local ILI9341 TFT display showing real-time sensor readings and occupancy count on the device itself, deriving a combined comfort score from VOC, temperature, humidity, and light readings
- Set up UART communication over an RN4871 BLE Click module to transmit sensor data wirelessly, building a Web Bluetooth dashboard connecting directly from the browser to the RN4871 as a fallback path, in parallel with a Raspberry Pi gateway version, to broadcast live sensor data and the overall comfort score to a webpage

## Gallery 🖼️

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; margin-top: 12px;">
  <img src="/images/comfortmonitor/batteryschematic.png" alt="Sensor cluster wired to the Pico" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;">
  <img src="/images/comfortmonitor/finalschematic.png" alt="Doorframe occupancy sensor PCB" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;">
  <img src="/images/comfortmonitor/finalpcb.png" alt="Main PCB and power circuit" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;">
  <img src="/images/comfortmonitor/jlcpcb.png" alt="Main PCB and power circuit" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;">

</div>

## Outcome

Delivered a working occupancy and comfort monitoring system with sensor data successfully transmitted over UART via BLE and displayed both locally on the TFT and remotely via the web dashboard. Developed strong skills in multi-sensor embedded systems integration, PCB design and fault-finding at the hardware level, and wireless data transmission via BLE. Gained experience working as part of a team on a full-stack embedded project spanning schematic design, firmware, and web-facing data visualisation.
