---
title: "NTC Thermistor Temperature Sensing System"
date: 2024-08-01
excerpt: "Analogue temperature sensing circuit with op-amp buffer, Arduino firmware, and live IoT dashboard — EG1012 Electric Circuits, Sem 2 2024."
header:
  teaser: thermistor.png
collection: portfolio
---

**Course:** EG1012 Electric Circuits — Semester 2, 2024 — James Cook University, Cairns  
**Tools & Equipment:** Multimeter, laboratory thermometer, breadboard, LM258 op-amp, WeMos microcontroller, MATLAB, Desmos, Arduino IDE, ThingSpeak API

## Objective

Design and implement a complete temperature sensing circuit using an NTC thermistor, capable of accurately reading temperatures between 0–100°C and transmitting data wirelessly via a microcontroller.

## What I Did

- Calibrated an NTC thermistor across a 10–70°C range and validated measured resistance values against the Steinhart–Hart equation using MATLAB
- Designed an optimal voltage divider using a derived formula to maximise output voltage range across the full 0–100°C operating range
- Performed Thévenin equivalent circuit analysis and identified that source impedance exceeded ADC input requirements, necessitating a buffer stage
- Designed and analysed an op-amp voltage follower using the LM258 to resolve the impedance mismatch between the voltage divider and the microcontroller
- Assembled and debugged the full circuit on a breadboard, integrated Arduino firmware, and streamed live temperature data to a ThingSpeak dashboard via API

## Outcome

The completed system successfully read and transmitted temperature in real time, with a measured error of approximately 1.4°C attributed to component tolerances and non-ideal op-amp behaviour. Gained hands-on experience in sensor calibration, impedance matching, op-amp circuit design, and the full pipeline from analogue sensing to digital output.
