---
title: "Additive Audio Mixer — Design, Simulation & PCB Fabrication"
excerpt: "Three-stage analogue audio mixer (BJT pre-amp, JFET summing stage, emitter-follower buffer) with JLCPCB-fabricated PCB — EE2300 Circuit Design, T3 2025."
header:
  teaser: ![Teaser Photo](/images/audiomixer/preamp2.jpeg)
collection: portfolio
---

**Course:** EE2300 Circuit Design — Trimester 3, 2025 — James Cook University, Cairns  
**Tools & Equipment:** LTSpice, KiCad, MATLAB, oscilloscope, function generator, multimeter, breadboard, JLCPCB-fabricated PCB, AM4011 microphone, 2N5484 JFET, 2N2904 BJT, soldering iron

![Cover Photo](/images/audiomixer/preamp2.jpeg){: style="border: 2px solid #4a90a4; border-radius: 8px;"}

## Objective

Design and implement a three-stage additive audio mixer capable of combining a microphone input and an audio jack signal, using a BJT common-emitter pre-amplifier, a self-biased JFET summing stage, and a BJT emitter-follower buffer to drive a low-impedance speaker load.

## What I Did

- Characterised the AM4010 electret microphone output (100 mV peak) and calculated the required pre-amplifier gain of 10 to match a 1 V audio jack signal; designed a common-emitter BJT amplifier with voltage divider bias and swamped emitter resistors using hand calculations, then verified in LTSpice before committing to PCB layout in KiCad
- Designed the pre-amp PCB in KiCad within JLCPCB 50×50 mm design rules, applied a continuous ground plane to minimise parasitic inductance, and had the board fabricated and assembled; bench-tested the finished PCB and measured a pre-amp output of 1.15 V, closely matching the simulated result
- Designed a self-biased 2N5485 JFET summing stage using a MATLAB-generated transfer curve for midpoint biasing; simulated the two-frequency mix in LTSpice (Vpp = 2.16 V), then validated on breadboard (measured Vpp = 2.2 V), analysing and explaining minor clipping due to JFET manufacturing tolerances
- Designed a BJT emitter-follower buffer stage to drive a 16 Ω speaker load; identified and resolved a clipping issue caused by insufficient quiescent current through iterative LTSpice tuning, and successfully demonstrated the complete three-stage system driving speakers live at assessment

## Gallery 🖼️

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; margin-top: 12px;">
  <img src="/images/audiomixer/IMG_7840.jpg" alt="Gallery photo" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;">
  <img src="/images/audiomixer/IMG_7707.jpg" alt="Gallery photo" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;">
  <img src="/images/audiomixer/IMG_7728.jpg" alt="Gallery photo" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;">
  <img src="/images/audiomixer/Screenshot%202025-11-26%20103726.png" alt="LTSpice simulation" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;">
  <img src="/images/audiomixer/Screenshot%202025-11-26%20103950.png" alt="LTSpice simulation" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;">
  <img src="/images/audiomixer/Screenshot%202025-11-28%20184633.png" alt="KiCad PCB layout" style="width: 100%; border-radius: 6px; object-fit: cover; aspect-ratio: 4/3;">
</div>

## Outcome

Successfully demonstrated a fully functional audio mixer driving a live speaker load at assessment. Gained end-to-end experience in the analogue design process — hand calculations, LTSpice simulation, KiCad PCB layout, JLCPCB fabrication, soldering, and bench testing. Deepened understanding of BJT biasing, JFET transfer characteristics, impedance matching, and the practical impact of component tolerances on real-world circuit performance.
