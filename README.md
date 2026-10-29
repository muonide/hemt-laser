# HEMT & Laser Bench

Interactive, self-consistent band diagrams and device characteristics for high-electron-mobility transistors and heterostructure lasers, built around exemplars from commercial products and current research. Single self-contained `index.html` (300 K). Spun off from [junction-bench](https://github.com/muonide/junction-bench) and sharing its Schrödinger–Poisson and drift–diffusion solver.

Live: https://muonide.github.io/hemt-laser/ (append `#hemt` or `#laser` to open a tab).

## Status

**HEMT tab (phases 1–2).** Self-consistent Schrödinger–Poisson cross-section under the gate, with quantized electron *and* heavy-hole subbands; n_s (or p_s) and gate C–V versus V_G; and a deliberately simple transistor model (charge control from the solved sheet density, velocity saturation, access resistance, parasitic capacitance) giving transfer and output curves, g_m and f_T for n- and p-channel devices. Gate dielectrics (SiN, Al₂O₃) and p-GaN gates are supported. Twelve exemplars:

- n-channel: GaAs pHEMT, metamorphic HEMT on GaAs, InP HEMT, AlGaN/GaN on SiC, p-GaN-gate normally-off GaN-on-Si, InAlN/GaN, ScAlN/GaN, N-polar GaN deep-recess, β-(AlGa)₂O₃/Ga₂O₃ MODFET
- p-channel: GaN/AlN polarization 2DHG, strained Ge/SiGe hole quantum well, H-terminated diamond (surface-transfer-doped 2DHG)

Basic mode (introductory notes) and Advanced mode (graduate notes, full layer editing).

**Laser tab (phase 3).** Edge-emitting laser cross-section under forward bias: self-consistent electron and heavy-hole subbands with light holes and biaxial strain, TE/TM modal gain spectra from the subband pairs, the fundamental slab mode and confinement factor, a background injection sweep (peak gain versus recombination current, including the confinement layers), threshold and the above-threshold light–current curve. Cavity length, facet reflectivities, stripe width, internal loss, injection efficiency and line broadening are adjustable. Exemplars: 976 nm InGaAs/AlGaAs pump laser, 1550 nm InGaAs/InGaAsP MQW telecom laser, 450 nm InGaN/GaN blue laser diode.

## Roadmap

| Phase | Content |
|---|---|
| 2 ✓ | Self-consistent hole subbands; gate dielectrics and p-GaN gates; nine more HEMT exemplars (listed above) |
| 3 ✓ | Laser physics: gain spectrum with strain, 1D waveguide mode and confinement factor, threshold and L–I. Exemplars: 976 nm InGaAs/AlGaAs, 1550 nm InP MQW, 450 nm InGaN |
| 4 | 1310 nm AlGaInAs, 650 nm AlGaInP red, InGaN green, interband cascade (GaSb), AlGaN UV-C laser diode |
| 5 | Model sections, UX pass, publish |

**Deferred (noted, not scheduled):** vertical-cavity surface-emitting lasers (need a DBR/cavity solver) and quantum cascade lasers (need intersubband transitions and injector alignment under bias). Quantum-dot lasers on Si are out of scope for a 1D solver.

## Model limits

The transistor model has no short-channel effects, self-heating, trapping or gate leakage; f_T is an intrinsic estimate with a lumped parasitic capacitance. Holes use one in-plane mass per band (no k·p band mixing); the L–I curve has no heating or current spreading. ScAlN, (AlGa)₂O₃ and H-diamond parameters are less settled than the III–V and AlGaN values. Material constants are 300 K literature values (Vurgaftman et al. 2001 and others cited in the page).
