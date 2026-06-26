---
title: CWE — Coherent Wake Emission
created: 2026-06-25
updated: 2026-06-25
type: concept
tags: [hhg, cwe, sub-relativistic, plasma-gradient, attosecond]
sources:
  - path: /home/zhiping/knowledge_base/paper/2006/2006--Coherent-Wake-Emission-of-High-Order-Harmonics-from-Overdense-Plasmas/paper.md
    doi: 10.1103/PhysRevLett.96.125004
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2010/2010--High-order-harmonic-and-attosecond-pulse-generation-on-plasma-mirrors/paper.md
    doi: 10.1088/0953-4075/43/21/213001
    read: true
    sections: [all]
confidence: high
---

# CWE — Coherent Wake Emission

## Physical Picture

Coherent Wake Emission (CWE) is the dominant HHG mechanism for **sub-relativistic** laser intensities (a₀ < 1, Iλ² < 10¹⁸ W/cm² μm²) interacting with steep plasma density gradients (L < λ/20).

### Step-by-step mechanism:

1. **Electron extraction**: During p-polarized oblique incidence, the laser electric field component along the target normal pulls electrons out of the plasma surface

2. **Ballistic acceleration**: Extracted electrons are accelerated by the laser field back into the plasma

3. **Excitation of plasma oscillations**: These fast electron bunches travel through the plasma density gradient, exciting collective plasma oscillations (Langmuir waves) at the local plasma frequency

4. **Coherent emission**: The plasma oscillations coherently radiate electromagnetic fields, producing harmonics up to the plasma frequency

— Thaury & Quéré, J. Phys. B 43, 213001 (2010), §2
  "CWE starts occurring at moderately high intensities (I ≃ 10¹⁶ W/cm²) and is triggered by laser-driven electron bunches that excite collective electronic plasma oscillations in the density gradient between vacuum and the plasma bulk."

**Original CWE paper**:
- F. Quéré, C. Thaury, P. Monot, S. Dobosz, Ph. Martin, J. P. Geindre, and P. Audebert, Phys. Rev. Lett. 96, 125004 (2006)

## Key Characteristics

| Property | CWE | ROM/CSE |
|----------|-----|---------|
| Intensity regime | a₀ < 1 (sub-relativistic) | a₀ > 1 (relativistic) |
| Gradient requirement | Steep (L < λ/20) | Moderate (L ~ 0.1λ optimal) |
| Spectral cutoff | ω_p (plasma frequency) | γ³ (Lorentz factor) |
| Scaling | Discrete harmonics | Power-law continuum |
| Phase | Different from ROM | — |
| CEP sensitivity | Yes (few-cycle) | Weak (multi-cycle) |

## CWE vs ROM: Distinct Mechanisms

### CWE (sub-relativistic)
- Driven by **resonance absorption** and **Brunel heating**
- Requires p-polarization and oblique incidence
- Harmonics up to ω_p only
- Phase properties different from ROM

### ROM (relativistic)
- Driven by **ponderomotive force** on the electron surface
- Works at any polarization (p more efficient)
- Harmonics up to γ³ ω_L
- Phase-locked attosecond pulses

— Thaury & Quéré, J. Phys. B 43, 213001 (2010), §1
  "Two main harmonic generation processes on PM have been identified in the literature... CWE starts occurring at moderately high intensities... The second mechanism, called 'relativistic oscillating mirror' (ROM), occurs at even higher intensities."

**Key experimental paper demonstrating CWE**:
- F. Quéré, C. Thaury, P. Monot, S. Dobosz, Ph. Martin, J. P. Geindre, and P. Audebert, Phys. Rev. Lett. 96, 125004 (2006)

## CWE as Gradient Diagnostic

CWE harmonics can serve as a **diagnostic** of the plasma density gradient:
- Harmonic spectrum shape encodes the density profile
- Used to measure L in real-time during experiments

**Original paper on CWE diagnostics**:
- A. Malvache, A. Borot, F. Quéré, and R. Lopez-Martens, Phys. Rev. E 87, 035101 (2013)

## Historical Context

### 2006: Discovery
Quéré et al. first proposed and demonstrated CWE:
- 50 fs, 1 TW laser at 45° oblique incidence
- Observed harmonics 16-18 from solid target
- Identified as distinct from ROM

**Original paper**:
- F. Quéré, C. Thaury, P. Monot, S. Dobosz, Ph. Martin, J. P. Geindre, and P. Audebert, Phys. Rev. Lett. 96, 125004 (2006)

### 2007: Systematic confirmation
Thaury et al. provided systematic experimental evidence:
- Clear separation of CWE and ROM regimes
- Identified the role of plasma gradient

**Original paper**:
- C. Thaury, F. Quéré, J.-P. Geindre, G. Bonnaud, P. Monot, and P. Martin, Nat. Phys. 3, 424–429 (2007)

## Relevance to Attosecond Source Development

CWE harmonics have **different phase properties** than ROM harmonics, which affects:
- Attosecond pulse formation (different timing)
- Coherence properties
- Pulse isolation

For attosecond source development, CWE is generally **avoided** by using:
- High-contrast pulses (to maintain steep gradient)
- Relativistic intensities (a₀ > 1)
- Short pulse durations (to prevent gradient expansion)

However, CWE remains important as:
- A **diagnostic tool** for gradient characterization
- A **benchmark** for distinguishing HHG mechanisms
- The dominant mechanism in some experimental conditions

## Coherent Focusing of CWE Harmonics

Gordienko et al. (2005) proposed that CWE harmonics can be coherently focused using a curved (spherical) plasma surface to achieve extreme intensities. The key insight is that the CWE spectrum decays as |E_ω|² ∝ ω^{-p} with p = 5/2, which is slower than the 1/ω⁴ threshold needed for coherent intensity boosting.

### Mechanism
1. Reflect a few-fs laser pulse from a concave plasma surface
2. Harmonics generated via relativistic Doppler shift: ω_n = 4γ(t_n)² ω₀
3. Huygens principle in spherical geometry: focusing adds a factor ω in the focal field integral
4. All harmonics interfere constructively in the focal volume

### Scaling
- Focal intensity: I_CHF = μ₁(R₀Ω/λ)² a₀³ I₀
- Pulse duration: τ_CHF = 2πμ₂/(a₀²ω₀), reaching sub-attosecond (zeptosecond) range
- Schwinger limit reachable with I₀ ~ 10²² W/cm² incident laser

— doi: 10.1103/PhysRevLett.94.103903
  [KB: /home/zhiping/knowledge_base/paper/2005/2005--Coherent Focusing of High Harmonics_ A New Way Towards the Extreme Intensities]

## Links

- [[rom-theory]] — Relativistic mechanism, distinct from CWE
- [[cse-theory]] — Another relativistic mechanism
- [[preplasma-scale-length]] — Gradient determines CWE vs ROM
- [[scaling-laws]] — CWE has different scaling than ROM
- [[chf-mechanism]] — CWE harmonics can be coherently focused
