---
title: "NTC Thermistor Temperature Sensing System"
excerpt: "Analogue temperature sensing circuit with op-amp buffer, Arduino firmware, and live IoT dashboard — EG1012 Electric Circuits, Sem 2 2024."
header:
  teaser: thermistor.png
collection: portfolio
---

**Course:** EG1012 Electric Circuits — Semester 2, 2024 — James Cook University, Cairns  
**Tools & Equipment:** Multimeter, laboratory thermometer, breadboard, LM258 op-amp, WeMos microcontroller, MATLAB, Desmos, Arduino IDE, ThingSpeak API

![Cover Photo](/images/thermistor/thermcover.png){: style="border-radius: 8px"}

## Objective

Design and implement a complete temperature sensing circuit using an NTC thermistor, capable of accurately reading temperatures between 0–100°C and transmitting data wirelessly via a microcontroller.

## What I Did

- Calibrated an NTC thermistor across a 10–70°C range and validated measured resistance values against the Steinhart–Hart equation using MATLAB
- Designed an optimal voltage divider using a derived formula to maximise output voltage range across the full 0–100°C operating range
- Performed Thévenin equivalent circuit analysis and identified that source impedance exceeded ADC input requirements, necessitating a buffer stage
- Designed and analysed an op-amp voltage follower using the LM258 to resolve the impedance mismatch between the voltage divider and the microcontroller
- Assembled and debugged the full circuit on a breadboard, integrated Arduino firmware, and streamed live temperature data to a ThingSpeak dashboard via API

## Gallery 🖼️

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; margin-top: 12px;">
  <a href="/images/thermistor/calcs.png"><img src="/images/thermistor/calcs.png" alt="Breadboard circuit assembly" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
  <a href="/images/thermistor/voltagefollower.png"><img src="/images/thermistor/voltagefollower.png" alt="Voltage divider circuit diagram" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
  <a href="/images/thermistor/matlab.png"><img src="/images/thermistor/matlab.png" alt="LM258 op-amp buffer stage" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
  <a href="/images/thermistor/graph.png"><img src="/images/thermistor/graph.png" alt="MATLAB calibration analysis" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
  <a href="/images/thermistor/breadboard.png"><img src="/images/thermistor/breadboard.png" alt="WeMos microcontroller wiring" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
  <a href="/images/thermistor/dashboard.png"><img src="/images/thermistor/dashboard.png" alt="Live ThingSpeak dashboard" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
</div>

## Outcome

The completed system successfully read and transmitted temperature in real time, with a measured error of approximately 1.4°C attributed to component tolerances and non-ideal op-amp behaviour. Gained hands-on experience in sensor calibration, impedance matching, op-amp circuit design, and the full pipeline from analogue sensing to digital output.