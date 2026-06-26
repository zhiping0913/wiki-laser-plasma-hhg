---
title: Double-Foil Target — Enhanced CSE in Transmission
created: 2026-06-25
updated: 2026-06-25
type: concept
tags: [cse, attosecond, double-foil, nanobunch, pic-simulation]
sources:
  - path: /home/zhiping/knowledge_base/paper/2018/2018--Coherent synchrotron emission in transmission with double foil target/paper.md
    doi: 10.1088/1361-6587/aaa57d
    read: true
    sections: [1-5]
confidence: high
---

# Double-Foil Target

## Overview

The double-foil target (DFT) scheme enables efficient coherent synchrotron emission (CSE) in the **transmitted direction**, producing intense single attosecond pulses. Unlike conventional single-foil targets where CSE is weak in transmission, the DFT configuration creates an optimal environment for nanobunch formation and radiation.

## Physical Mechanism

### Key differences from single-foil target (SFT):

1. **Extended acceleration length**: The vacuum gap between foils allows electrons blown out from the first foil to be accelerated over a longer distance

2. **Dense nanobunch formation**: Electrons undergo self-compression in the vacuum gap, forming a δ-like density distribution with high γ_x

3. **Enhanced laser penetration**: More laser energy penetrates through the nanobunch, reflects from the second foil, and interacts with the nanobunch

4. **Single pulse generation**: After the main attosecond pulse, the nanobunch disperses when it hits the second foil, terminating CSE

— Xu et al., PPCF 60, 045005 (2018) [KB: .../paper.md, section 2]
  "the dense electron nanobunch is formed by the electrons blown out from the first ultrathin foil, which is accelerated more efficiently through the vacuum gap between two foils"

## Optimal Conditions

### First foil requirements:
- **Thickness**: d₁ must satisfy optimal condition for blow-out
- **Optimal condition**: a₀ ≈ 2πn₁d₁/n_cλ
- When satisfied: nanobunch has maximum density and energy

### Vacuum gap:
- **Width**: 0.125λ ≤ D ≤ 0.25λ
- Too small: insufficient acceleration length
- Too large: nanobunch disperses or is pulled back

### Second foil:
- **Density**: High enough for specular reflection
- **Thickness**: Thick enough to survive the interaction
- **Role**: Reflects penetrated laser, shields nanobunch after emission

— Xu et al. (2018) [KB: .../paper.md, section 2]
  "the gap width to be < 0.25λ, which approximately corresponds to the time duration when the laser Lorentz force is greater than the nearly constant E_s"

## Simulation Results (1D PIC)

### Nanobunch properties (at I = 7.7 × 10²¹ W/cm²):
- Maximum density: > 4000 n_c
- Thickness: 0.24 nm (FWHM)
- Peak γ_x ≈ 9

### Attosecond pulse:
- Duration: **18 as**
- Photon energy: > 0.16 keV (ω > 100ω₀)
- Peak intensity: **1.7 × 10²⁰ W/cm²**
- Direction: Transmitted

### Cutoff frequency:
- Exceeds 2000ω₀ (much higher than SFT case)
- Enables keV photon energies

— Xu et al. (2018) [KB: .../paper.md, section 3]
  "a single attosecond pulse with duration of 18 as, photon energy > 0.16 keV and peak intensity of 1.7 × 10²⁰ W/cm²"

## Robustness

### Laser amplitude:
- Single attosecond pulses obtained for a₀ = 20-100
- Intensity increases with a₀ when optimal condition satisfied

### First foil thickness:
- Broad range tolerable around optimal value
- Single pulses still generated with some deviation

### Gap width:
- Works for 0.125λ ≤ D ≤ 0.25λ
- Outside this range: nanobunch disperses or insufficient interaction

### Laser duration:
- Works with longer pulses (τ = 6.0T₀ tested)
- Pre-expansion (preplasma) also compatible

### 2D effects:
- 2D PIC simulations confirm single attosecond pulse generation
- Duration increases to 44 as (due to transverse effects)
- Still much more intense than SFT case

— Xu et al. (2018) [KB: .../paper.md, section 4]
  "intense single attosecond pulses can be efficiently generated through a wide range of parameters"

## Advantages over Single-Foil Target

| Property | SFT | DFT |
|----------|-----|-----|
| CSE in transmission | Weak | Strong |
| Nanobunch energy | Limited (γ_x ~ few) | High (γ_x ~ 9) |
| Cutoff frequency | ~100-200ω₀ | >2000ω₀ |
| Attosecond pulse intensity | Low | 10²⁰ W/cm² |
| Single pulse isolation | Difficult | Natural (nanobunch disperses) |

## Experimental Challenges

1. **Small gap width**: 0.125-0.25λ is challenging to control
2. **High contrast laser**: Required to avoid pre-heating first foil
3. **Target fabrication**: Nanometer-scale foils with precise spacing
4. **Alignment**: Both foils must be properly aligned

— Xu et al. (2018) [KB: .../paper.md, section 5]
  "the small distance required between two foils in the DFT case is still challenging for many laboratories"

## Related Work

### Relativistic electron mirrors (Kiefer et al. 2013):
- Nanoscale foils create relativistic electron mirrors
- Coherent backscattering demonstrated
- Frequency upshift from 800 nm to ~60 nm
- Efficiency > 10⁴ times higher than incoherent scattering

— Kiefer et al., Nat. Commun. 4, 1763 (2013) [KB: .../paper.md, abstract]
  "dense relativistic electron mirrors can be created from the interaction of a high-intensity laser pulse with a freestanding, nanometre-scale thin foil"

## Links

- [[cse-theory]] — CSE mechanism in detail
- [[scaling-laws]] — Bunch-width limits cutoff
- [[waveform-engineering]] — Optimal driving waveform
- [[efficiency-optimization]] — How to maximize conversion
- [[attosecond-lighthouse]] — Isolation techniques
