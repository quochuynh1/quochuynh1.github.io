---
title: "Function Generator — Colpitts Oscillator"
excerpt: "5 MHz single-supply function generator with sine and square wave outputs, adjustable amplitude, and JLCPCB-fabricated PCB — EE3300 Electronic Applications, Block 2 2026."
header:
  teaser: colpitts.jpeg
collection: portfolio
---

**Course:** EE3300 Electronic Applications — Block 2, 2026 — James Cook University, Cairns  
**Tools & Equipment:** LTSpice, KiCad, oscilloscope, function generator, multimeter, breadboard, various op-amps, NPN/PNP BJTs

![Cover Photo](/images/colpitts.jpeg){: style="border-radius: 8px"}

## Objective

Design a 5 MHz function generator with single-supply functionality, minimal harmonic distortion, voltage amplitude control, and square wave switching.

## Design Overview

<!-- IMAGE: The "Design Process" pipeline slide (slide 3) showing all five stages side by side — Basic Colpitts → Single Supply → Buffer → Harmonic Filter → Amplitude Control → Square Wave Generator -->
![Design Process](/images/functiongenerator/designoverview.png){: style="border-radius: 8px"}

## What I Did

### 1. Single-Supply Colpitts Oscillator

Adapted a Colpitts oscillator from previous practical work to operate on a single supply rail using a voltage divider bias network at the base; simulated each design iteration in LTSpice before breadboard testing, iterating between references, simulation, and measured results.

<!-- IMAGE: From slide 4 — the two-column comparison showing the final LTSpice schematic (voltage divider design) alongside its transient analysis and breadboard + oscilloscope test results -->
![Single Supply Oscillator](/images/functiongenerator/singlesupply.png){: style="border-radius: 8px"}

### 2. Buffer Stage

Evaluated and selected a buffer stage (emitter follower vs unity-gain op-amp).

<!-- IMAGE: From slide 5 — the emitter follower schematic and its transient analysis alongside the final breadboard and oscilloscope result at ~5 MHz -->
![Buffer Stage](/images/functiongenerator/bufferstage.png){: style="border-radius: 8px"}

### 3. Harmonic Filter Stage

Compared an RC low-pass filter against an LC low-pass filter using FFT analysis in LTSpice, selecting the LC design for superior harmonic rejection at 5 MHz.

<!-- IMAGE: From slide 6 — the side-by-side FFT plots (RC vs LC), showing the LC filter's clearly cleaner spectrum, plus the before/after oscilloscope traces -->
![Harmonic Filter FFT Comparison](/images/functiongenerator/filterstage.png){: style="border-radius: 8px"}

### 4. Adjustable Amplitude Control

Progressed from a common-emitter BJT with variable RC to an inverting op-amp (AD8061, 300 MHz bandwidth) with a variable feedback resistor via 10 kΩ potentiometer.

<!-- IMAGE: From slide 7 — the op-amp final design column: schematic, transient analysis, and breadboard with potentiometer highlighted -->
![Amplitude Control](/images/functiongenerator/amplitudecontrol.png){: style="border-radius: 8px"}

### 5. Square Wave Generator

Designed and evaluated three square wave generator approaches (differential pair, Schmitt trigger, comparator) with LTSpice simulation and bench testing of each.

<!-- IMAGE: From slide 8 — all three schematics with their transient analyses and corresponding oscilloscope results side by side -->
![Square Wave Generator](/images/functiongenerator/squarewave.png){: style="border-radius: 8px"}

### 6. PCB Design & Final Integration

Integrated all five stages into a complete KiCad schematic and PCB layout with a 3D model produced prior to JLCPCB fabrication.

<!-- IMAGE: From slide 9 — the KiCad PCB editor layout and the PCB 3D model render side by side -->
![KiCad PCB Layout and 3D Model](/images/functiongenerator/kicad.png){: style="border-radius: 8px"}

## Outcome

Delivered a fully functional 5 MHz function generator.

<!-- IMAGE: From slide 9 — the final breadboard assembly photo (colour-coded by stage) and the oscilloscope showing the clean 5.000 MHz sine wave output -->
![Final Assembly and Output](/images/functiongenerator/outcome.png){: style="border-radius: 8px"}
Developed strong skills in RF-range analogue circuit design, iterative simulation-driven design, and component selection at high frequencies. Gained experience critically comparing circuit topologies and justifying design decisions based on simulation and measured performance.