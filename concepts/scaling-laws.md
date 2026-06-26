     1|---
     2|title: HHG Scaling Laws — Power-Law Exponent and Cutoff
     3|created: 2026-06-25
     4|updated: 2026-06-25
     5|type: concept
     6|tags: [hhg, rom, cse, scaling, pic-simulation, theory]
     7|sources:
     8|  - path: /home/zhiping/knowledge_base/thesis/2019/2019--Ultrafast Sources of Intense Radiation/thesis.md
     9|    doi: null (PhD thesis, Princeton 2019)
    10|    read: true
    11|    sections: [4.1, 4.2, 4.3]
    12|  - path: /home/zhiping/knowledge_base/paper/2020/2020--Electron-Nanobunch-Width-Dominated Spectral Power Law for Relativistic Harmonic Generation from Ultrathin Foils
    13|    doi: 10.1103/PhysRevLett.124.185004
    14|    read: true
    15|    sections: [all]
    16|  - path: /home/zhiping/knowledge_base/paper/2016/2016--Waveform-Controlled Relativistic High-Order-Harmonic Generation
    17|    doi: 10.1103/PhysRevLett.117.125001
    18|    read: true
    19|    sections: [all]
    20|  - path: /home/zhiping/knowledge_base/paper/2013/2013--Scaling High-Order Harmonic Generation from Laser-Solid Interactions to Ultrahigh Intensity
    21|    doi: 10.1103/PhysRevLett.110.175002
    22|    read: true
    23|    sections: [all]
    24|  - path: /home/zhiping/knowledge_base/paper/2005/2005--Scalings for ultrarelativistic laser plasmas and quasimonoenergetic electrons
    25|    doi: 10.1063/1.1884126
    26|    read: true
    27|    sections: [all]
    28|confidence: high
    29|---
    30|
    31|# HHG Scaling Laws
    32|
    33|## Overview
    34|
    35|The reflected harmonic spectrum from relativistic laser-plasma HHG generally follows a power-law I(ω) ∝ ω^{-p} up to a cutoff frequency ω_c, beyond which intensity drops exponentially. The values of p and ω_c are central to predicting HHG source utility.
    36|
    37|## Historical Predictions for p
    38|
    39|| Model | Year | p value | Cutoff | Original Paper |
    40||-------|------|---------|--------|----------------|
    41|| Gordienko OMM | 2004 | 5/2 (quasimonochromatic), 3 (broadband) | ∝ γ² | Gordienko et al., PRL 93, 115002 (2004) |
    42|| Baeva BGP | 2006 | **8/3** | √8α · γ³ | Baeva et al., PRE 74, 046404 (2006) |
    43|| CSE model | 2010 | **4/3** | √8α · γ³ | an der Brügge & Pukhov, Phys. Plasmas 17, 033110 (2010) |
    44|| Thin-foil (Edwards) | 2019 | **10/3** | bunch-width limited | Edwards et al., PRL 124, 185004 (2020) |
    45|
    46|— Edwards' thesis (Princeton 2019) §4.1 [KB: .../thesis.md, line 1609]
    47|  "proposed ultimate values of p span a broad range, with strong implications for the usefulness of HHG-based x-ray sources"
    48|
    49|**Key original papers**:
    50|- S. Gordienko, A. Pukhov, O. Shorokhov, and T. Baeva, Phys. Rev. Lett. 93, 115002 (2004)
    51|- T. Baeva, S. Gordienko, and A. Pukhov, Phys. Rev. E 74, 046404 (2006)
    52|- D. an der Brügge and A. Pukhov, Phys. Plasmas 17, 033110 (2010)
    53|
    54|## Edwards' Key Finding: p Is NOT Universal
    55|
    56|Edwards' PIC simulations (EPOCH, BOPS) across a₀ = 1–1000 and N = 12–1000 show that **p is not a universal constant** but depends on a₀/N:
    57|
    58|### Asymptotic limit (a₀ → ∞ at fixed S)
    59|p approaches a constant that scales logarithmically with S:
    60|
    61|**p ≈ 1.5 ln(a₀/N)** for a₀/√N > 2
    62|
    63|### Range of p values
    64|At fixed S, p can range from **>6 to <2**, depending on a₀/N.
    65|
    66|### Transition at a₀/N ≈ 0.2
    67|For a₀/N > 0.2, p exceeds the BGP prediction of 8/3. This regime corresponds to I_out > I_in, violating the oscillating mirror model assumptions.
    68|
    69|— Edwards' thesis (Princeton 2019) §4.1.3 [KB: .../thesis.md, line 1663]
    70|  "for a₀ → ∞ at fixed S, p approaches a constant value"
    71|
    72|— doi: 10.1103/PhysRevLett.117.125001
    73|  [KB: /home/zhiping/knowledge_base/paper/2016/2016--Waveform-Controlled Relativistic High-Order-Harmonic Generation]
    74|  (Full paper read — waveform-controlled HHG, optimal waveform at ω_pR)
    75|
    76|## Bunch-Width Limited Cutoff
    77|
    78|The CSE model predicts cutoff at ω_γ = √8α · γ³, but Edwards shows the **actual cutoff is much lower**, limited by the electron bunch width Δ:
    79|
    80|**ω_b = λ/(2Δ)**
    81|
    82|Above ω_b, the spectrum gains an additional ω^{-2} factor from incoherent summation:
    83|
    84|**I(ω) ∝ ω^{-4/3} · ω^{-2} = ω^{-10/3}** for ω > ω_b
    85|
    86|— Edwards' thesis (Princeton 2019) §4.3.4 [KB: .../thesis.md, line 1923]
    87|  "The bunch width Δ therefore sets a frequency cutoff ω_b approximated as: ω_b/ω_L = λ/(2Δ)"
    88|
    89|— doi: 10.1103/PhysRevLett.124.185004
    90|  [KB: /home/zhiping/knowledge_base/paper/2020/2020--Electron-Nanobunch-Width-Dominated Spectral Power Law for Relativistic Harmonic Generation from Ultrathin Foils]
    91|  (Full paper read — bunch-width limited cutoff, thin-foil n^{-10/3})
    92|
    93|## Thin-Foil Scaling: n^{-10/3}
    94|
    95|For thin-foil targets (S·D < 0.2), individual electrons follow CSE trajectories with p = 4/3, but the finite bunch size adds ω^{-2}:
    96|
    97|**I(ω) ∝ ω^{-10/3}** (p = 10/3 ≈ 3.3 ± 0.5)
    98|
    99|The mechanism: the bunch has a sharp leading edge. Only electrons within λ/2 of the leading edge contribute coherently at frequency ω. The number of coherent electrons ∝ λ_n, so intensity ∝ λ_n² ∝ ω^{-2}.
   100|
   101|— Edwards' thesis (Princeton 2019) §4.2.2 [KB: .../thesis.md, line 1821]
   102|  "the harmonic intensity varies as: I(ω) ∝ ω^{-10/3}"
   103|
   104|— doi: 10.1103/PhysRevLett.124.185004
   105|  [KB: /home/zhiping/knowledge_base/paper/2020/2020--Electron-Nanobunch-Width-Dominated Spectral Power Law for Relativistic Harmonic Generation from Ultrathin Foils]
   106|  (Full paper read — thin-foil scaling law)
   107|
   108|## Efficiency Scaling with a₀/N
   109|
   110|The attosecond pulse generation efficiency follows:
   111|
   112|**I_a/I_L ∝ (a₀/N)^q**
   113|
   114|with q₁ ≈ 9.2 for a₀/N < 0.2 (increasing efficiency) and q₂ ≈ -1.5 to -1.7 for a₀/N > 0.5 (decreasing efficiency due to relativistic transparency).
   115|
   116|**Optimal efficiency at a₀/N ≈ 0.2–0.5**
   117|
   118|— Edwards' thesis (Princeton 2019) §4.1.1 [KB: .../thesis.md, line 1631]
   119|  "a maximum pulse generation efficiency exists near a₀/N ≈ 0.2 − 0.5"
   120|
   121|— doi: 10.1103/PhysRevLett.110.175002
   122|  [KB: /home/zhiping/knowledge_base/paper/2013/2013--Scaling High-Order Harmonic Generation from Laser-Solid Interactions to Ultrahigh Intensity]
   123|  (Full paper read — scaling of HHG to ultrahigh intensity)
   124|
   125|## Surface Displacement Scaling
   126|
   127|From ponderomotive force vs. ion restoring force balance:
   128|
   129|**x_disp ∝ a₀/N**
   130|
   131|Confirmed by PIC simulations: x/λ = 0.31 · a₀/N at θ_L = 15°.
   132|
   133|— Edwards' thesis (Princeton 2019) §4.3.2 [KB: .../thesis.md, line 1882]
   134|  "x_disp ∝ a₀/N"
   135|
   136|## Lorentz Factor Scaling
   137|
   138|**γ ∝ a₀** at fixed a₀/N (from similarity theory: γ = S^{α_γ} a₀ with α_γ ≈ 3)
   139|
   140|— doi: 10.1063/1.1884126
   141|  [KB: /home/zhiping/knowledge_base/paper/2005/2005--Scalings for ultrarelativistic laser plasmas and quasimonoenergetic electrons]
   142|  (Full paper read — similarity theory)
   143|
   144|## Preplasma Effects on Scaling
   145|
   146|Finite plasma gradients modify the scaling substantially:
   147|- For L_e/λ = 0 to 0.1: efficiency increases dramatically
   148|- Optimal L_e/λ ≈ 0.1 (but depends on a₀)
   149|- The a₀-dependence of efficiency weakens with gradient
   150|
   151|— Edwards' thesis (Princeton 2019) §4.1.4 [KB: .../thesis.md, line 1679]
   152|  "A substantial increase in efficiency occurs as L_e/λ is increased from 0 to 0.1"
   153|
   154|— doi: 10.1103/PhysRevLett.110.175002
   155|  [KB: /home/zhiping/knowledge_base/paper/2013/2013--Scaling High-Order Harmonic Generation from Laser-Solid Interactions to Ultrahigh Intensity]
   156|  (Full paper read — preplasma optimization)
   157|
   158|## Summary Table
   159|
   160|| Quantity | Scaling | Conditions | Original Paper |
   161||----------|---------|------------|----------------|
   162|| Power-law exponent p | 1.5 ln(a₀/N) | a₀/√N > 2, normal incidence | Edwards & Mikhailova, PRL 117, 125001 (2016) |
   163|| Thin-foil p | 10/3 | S·D < 0.2 | Edwards et al., PRL 124, 185004 (2020) |
   164|| Cutoff (bunch-width) | ω_b = λ/(2Δ) ∝ a₀ | General | Edwards et al., PRL 124, 185004 (2020) |
   165|| Cutoff (Lorentz) | ω_γ = √8α · γ³ ∝ a₀³ | Single electron | Baeva et al., PRE 74, 046404 (2006) |
   166|| Efficiency peak | a₀/N ≈ 0.2–0.5 | Steep gradient | Edwards & Mikhailova, PRL 117, 125001 (2016) |
   167|| Surface displacement | x ∝ a₀/N | a₀ >> 1 | Gordienko & Pukhov, Phys. Plasmas 12, 043109 (2005) |
   168|| Lorentz factor | γ ∝ a₀ | Fixed a₀/N | Gordienko & Pukhov, Phys. Plasmas 12, 043109 (2005) |
   169|
   170|## Links
   171|
   172|- [[rom-theory]] — BGP prediction of p = 8/3
   173|- [[cse-theory]] — CSE prediction of p = 4/3
   174|- [[unified-hhg-picture]] — Why both are synchrotron radiation
   175|- [[waveform-engineering]] — How to improve scaling via two-color
   176|- [[preplasma-scale-length]] — Gradient effects on scaling
   177|