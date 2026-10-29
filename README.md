# HEMT & Laser Bench

Interactive, self-consistent band diagrams and device characteristics for high-electron-mobility transistors and heterostructure lasers, built around exemplars from commercial products and current research. Single self-contained `index.html` (300 K). Spun off from [junction-bench](https://github.com/muonide/junction-bench) and sharing its Schrödinger–Poisson and drift–diffusion solver.

Live: https://muonide.github.io/hemt-laser/ (append `#hemt` or `#laser` to open a tab).

## Status

**HEMT tab (phase 1).** Self-consistent Schrödinger–Poisson cross-section under the gate, n_s and gate C–V versus V_G, and a deliberately simple transistor model (charge control from the solved n_s, velocity saturation, access resistance, parasitic capacitance) giving transfer and output curves, g_m and f_T. Exemplars: GaAs pHEMT, AlGaN/GaN HEMT on SiC, InP HEMT. Basic mode (introductory notes) and Advanced mode (graduate notes, full layer editing).

**Laser tab.** Placeholder; physics arrives in phase 3.

## Roadmap

| Phase | Content |
|---|---|
| 2 | Self-consistent hole subbands; gate dielectrics and p-GaN gates. HEMT exemplars: p-GaN-gate normally-off GaN on Si, metamorphic HEMT, InAlN/GaN, ScAlN/GaN, N-polar GaN deep-recess, AlN/GaN p-channel (2DHG), β-(AlGa)₂O₃/Ga₂O₃ MODFET, strained Ge/SiGe hole quantum well, hydrogen-terminated diamond (surface-transfer-doped 2DHG) |
| 3 | Laser physics: gain spectrum with strain, 1D waveguide mode and confinement factor, threshold and L–I. Exemplars: 9xx nm InGaAs/AlGaAs, 1310/1550 nm InP MQW, 450 nm InGaN |
| 4 | 650 nm AlGaInP red, InGaN green, interband cascade (GaSb), AlGaN UV-C laser diode |
| 5 | Model sections, UX pass, publish |

**Deferred (noted, not scheduled):** vertical-cavity surface-emitting lasers (need a DBR/cavity solver) and quantum cascade lasers (need intersubband transitions and injector alignment under bias). Quantum-dot lasers on Si are out of scope for a 1D solver.

## Model limits

The transistor model has no short-channel effects, self-heating, trapping or gate leakage; f_T is an intrinsic estimate with a lumped parasitic capacitance. Holes are classical until phase 2. Material constants are 300 K literature values (Vurgaftman et al. 2001 and others cited in the page).
