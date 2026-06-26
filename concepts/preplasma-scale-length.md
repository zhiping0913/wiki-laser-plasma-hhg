---
title: Preplasma Scale Length — Effects on HHG
created: 2026-06-25
updated: 2026-06-25
type: concept
tags: [hhg, preplasma, gradient, optimization, rom, cwe, pic-simulation]
sources:
  - path: /home/zhiping/knowledge_base/thesis/2019/2019--Ultrafast Sources of Intense Radiation/thesis.md
    doi: null (PhD thesis, Princeton 2019)
    read: true
    sections: [4.1.4]
  - path: /home/zhiping/knowledge_base/thesis/2019/2019--Ultrafast Sources of Intense Radiation/thesis.md
    doi: null (PhD thesis, Princeton 2019)
    read: true
    sections: [5.1.1]
  - path: /home/zhiping/knowledge_base/other/2024--陈自宇--Laser Plasma Notes for Beginners High Harmonic Generation/paper.md
    doi: null (tutorial note)
    read: true
    sections: [0.4.3]
confidence: high
---

# Preplasma Scale Length

## Overview

The plasma density gradient (preplasma) at the target surface is one of the most critical parameters for HHG. It determines:
- Which mechanism dominates (CWE vs ROM)
- The efficiency of harmonic generation
- The quality of attosecond pulses
- The optimal driving waveform

## Definition

The preplasma scale length L characterizes how the electron density varies near the target surface:

### Exponential gradient
**n_e(x) = n_max · exp(x/L_e)**

where L_e is the exponential scale length.

### Linear gradient
**n_e(x) = n_max · (x/L_l)**

where L_l is the linear scale length.

Both are typically normalized to the laser wavelength: L/λ.

## Physical Origin

Preplasma is created by:
1. **Prepulse** (ASE, prepulses): Ionizes and expands the target before the main pulse arrives
2. **Rising edge of main pulse**: The leading edge of an intense pulse creates plasma
3. **Target preparation**: Some experiments intentionally create gradients

The scale length depends on:
- Laser contrast (prepulse intensity)
- Pulse duration (longer pulses → more expansion)
- Target material (ion mass, ionization state)
- Delay between prepulse and main pulse

## Effects on HHG Mechanisms

### CWE regime (a₀ < 1)
- **Requires steep gradient**: L < λ/20
- Longer gradients suppress CWE
- CWE harmonics disappear for L > λ/10

### ROM regime (a₀ > 1)
- **Requires moderate gradient**: L ~ 0.05-0.15λ optimal
- Too steep (L → 0): Reduced efficiency
- Too long (L > 0.2λ): Efficiency drops, complex dynamics

— Edwards Thesis §4.1.4 [KB: .../thesis.md, line 1679]
  "A substantial increase in efficiency occurs as L_e/λ is increased from 0 to 0.1"

— 张玉雪 Thesis §1.4.6 [KB: .../thesis.md, line 799]
  "BGP模型有一定的局限性...在斜入射情况下,有时反射光场出现一定地被压缩现象"

## Edwards' Results on Gradient Effects

### Efficiency enhancement
For a₀ = 5-30 at θ_L = 30°:
- L/λ = 0: Baseline efficiency
- L/λ = 0.05: ~3× enhancement
- L/λ = 0.1: ~10× enhancement (near optimal)
- L/λ = 0.15: Complex behavior, depends on a₀

The optimal gradient length depends on a₀, which explains variance in reported optimal values.

— Edwards Thesis §4.1.4 [KB: .../thesis.md, line 1685]
  "the most efficient scale length observed will depend on the choice of a₀"

### Physics of enhancement
The gradient provides lower effective density:
- Laser interacts near critical density, not at maximum density
- The ponderomotive force (∝ v × B) balances the restoring force (∝ ∫N(x)dx)
- At optimal gradient: density matches the laser intensity for best HHG

### Weakened a₀-dependence
With a gradient:
- The a₀-dependence of efficiency weakens substantially
- At L/λ = 0.1: efficiency has almost no a₀-dependence
- This is because the laser finds its own optimal density in the gradient

### Implications for isolated attosecond pulses
The weakened nonlinearity makes isolation more difficult:
- Gas HHG relies on strong a₀-dependence for isolation
- With gradient, the attosecond pulse train envelope follows the laser envelope
- Shorter allowable pulse width for isolation

— Edwards Thesis §4.1.5 [KB: .../thesis.md, line 1736]
  "the presence of a finite gradient makes the creation of isolated attosecond pulses more difficult"

## Effects on Two-Color Enhancement

The two-color enhancement persists with gradients:
- At L/λ = 0.05: 10× enhancement with 5-10% SH
- At L/λ = 0.15: Similar enhancement
- Combined effect: gradient + two-color = substantial improvement

— Edwards Thesis §5.1.1 [KB: .../thesis.md, line 2153]
  "tenfold enhancement is seen for gradients of L/λ = 0.05 and 0.15"

## Effects on Secondary Attosecond Pulses

The gradient affects secondary pulse dynamics:
- Gradient changes the plasma density profile
- Secondary pulse formation depends on local ω_p
- More complex than for step-like profiles

## Experimental Considerations

### Measuring L
- **CWE spectroscopy**: Harmonic spectrum shape encodes gradient
- **Interferometry**: Measures plasma expansion in real-time
- **Reflectivity**: Changes with gradient length

### Controlling L
- **Laser contrast**: Higher contrast → steeper gradient
- **Plasma mirror**: First plasma mirror improves contrast for second
- **Target choice**: Different materials expand differently
- **Pulse duration**: Shorter pulses → less expansion

### Typical values
- Best experiments: L/λ ~ 0.01-0.05
- PIC simulations (ideal): L/λ = 0-0.15
- Real experiments: L varies during pulse, ~0.05-0.2

## Scaling with Gradient

| L/λ | HHG Mechanism | Efficiency | Isolation |
|-----|---------------|------------|-----------|
| 0 | CWE (sub-rel), ROM (rel) | Low | Best |
| 0.01-0.05 | ROM dominant | Moderate | Good |
| 0.1 | ROM optimal | High | Moderate |
| 0.15-0.2 | ROM, complex | Variable | Poor |
| >0.2 | Weak HHG | Low | N/A |

## Connection to Similarity Theory

With a gradient, the interaction depends on:
- a₀ and the gradient scale length L (not N_max)
- The effective density is set by where the laser reflects
- Similarity parameter S is less relevant (gradient sets the scale)

— Edwards Thesis §4.1.4 [KB: .../thesis.md, line 1679]
  "the interaction should now depend almost entirely on a₀ and the length scale of the gradient"

## Links

- [[cwe-mechanism]] — CWE requires steep gradient
- [[rom-theory]] — ROM optimal at moderate gradient
- [[scaling-laws]] — Gradient modifies all scaling laws
- [[waveform-engineering]] — Two-color works with gradients
- [[secondary-attosecond-pulses]] — Gradient affects secondary pulses
- [[attosecond-pulse-characterization]] — Gradient affects pulse quality
