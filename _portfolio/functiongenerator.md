---
title: "Function Generator — Colpitts Oscillator"
excerpt: "5 MHz single-supply function generator with sine and square wave outputs, adjustable amplitude, and JLCPCB-fabricated PCB — EE3300 Electronic Applications, Block 2 2026."
header:
  teaser: colpitts.jpeg
collection: portfolio
---

**Course:** EE3300 Electronic Applications — Block 2, 2026 — James Cook University, Cairns  
**Tools & Equipment:** LTSpice, KiCad, oscilloscope, function generator, multimeter, breadboard, various op-amps, NPN/PNP BJTs

## Objective

Design a 5 MHz function generator with single-supply functionality, minimal harmonic distortion, voltage amplitude control, and square wave switching.

## What I Did

- Adapted a Colpitts oscillator from previous practical work to operate on a single supply rail using a voltage divider bias network at the base; simulated each design iteration in LTSpice before breadboard testing, iterating between references, simulation, and measured results
- Evaluated and selected a buffer stage (emitter follower vs unity-gain op-amp); compared an RC low-pass filter against an LC low-pass filter using FFT analysis in LTSpice, selecting the LC design for superior harmonic rejection at 5 MHz
- Designed adjustable amplitude control, progressing from a common-emitter BJT with variable RC to an inverting op-amp (AD8061, 300 MHz bandwidth) with a variable feedback resistor via 10 kΩ potentiometer; designed and evaluated three square wave generator approaches (differential pair, Schmitt trigger, comparator) with LTSpice simulation and bench testing of each
- Integrated all five stages into a complete KiCad schematic and PCB layout with a 3D model produced prior to JLCPCB fabrication, delivering a working 5 MHz function generator with sine and square wave outputs and voltage amplitude control

## Outcome

Delivered a fully functional 5 MHz function generator. Developed strong skills in RF-range analogue circuit design, iterative simulation-driven design, and component selection at high frequencies. Gained experience critically comparing circuit topologies and justifying design decisions based on simulation and measured performance.
