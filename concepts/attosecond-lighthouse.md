---
title: Attosecond Lighthouse — Isolated Pulse Generation
created: 2026-06-25
updated: 2026-06-25
type: concept
tags: [attosecond, lighthouse, wavefront-rotation, isolation, pic-simulation]
sources:
  - path: /home/zhiping/knowledge_base/paper/2020/2020--Techniques to generate intense isolated attosecond pulses from relativistic plasma mirrors/paper.md
    doi: 10.1103/PhysRevResearch.2.043007
    read: true
    sections: [I-III]
confidence: high
---

# Attosecond Lighthouse

## Overview

The attosecond lighthouse effect is a technique to generate **isolated attosecond pulses** by imprinting different propagation directions to successive attosecond pulses in the train, then spatially filtering one pulse in the far field. This enables isolated pulse generation without requiring few-cycle driving lasers.

## Basic Principle

### Wavefront Rotation (WFR)
- Apply controlled spatiotemporal coupling to the driving laser at focus
- Direction of incident laser light varies linearly in time along the femtosecond envelope
- Successive attosecond pulses are emitted in slightly different directions

### Spatial Filtering
- Place a slit in the far field to select one attosecond pulse
- Angular separation must be larger than harmonic beam divergence

### Separation Criterion
**Δθ = v_r ΔT ≥ θ_n**

where:
- v_r = WFR velocity of laser wavefronts
- ΔT = time delay between successive attosecond pulses (= T₀ for ROM)
- θ_n = harmonic beam divergence

**Maximum laser duration**: N_max ≈ θ₀/θ_n

— Kallala, Quéré, Vincenti, PRR 2, 043007 (2020) [KB: .../paper.md, section I]
  "consists in imprinting different propagation directions to successive attosecond pulses of the train, and then spatially filtering one pulse in the far field"

## Challenge in Relativistic Regime

### Plasma Mirror Denting
At relativistic intensities:
- Laser radiation pressure **curves the plasma mirror surface**
- Curved PM focuses the harmonic beam
- This **increases harmonic divergence** dramatically

### Quantitative Problem
For optimal HHG conditions (L ≈ λ₀/20 - λ₀/8):
- θ_L/θ_n ≈ 1
- N_max ≈ 1
- Would require single-cycle driving pulses!

This severely limits the attosecond lighthouse in the ROM regime.

— Kallala et al. (2020) [KB: .../paper.md, section II]
  "generating isolated attosecond pulses with the lighthouse effect in laser-plasma conditions that are optimal for Doppler harmonic generation is very challenging"

## Solution 1: Wavefront Curvature Compensation

### Principle
- Place PM **slightly away from laser best focus** (defocusing distance Δz > 0)
- Incident laser wavefronts are diverging at PM plane
- This **compensates** for the wavefront curvature induced by PM

### Optimal Defocusing
- Calculate optimal Δz that maximizes θ_L/θ_n
- Depends on laser-plasma parameters
- Achievable with current experimental know-how

### Validation
- 2D PIC simulations confirm effectiveness
- Harmonic divergence significantly reduced
- Lighthouse effect becomes viable for multi-cycle pulses

— Kallala et al. (2020) [KB: .../paper.md, section III]
  "placing the PM slightly away from the laser best focus, so that the incident laser wavefronts are curved and compensate for the wavefront curvature induced by the PM"

## Solution 2: Amplitude Profile Tailoring

### Principle
- Tailor the amplitude profile of the incident laser beam
- Can reduce harmonic beam divergence
- Combined with WFR for lighthouse effect

### Implementation
- Requires shaping of laser spatial profile
- Also achievable with current technology

## 3D PIC Validation

### Simulation Setup
- Code: warp+pxr (pseudo-spectral 3D PIC)
- PW-class laser parameters
- Realistic plasma conditions

### Results
- **Isolated attosecond pulses** demonstrated
- **10 TW peak power** in XUV range
- Validates both techniques

— Kallala et al. (2020) [KB: .../paper.md, section V]
  "isolated attosecond pulses with 10 TW peak power in the XUV range can be generated with PW-class lasers"

## Comparison with Other Isolation Techniques

| Technique | Driving Pulse | Harmonic Range | Status |
|-----------|---------------|----------------|--------|
| Intensity gating | Few-cycle | Limited | Demonstrated |
| Polarization gating | Few-cycle | Limited | Demonstrated |
| Attosecond lighthouse | Multi-cycle | Broad | Theoretical/partial |
| Wavefront curvature | Multi-cycle | Broad | Validated (PIC)
| Double-foil target | Multi-cycle | Broad | Theoretical |

## Advantages

1. **No few-cycle requirement**: Works with 6-15 cycle pulses
2. **Broad harmonic range**: Can select high harmonics
3. **PW-class compatible**: Designed for highest-power lasers
4. **Simple implementation**: Only requires phase/amplitude control

## Experimental Requirements

### For Wavefront Curvature:
- Controlled defocusing of laser on PM
- Phase control of driving laser
- WFR applied to beam

### For Amplitude Tailoring:
- Spatial shaping of laser beam
- Combined with WFR

## Connection to CHF

The attosecond lighthouse is important for CHF because:
- Isolated attosecond pulses needed for many applications
- Multi-cycle pulses available from PW lasers
- Combined with efficiency optimization → practical CHF source

## Links

- [[secondary-attosecond-pulses]] — Why isolation is challenging
- [[waveform-engineering]] — Alternative approach to enhancement
- [[efficiency-optimization]] — Combining efficiency with isolation
- [[chf-mechanism]] — Ultimate goal of isolated attosecond sources
- [[preplasma-scale-length]] — PM denting depends on gradient
