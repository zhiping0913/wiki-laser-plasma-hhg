---
title: CHF — Coherent Harmonic Focusing
created: 2026-06-25
updated: 2026-06-25
type: concept
tags: [hhg, chf, schwinger-limit, focusing, extreme-intensity]
sources:
  - path: /home/zhiping/knowledge_base/paper/2009/2009--Controlling the divergence of high harmonics from solid targets a route toward coherent harmonic focusing/paper.md
    doi: 10.1140/epjd/e2009-00084-x
    read: true
    sections: [abstract]
  - path: /home/zhiping/knowledge_base/paper/2021/2021--Reflecting petawatt lasers off relativistic plasma mirrors a realistic path to the Schwinger limit/paper.md
    doi: 10.1017/hpl.2020.46
    read: true
    sections: [1-4]
  - path: /home/zhiping/knowledge_base/paper/2005/2005--Coherent Focusing of High Harmonics_ A New Way Towards the Extreme Intensities
    doi: 10.1103/PhysRevLett.94.103903
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2019/2019--Achieving Extreme Light Intensities using Optically Curved Relativistic Plasma Mirrors
    doi: 10.1103/PhysRevLett.123.105001
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2014/2014--Optical properties of relativistic plasma mirrors
    doi: 10.1038/ncomms4403
    read: true
    sections: [all]
confidence: high
---

# CHF — Coherent Harmonic Focusing

## Overview

Coherent Harmonic Focusing (CHF) is a proposed scheme to focus high-order harmonics generated from solid-density plasma mirrors to **extreme intensities approaching the Schwinger limit** (~10²⁹ W/cm²). The key idea is that the exceptional coherence properties of the driving laser can be preserved in the emitted harmonic radiation, allowing diffraction-limited focusing.

## Physical Concept

### Basic principle
1. Generate high-order harmonics from a plasma mirror using a relativistic laser
2. The harmonics inherit the coherence of the driving laser
3. Focus the harmonic radiation using appropriate optics
4. The shorter wavelength allows tighter focusing than the fundamental

### Why harmonics can reach higher intensities
- Harmonic wavelength λ_n = λ_L/n (shorter → tighter diffraction limit)
- Coherent emission preserves spatial coherence
- Attosecond phase locking ensures temporal coherence
- Combined: diffraction-limited focusing to λ_n-scale spots

## Path to the Schwinger Limit

The Schwinger limit (E_S = m_e²c³/eℏ ≈ 1.3 × 10¹⁸ V/m, I_S ≈ 4.6 × 10²⁹ W/cm²) is the field strength where vacuum electron-positron pair production becomes significant.

### Requirements for CHF
- High conversion efficiency to harmonics (η ~ 10%)
- Good spatial coherence (diffraction-limited beam)
- Tight focusing to ~λ_n spot
- Sufficient pulse energy

### Estimated intensities
With current/pnear-future laser systems:
- 100 TW class laser → ~10 TW in harmonics
- Focus to ~λ/10 spot → I ~ 10²⁴-10²⁵ W/cm²
- With next-generation PW lasers: I ~ 10²⁶-10²⁸ W/cm²
- Ultimate limit: approaches Schwinger with sufficient energy

— doi: 10.1140/epjd/e2009-00084-x [KB: .../paper.md, abstract]
  "pave the way for unique experiments exploring the nonlinear properties of vacuum on ultra-fast timescales"

## Key Challenges

### 1. Wavefront control
The harmonic wavefronts must be precisely controlled for tight focusing:
- Plasma surface deformation affects wavefront quality
- Density gradients introduce aberrations
- Pre-shaped targets can correct wavefronts

— doi: 10.1140/epjd/e2009-00084-x [KB: .../paper.md, abstract]
  "precise control of the wavefronts and thus the focusability of the generated harmonics is possible with pre-shaped targets"

### 2. Conversion efficiency
Current HHG efficiencies are typically:
- CWE: ~10⁻⁶-10⁻⁴ per harmonic
- ROM: ~10⁻⁴-10⁻² per harmonic
- Optimized (Edwards): up to 63% total conversion

Higher efficiency → more harmonic energy → higher focused intensity

### 3. Spectral selection
To focus a single harmonic (or attosecond pulse):
- Must select desired spectral range
- Reject fundamental and other harmonics
- Use multilayer mirrors or gratings

### 4. Phase control
For coherent addition at focus:
- All harmonics must have well-defined phase
- CEP stability of driving laser required
- Attosecond phase locking must be preserved

## Experimental Status

### Demonstrated
- High harmonic generation from plasma mirrors (up to keV)
- Good spatial coherence for low harmonics
- Attosecond phase locking

### Not yet demonstrated
- Focused harmonic intensity approaching Schwinger limit
- Full wavefront characterization of high harmonics
- Systematic CHF experiments

## Theoretical Framework

### From Gordienko-Pukhov (2004)
The original proposal for using relativistic HHG to reach extreme intensities:

— doi: 10.1103/PhysRevLett.93.115002
  [KB: /home/zhiping/knowledge_base/paper/2004/2004--Relativistic Doppler Effect_ Universal Spectra and Zeptosecond Pulses]

### Coherent Focusing of Harmonics (Gordienko 2005)

Gordienko et al. (2005) proposed that CWE harmonics can be coherently focused using a concave plasma surface to achieve extreme intensities. The key mechanism:

1. Reflect a few-fs laser pulse from a spherical plasma surface
2. Harmonics generated via relativistic Doppler shift: ω_n = 4γ(t_n)²ω₀
3. Huygens principle in spherical geometry adds a factor ω in the focal field integral
4. All harmonics interfere constructively → intensity boosting

**Scaling**:
- Focal intensity: I_CHF = μ₁(R₀Ω/λ)² a₀³ I₀
- Pulse duration: τ_CHF = 2πμ₂/(a₀²ω₀), reaching sub-attosecond (zeptosecond) range
- Schwinger limit reachable with I₀ ~ 10²² W/cm²

— doi: 10.1103/PhysRevLett.94.103903
  [KB: /home/zhiping/knowledge_base/paper/2005/2005--Coherent Focusing of High Harmonics_ A New Way Towards the Extreme Intensities]
  Abstract: "a new way towards the extreme intensities... the spectrum must decay slower than 1/ω⁴"

### Curved Relativistic Plasma Mirror (Vincenti 2019)

Vincenti (2019) proposed a realistic all-optical scheme based on plasma mirrors optically curved by radiation pressure, demonstrating that intensities above 10²⁵ W/cm² are achievable with 3 PW lasers.

**Key results**:
- PM denting creates parabolic mirror: δ(s) = 2L·cos²θ·ln(a(s))
- Focal length: f_p = w_L²/(2δ_p)
- Intensity gain Γ ~ 10³: ~5× from Doppler compression + ~200× from spatial focusing
- ~100 as pulses, ~1.5 J energy, spot ~0.4λ
- Only ~30 harmonic orders needed (highly robust)

— doi: 10.1103/PhysRevLett.123.105001
  [KB: /home/zhiping/knowledge_base/paper/2019/2019--Achieving Extreme Light Intensities using Optically Curved Relativistic Plasma Mirrors]
  Abstract: "intensities above 10²⁵ W/cm² could be reached with a 3 PetaWatt (PW) laser"

### PM Curvature Effects (Vincenti 2014)

Vincenti et al. (2014) showed that PM curvature from the preplasma gradient affects CHF by increasing harmonic divergence. The focusing parameter Ψ_n ∝ n·δ_T/λ_L scales linearly with harmonic order, increasing divergence by up to 3× for optimal L ~ 0.05-0.1λ. This can be compensated by defocusing the driving laser.

— doi: 10.1038/ncomms4403
  [KB: /home/zhiping/knowledge_base/paper/2014/2014--Optical properties of relativistic plasma mirrors]

### From Quéré-Vincenti (2021)
The review "Reflecting petawatt lasers off relativistic plasma mirrors: a realistic path to the Schwinger limit" provides the modern perspective on CHF:

Key points from the paper:
- **Schwinger limit**: I_S = 4.7 × 10²⁹ W/cm² (E_S = 1.32 × 10¹⁸ V/m)
- **Current record**: 5.5 × 10²² W/cm² (7 orders of magnitude below Schwinger)
- **CHF mechanism**: Curved relativistic plasma mirrors (p-CRM) simultaneously:
  1. Down-convert wavelength by factor α ≈ 1/4γ²
  2. Compress pulse in time by same factor
  3. Imprint wavefront curvature for focusing
- **Intensity gain**: Scales as 1/α³ ∝ γ⁶
- **Practical path**: Use petawatt-class lasers + relativistic plasma mirrors
- **Challenge**: Generate sufficiently curved plasma surfaces with γ ≈ 10

— Quéré and Vincenti, High Power Laser Sci. Eng. 9, e6 (2021) [KB: .../paper.md, sections 1-4]
  "approaching the Schwinger limit in the coming years by applying this scheme to the latest generation of petawatt-class lasers is a challenging but realistic objective"

## Relevance to ULMI Lab Research

CHF represents the **ultimate application** of relativistic HHG:
- If we can optimize HHG efficiency (via waveform engineering, curved targets, etc.)
- And control the wavefronts (via target shaping)
- Then we can create the most intense attosecond pulses possible

This connects to:
- [[scaling-laws]] — Need efficient HHG for CHF
- [[waveform-engineering]] — Optimize driving waveform for efficiency
- [[cse-theory]] — CSE may provide better coherence than ROM
- [[preplasma-scale-length]] — Gradient affects wavefront quality

## Links

- [[rom-theory]] — ROM produces the harmonics for CHF
- [[scaling-laws]] — Efficiency determines CHF feasibility
- [[waveform-engineering]] — Optimization for CHF
- [[attosecond-pulse-characterization]] — Measuring CHF output
- [[preplasma-scale-length]] — Gradient effects on focusing
