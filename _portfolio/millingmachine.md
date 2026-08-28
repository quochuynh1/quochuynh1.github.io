---
title: "CNC Milling Machine Control System"
excerpt: "Embedded C control system for a 2-axis CNC milling machine on Raspberry Pi Pico — CC2511 Digital Logic & Embedded Systems, T1 2025."
header:
  teaser: cnc3.jpeg
collection: portfolio
---

**Course:** CC2511 Digital Logic and Embedded Systems Design Process — Trimester 1, 2025 — James Cook University, Cairns  
**Tools & Equipment:** Raspberry Pi Pico RP2040, CNC motor driver shield PCB, power supply PCB, soldering iron, stepper motors, spindle motor, PuTTY, C/Pico SDK, MATLAB

![Cover Photo](/images/millingmachine/cnc.png){: style="border-radius: 8px"}

## Objective

Design and implement a complete software control system for a 2-axis CNC milling machine, with manual and automatic motor control, spindle control, and emergency stop.

## What I Did

- Hardware assembly — soldered the power PCB and wired all components into a working rig
- Wrote a modular C program with X/Y/Z step functions using the right-hand rule
- Implemented all software features — manual 10-direction control, coordinate input, return-to-home, PWM spindle with soft-start, and real-time emergency stop
- Fault diagnosis — resolved a faulty CNC shield, blown fuses, dead Pico boards, and an emergency stop bug encountered during testing

## Gallery 🖼️

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; margin-top: 12px;">
  <a href="/images/millingmachine/powerpcb.png"><img src="/images/millingmachine/powerpcb.png" alt="Soldered power PCB" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
  <a href="/images/millingmachine/steppermotors.png"><img src="/images/millingmachine/steppermotors.png" alt="Wiring of stepper motors and driver shield" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
  <a href="/images/millingmachine/cncshield.png"><img src="/images/millingmachine/cncshield.png" alt="CNC motor driver shield" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
  <a href="/images/millingmachine/rpipico.png"><img src="/images/millingmachine/rpipico.png" alt="Raspberry Pi Pico controller" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
  <a href="/images/millingmachine/board.png"><img src="/images/millingmachine/examplecode.png" alt="Example control code" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
  <a href="/images/millingmachine/examplecode.png"><img src="/images/millingmachine/examplecode.png" alt="Example control code" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;"></a>
</div>

## Outcome

Successfully demonstrated all base requirements at assessment. Gained embedded C, GPIO/PWM, hardware troubleshooting, and teamwork skills.