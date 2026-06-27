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
  - path: /home/zhiping/knowledge_base/paper/2009/2009--Diffraction-limited performance and focusing of high harmonics from relativistic plasmas/paper.md
    doi: 10.1038/nphys1158
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2010/2010--Geometrical optimization of an ellipsoidal plasma mirror toward tight focusing of ultra-intense laser pulse/paper.md
    doi: 10.1088/1742-6596/244/3/032008
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2023/2023--Plasma mirrors as a path to the Schwinger limit theoretical and numerical developments/paper.md
    doi: 10.1140/epjs/s11734-023-00909-2
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
- **Diffraction-limited harmonic emission** (Dromey 2009)
- **Surface smoothing mechanism** (Dromey 2009)
- **Ellipsoidal PM focusing** (Nakatsutsumi 2010)

### Not yet demonstrated
- Focused harmonic intensity approaching Schwinger limit
- Full wavefront characterization of high harmonics
- Systematic CHF experiments

### Key Experimental Results

#### Diffraction-Limited Harmonic Emission (Dromey 2009)

Dromey et al. (2009) provided the **first quantitative evidence** that harmonics from relativistically oscillating plasma surfaces can achieve diffraction-limited performance. This is crucial for CHF because it confirms that the coherence properties of the driving laser are preserved in the emitted harmonics.

**Key findings**:
- ROM harmonics emitted into a narrow on-axis cone (~diffraction limit)
- CWE harmonics scattered into large angles (off-axis)
- Clear spatial separation between ROM and CWE mechanisms
- Harmonics insensitive to initial surface roughness (φ_r.m.s. up to ~λ_n)

**Surface smoothing mechanism**:
- Electron trajectories extend many times the original surface roughness
- Transverse and longitudinal motion averages over small-scale roughness
- Plasma expansion phase (~100 fs) enables additional smoothing
- Result: smooth relativistic mirror surface even for rough initial targets

**Surface denting effects**:
- Ponderomotive pressure pushes plasma surface inward
- Creates curved wavefront → harmonics pass through intermediate focus
- Dent depth ~35 nm (Astra) to ~300 nm (Vulcan)
- All harmonic orders exhibit constant divergence (curved wavefront signature)

**Intrinsic phase effects**:
- Harmonic phase depends on target density: φ_n ∝ (1 - N/N_crit)^(1/2)
- Intensity-dependent phase from ponderomotive pressure
- Can be controlled by tailoring laser intensity distribution

— doi: 10.1038/nphys1158
  [KB: /home/zhiping/knowledge_base/paper/2009/2009--Diffraction-limited performance and focusing of high harmonics from relativistic plasmas/paper.md]
  Abstract: "the occurrence of surface smoothing on the scale of the wavelength of the generated harmonics, and plasma denting of the irradiated surface, enables the production of high-quality X-ray beams focused down to the diffraction limit"

#### Ellipsoidal Plasma Mirror Focusing (Nakatsutsumi 2010)

Nakatsutsumi et al. (2010) developed **compact ellipsoidal plasma mirror systems** for tight focusing of ultra-intense laser pulses, demonstrating a practical approach to achieve the high intensities needed for CHF.

**Key results**:
- Extremely low f-number: f/# = 0.4 (compared to standard f/2.7)
- Spot size reduction: 1/5 of standard focusing
- Compact design: <1 cm³ volume
- Plasma mirror regime: debris protection + contrast enhancement

**Technical details**:
- Confocal ellipsoid geometry
- Plasma surface created by prepulse
- Main pulse reflected from curved plasma surface
- Achieves significant intensity enhancement without modifying laser system

**Relevance to CHF**:
- Demonstrates feasibility of curved plasma optics for focusing
- Shows that plasma mirrors can be used as compact, high-quality focusing elements
- Provides a practical route to achieve the tight focusing needed for CHF
- Combined with harmonic generation, could enable extreme intensity focusing

— doi: 10.1088/1742-6596/244/3/032008
  [KB: /home/zhiping/knowledge_base/paper/2010/2010--Geometrical optimization of an ellipsoidal plasma mirror toward tight focusing of ultra-intense laser pulse/paper.md]
  Abstract: "very compact (<1 cm³) extremely low f-number (f/# = 0.4) confocal ellipsoid focusing systems... 1/5 reduction of the spot size compared to standard focusing"

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

### CRM Review and Numerical Methods (Vincenti 2023)

Vincenti et al. (2023) provided a comprehensive review of the CRM paradigm and the pseudo-spectral PIC codes required for accurate 3D simulations.

**CRM Paradigm**:
- Two intensification mechanisms: (i) temporal compression by relativistic Doppler effect, (ii) tight focusing of Doppler-upshifted light
- Single laser beam both creates the mirror AND reflects off it (no two-beam collision needed)
- Surface naturally curved by radiation pressure (plasma denting) — a realistic CRM implementation

**Pseudo-Spectral PIC Codes**:
- Standard FDTD suffers from numerical dispersion, artificial vacuum index, nonphysical refraction of Doppler harmonics
- PSATD (Pseudo-Spectral Analytical Time Domain): analytically solves Maxwell's equations in Fourier space — eliminates BOTH spatial AND temporal numerical dispersion
- PICSAR library: developed at CEA + LBNL for exascale; "local" FFT method avoids all-to-all communications, scales to 100k+ cores

**Path to Schwinger**:
- QED critical field: E_S ~ 1.3 × 10¹⁶ V/cm, I_S ~ 4.6 × 10²⁹ W/cm²
- Current PW lasers reach ~5.5 × 10²² W/cm² (record); CRM can bridge the gap
- 3D simulations with WarpX + PICSAR demonstrated CRM as realistic implementation
- Exascale computing required for most challenging simulations

— doi: 10.1140/epjs/s11734-023-00909-2
  [KB: /home/zhiping/knowledge_base/paper/2023/2023--Plasma mirrors as a path to the Schwinger limit theoretical and numerical developments]

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
