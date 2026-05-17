---
title: "CNC Milling Machine Control System"
date: 2025-02-01
excerpt: "Embedded C control system for a 2-axis CNC milling machine on Raspberry Pi Pico — CC2511 Digital Logic & Embedded Systems, T1 2025."
header:
  teaser: cnc3.jpeg
collection: portfolio
---

**Course:** CC2511 Digital Logic and Embedded Systems Design Process — Trimester 1, 2025 — James Cook University, Cairns  
**Tools & Equipment:** Raspberry Pi Pico RP2040, CNC motor driver shield PCB, power supply PCB, soldering iron, stepper motors, spindle motor, PuTTY, C/Pico SDK, MATLAB

## Objective

Design and implement a complete software control system for a 2-axis CNC milling machine, with manual and automatic motor control, spindle control, and emergency stop.

## What I Did

- Hardware assembly — soldered the power PCB and wired all components into a working rig
- Wrote a modular C program with X/Y/Z step functions using the right-hand rule
- Implemented all software features — manual 10-direction control, coordinate input, return-to-home, PWM spindle with soft-start, and real-time emergency stop
- Fault diagnosis — resolved a faulty CNC shield, blown fuses, dead Pico boards, and an emergency stop bug encountered during testing

## Outcome

Successfully demonstrated all base requirements at assessment. Gained embedded C, GPIO/PWM, hardware troubleshooting, and teamwork skills.
