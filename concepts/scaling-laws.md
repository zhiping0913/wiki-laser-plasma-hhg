---
title: HHG Scaling Laws — Power-Law Exponent and Cutoff
created: 2026-06-25
updated: 2026-06-25
type: concept
tags: [hhg, rom, cse, scaling, pic-simulation, theory]
sources:
  - path: /home/zhiping/knowledge_base/thesis/2019/2019--Ultrafast Sources of Intense Radiation/thesis.md
    doi: null (PhD thesis, Princeton 2019)
    read: true
    sections: [4.1, 4.2, 4.3]
  - path: /home/zhiping/knowledge_base/paper/2020/2020--Electron-Nanobunch-Width-Dominated Spectral Power Law for Relativistic Harmonic Generation from Ultrathin Foils
    doi: 10.1103/PhysRevLett.124.185004
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2016/2016--Waveform-Controlled Relativistic High-Order-Harmonic Generation
    doi: 10.1103/PhysRevLett.117.125001
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2013/2013--Scaling High-Order Harmonic Generation from Laser-Solid Interactions to Ultrahigh Intensity
    doi: 10.1103/PhysRevLett.110.175002
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2005/2005--Scalings for ultrarelativistic laser plasmas and quasimonoenergetic electrons
    doi: 10.1063/1.1884126
    read: true
    sections: [all]
confidence: high
---

# HHG Scaling Laws

## Overview

The reflected harmonic spectrum from relativistic laser-plasma HHG generally follows a power-law I(ω) ∝ ω^{-p} up to a cutoff frequency ω_c, beyond which intensity drops exponentially. The values of p and ω_c are central to predicting HHG source utility.

## Historical Predictions for p

| Model | Year | p value | Cutoff | Original Paper |
|-------|------|---------|--------|----------------|
| Gordienko OMM | 2004 | 5/2 (quasimonochromatic), 3 (broadband) | ∝ γ² | Gordienko et al., PRL 93, 115002 (2004) |
| Baeva BGP | 2006 | **8/3** | √8α · γ³ | Baeva et al., PRE 74, 046404 (2006) |
| CSE model | 2010 | **4/3** | √8α · γ³ | an der Brügge & Pukhov, Phys. Plasmas 17, 033110 (2010) |
| Thin-foil (Edwards) | 2019 | **10/3** | bunch-width limited | Edwards et al., PRL 124, 185004 (2020) |

— Edwards Thesis §4.1 [KB: .../thesis.md, line 1609]
  "proposed ultimate values of p span a broad range, with strong implications for the usefulness of HHG-based x-ray sources"

**Key original papers**:
- S. Gordienko, A. Pukhov, O. Shorokhov, and T. Baeva, Phys. Rev. Lett. 93, 115002 (2004)
- T. Baeva, S. Gordienko, and A. Pukhov, Phys. Rev. E 74, 046404 (2006)
- D. an der Brügge and A. Pukhov, Phys. Plasmas 17, 033110 (2010)

## Edwards' Key Finding: p Is NOT Universal

Edwards' PIC simulations (EPOCH, BOPS) across a₀ = 1–1000 and N = 12–1000 show that **p is not a universal constant** but depends on a₀/N:

### Asymptotic limit (a₀ → ∞ at fixed S)
p approaches a constant that scales logarithmically with S:

**p ≈ 1.5 ln(a₀/N)** for a₀/√N > 2

### Range of p values
At fixed S, p can range from **>6 to <2**, depending on a₀/N.

### Transition at a₀/N ≈ 0.2
For a₀/N > 0.2, p exceeds the BGP prediction of 8/3. This regime corresponds to I_out > I_in, violating the oscillating mirror model assumptions.

— Edwards Thesis §4.1.3 [KB: .../thesis.md, line 1663]
  "for a₀ → ∞ at fixed S, p approaches a constant value"

— Edwards & Mikhailova, Phys. Rev. Lett. 117, 125001 (2016)
  [KB: /home/zhiping/knowledge_base/paper/2016/2016--Waveform-Controlled Relativistic High-Order-Harmonic Generation]
  (Full paper read — waveform-controlled HHG, optimal waveform at ω_pR)

## Bunch-Width Limited Cutoff

The CSE model predicts cutoff at ω_γ = √8α · γ³, but Edwards shows the **actual cutoff is much lower**, limited by the electron bunch width Δ:

**ω_b = λ/(2Δ)**

Above ω_b, the spectrum gains an additional ω^{-2} factor from incoherent summation:

**I(ω) ∝ ω^{-4/3} · ω^{-2} = ω^{-10/3}** for ω > ω_b

— Edwards Thesis §4.3.4 [KB: .../thesis.md, line 1923]
  "The bunch width Δ therefore sets a frequency cutoff ω_b approximated as: ω_b/ω_L = λ/(2Δ)"

— Edwards et al., Phys. Rev. Lett. 124, 185004 (2020)
  [KB: /home/zhiping/knowledge_base/paper/2020/2020--Electron-Nanobunch-Width-Dominated Spectral Power Law for Relativistic Harmonic Generation from Ultrathin Foils]
  (Full paper read — bunch-width limited cutoff, thin-foil n^{-10/3})

## Thin-Foil Scaling: n^{-10/3}

For thin-foil targets (S·D < 0.2), individual electrons follow CSE trajectories with p = 4/3, but the finite bunch size adds ω^{-2}:

**I(ω) ∝ ω^{-10/3}** (p = 10/3 ≈ 3.3 ± 0.5)

The mechanism: the bunch has a sharp leading edge. Only electrons within λ/2 of the leading edge contribute coherently at frequency ω. The number of coherent electrons ∝ λ_n, so intensity ∝ λ_n² ∝ ω^{-2}.

— Edwards Thesis §4.2.2 [KB: .../thesis.md, line 1821]
  "the harmonic intensity varies as: I(ω) ∝ ω^{-10/3}"

— Edwards et al., Phys. Rev. Lett. 124, 185004 (2020)
  [KB: /home/zhiping/knowledge_base/paper/2020/2020--Electron-Nanobunch-Width-Dominated Spectral Power Law for Relativistic Harmonic Generation from Ultrathin Foils]
  (Full paper read — thin-foil scaling law)

## Efficiency Scaling with a₀/N

The attosecond pulse generation efficiency follows:

**I_a/I_L ∝ (a₀/N)^q**

with q₁ ≈ 9.2 for a₀/N < 0.2 (increasing efficiency) and q₂ ≈ -1.5 to -1.7 for a₀/N > 0.5 (decreasing efficiency due to relativistic transparency).

**Optimal efficiency at a₀/N ≈ 0.2–0.5**

— Edwards Thesis §4.1.1 [KB: .../thesis.md, line 1631]
  "a maximum pulse generation efficiency exists near a₀/N ≈ 0.2 − 0.5"

— Dollar et al., Phys. Rev. Lett. 110, 175002 (2013)
  [KB: /home/zhiping/knowledge_base/paper/2013/2013--Scaling High-Order Harmonic Generation from Laser-Solid Interactions to Ultrahigh Intensity]
  (Full paper read — scaling of HHG to ultrahigh intensity)

## Surface Displacement Scaling

From ponderomotive force vs. ion restoring force balance:

**x_disp ∝ a₀/N**

Confirmed by PIC simulations: x/λ = 0.31 · a₀/N at θ_L = 15°.

— Edwards Thesis §4.3.2 [KB: .../thesis.md, line 1882]
  "x_disp ∝ a₀/N"

## Lorentz Factor Scaling

**γ ∝ a₀** at fixed a₀/N (from similarity theory: γ = S^{α_γ} a₀ with α_γ ≈ 3)

— Gordienko & Pukhov, Phys. Plasmas 12, 043109 (2005)
  [KB: /home/zhiping/knowledge_base/paper/2005/2005--Scalings for ultrarelativistic laser plasmas and quasimonoenergetic electrons]
  (Full paper read — similarity theory)

## Preplasma Effects on Scaling

Finite plasma gradients modify the scaling substantially:
- For L_e/λ = 0 to 0.1: efficiency increases dramatically
- Optimal L_e/λ ≈ 0.1 (but depends on a₀)
- The a₀-dependence of efficiency weakens with gradient

— Edwards Thesis §4.1.4 [KB: .../thesis.md, line 1679]
  "A substantial increase in efficiency occurs as L_e/λ is increased from 0 to 0.1"

— Dollar et al., Phys. Rev. Lett. 110, 175002 (2013)
  [KB: /home/zhiping/knowledge_base/paper/2013/2013--Scaling High-Order Harmonic Generation from Laser-Solid Interactions to Ultrahigh Intensity]
  (Full paper read — preplasma optimization)

## Summary Table

| Quantity | Scaling | Conditions | Original Paper |
|----------|---------|------------|----------------|
| Power-law exponent p | 1.5 ln(a₀/N) | a₀/√N > 2, normal incidence | Edwards & Mikhailova, PRL 117, 125001 (2016) |
| Thin-foil p | 10/3 | S·D < 0.2 | Edwards et al., PRL 124, 185004 (2020) |
| Cutoff (bunch-width) | ω_b = λ/(2Δ) ∝ a₀ | General | Edwards et al., PRL 124, 185004 (2020) |
| Cutoff (Lorentz) | ω_γ = √8α · γ³ ∝ a₀³ | Single electron | Baeva et al., PRE 74, 046404 (2006) |
| Efficiency peak | a₀/N ≈ 0.2–0.5 | Steep gradient | Edwards & Mikhailova, PRL 117, 125001 (2016) |
| Surface displacement | x ∝ a₀/N | a₀ >> 1 | Gordienko & Pukhov, Phys. Plasmas 12, 043109 (2005) |
| Lorentz factor | γ ∝ a₀ | Fixed a₀/N | Gordienko & Pukhov, Phys. Plasmas 12, 043109 (2005) |

## Links

- [[rom-theory]] — BGP prediction of p = 8/3
- [[cse-theory]] — CSE prediction of p = 4/3
- [[unified-hhg-picture]] — Why both are synchrotron radiation
- [[waveform-engineering]] — How to improve scaling via two-color
- [[preplasma-scale-length]] — Gradient effects on scaling
