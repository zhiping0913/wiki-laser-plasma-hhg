---
title: CWE — Coherent Wake Emission
created: 2026-06-25
updated: 2026-06-25
type: concept
tags: [hhg, cwe, sub-relativistic, plasma-gradient, attosecond]
sources:
  - path: /home/zhiping/knowledge_base/paper/2006/2006--Coherent Wake Emission of High-Order Harmonics from Overdense Plasmas
    doi: 10.1103/PhysRevLett.96.125004
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2010/2010--High-order harmonic and attosecond pulse generation on plasma mirrors basic mechanisms
    doi: 10.1088/0953-4075/43/21/213001
    read: true
    sections: [1, 2]
  - path: /home/zhiping/knowledge_base/paper/2007/2007--Plasma mirrors for ultrahigh-intensity optics
    doi: 10.1038/nphys595
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2013/2013--Coherent wake emission spectroscopy as a probe of steep plasma density profiles
    doi: 10.1103/PhysRevE.87.035101
    read: true
    sections: [all]
---

# CWE — Coherent Wake Emission

## Physical Picture

Coherent Wake Emission (CWE) is the dominant HHG mechanism for **sub-relativistic** laser intensities (a₀ < 1, Iλ² < 10¹⁸ W/cm² μm²) interacting with steep plasma density gradients (L < λ/20).

### Step-by-step mechanism:

1. **Electron extraction**: During p-polarized oblique incidence, the laser electric field component along the target normal pulls electrons out of the plasma surface

2. **Ballistic acceleration**: Extracted electrons are accelerated by the laser field back into the plasma

3. **Excitation of plasma oscillations**: These fast electron bunches travel through the plasma density gradient, exciting collective plasma oscillations (Langmuir waves) at the local plasma frequency

4. **Coherent emission**: The plasma oscillations coherently radiate electromagnetic fields, producing harmonics up to the plasma frequency

— Thaury & Quéré, J. Phys. B 43, 213001 (2010)
  [KB: /home/zhiping/knowledge_base/paper/2010/2010--High-order harmonic and attosecond pulse generation on plasma mirrors basic mechanisms]
  §2: "CWE starts occurring at moderately high intensities (I ≃ 10¹⁶ W/cm²) and is triggered by laser-driven electron bunches that excite collective electronic plasma oscillations in the density gradient between vacuum and the plasma bulk."

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

— Thaury & Quéré, J. Phys. B 43, 213001 (2010)
  [KB: /home/zhiping/knowledge_base/paper/2010/2010--High-order harmonic and attosecond pulse generation on plasma mirrors basic mechanisms]
  §1: "Two main harmonic generation processes on PM have been identified in the literature... CWE starts occurring at moderately high intensities... The second mechanism, called 'relativistic oscillating mirror' (ROM), occurs at even higher intensities."

## CWE as Gradient Diagnostic

CWE harmonics can serve as a **diagnostic** of the plasma density gradient:
- Harmonic spectrum shape encodes the density profile
- Used to measure L in real-time during experiments

— Malvache et al., Phys. Rev. E 87, 035101 (2013)
  [KB: /home/zhiping/knowledge_base/paper/2013/2013--Coherent wake emission spectroscopy as a probe of steep plasma density profiles]
  (Full paper read — CWE as gradient diagnostic)

## Historical Context

### 2006: Discovery

Quéré et al. first proposed and demonstrated CWE:
- 50 fs, 1 TW laser at 45° oblique incidence
- Observed harmonics 16-18 from solid target
- Identified as distinct from ROM

— Quéré et al., Phys. Rev. Lett. 96, 125004 (2006)
  [KB: /home/zhiping/knowledge_base/paper/2006/2006--Coherent Wake Emission of High-Order Harmonics from Overdense Plasmas]
  (Full paper read — CWE discovery paper)

### 2007: Systematic confirmation

Thaury et al. provided systematic experimental evidence:
- Clear separation of CWE and ROM regimes
- Identified the role of plasma gradient

— Thaury et al., Nat. Phys. 3, 424–429 (2007)
  [KB: /home/zhiping/knowledge_base/paper/2007/2007--Plasma mirrors for ultrahigh-intensity optics]
  (Full paper read — systematic CWE/ROM separation)

## Relevance to Attosecond Source Development

CWE harmonics have **different phase properties** than ROM harmonics, which affects:
- Attosecond pulse formation (different timing)
- Coherence properties
- Pulse isolation

For attosecond source development, CWE is generally **avoided** by using:
- High-contrast pulses (to maintain steep gradient)
- Relativistic intensities (a₀ > 1)
- Short pulse durations (to prevent gradient expansion)

## Links

- [[rom-theory]] — Relativistic mechanism, distinct from CWE
- [[cse-theory]] — Another relativistic mechanism
- [[preplasma-scale-length]] — Gradient determines CWE vs ROM
- [[scaling-laws]] — CWE has different scaling than ROM
