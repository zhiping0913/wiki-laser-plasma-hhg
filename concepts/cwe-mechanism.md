     1|---
     2|title: CWE — Coherent Wake Emission
     3|created: 2026-06-25
     4|updated: 2026-06-25
     5|type: concept
     6|tags: [hhg, cwe, sub-relativistic, plasma-gradient, attosecond]
     7|sources:
     8|  - path: /home/zhiping/knowledge_base/paper/2006/2006--Coherent Wake Emission of High-Order Harmonics from Overdense Plasmas
     9|    doi: 10.1103/PhysRevLett.96.125004
    10|    read: true
    11|    sections: [all]
    12|  - path: /home/zhiping/knowledge_base/paper/2010/2010--High-order harmonic and attosecond pulse generation on plasma mirrors basic mechanisms
    13|    doi: 10.1088/0953-4075/43/21/213001
    14|    read: true
    15|    sections: [1, 2]
    16|  - path: /home/zhiping/knowledge_base/paper/2007/2007--Plasma mirrors for ultrahigh-intensity optics
    17|    doi: 10.1038/nphys595
    18|    read: true
    19|    sections: [all]
    20|  - path: /home/zhiping/knowledge_base/paper/2013/2013--Coherent wake emission spectroscopy as a probe of steep plasma density profiles
    21|    doi: 10.1103/PhysRevE.87.035101
    22|    read: true
    23|    sections: [all]
    24|---
    25|
    26|# CWE — Coherent Wake Emission
    27|
    28|## Physical Picture
    29|
    30|Coherent Wake Emission (CWE) is the dominant HHG mechanism for **sub-relativistic** laser intensities (a₀ < 1, Iλ² < 10¹⁸ W/cm² μm²) interacting with steep plasma density gradients (L < λ/20).
    31|
    32|### Step-by-step mechanism:
    33|
    34|1. **Electron extraction**: During p-polarized oblique incidence, the laser electric field component along the target normal pulls electrons out of the plasma surface
    35|
    36|2. **Ballistic acceleration**: Extracted electrons are accelerated by the laser field back into the plasma
    37|
    38|3. **Excitation of plasma oscillations**: These fast electron bunches travel through the plasma density gradient, exciting collective plasma oscillations (Langmuir waves) at the local plasma frequency
    39|
    40|4. **Coherent emission**: The plasma oscillations coherently radiate electromagnetic fields, producing harmonics up to the plasma frequency
    41|
    42|— doi: 10.1088/0953-4075/43/21/213001
    43|  [KB: /home/zhiping/knowledge_base/paper/2010/2010--High-order harmonic and attosecond pulse generation on plasma mirrors basic mechanisms]
    44|  §2: "CWE starts occurring at moderately high intensities (I ≃ 10¹⁶ W/cm²) and is triggered by laser-driven electron bunches that excite collective electronic plasma oscillations in the density gradient between vacuum and the plasma bulk."
    45|
    46|## Key Characteristics
    47|
    48|| Property | CWE | ROM/CSE |
    49||----------|-----|---------|
    50|| Intensity regime | a₀ < 1 (sub-relativistic) | a₀ > 1 (relativistic) |
    51|| Gradient requirement | Steep (L < λ/20) | Moderate (L ~ 0.1λ optimal) |
    52|| Spectral cutoff | ω_p (plasma frequency) | γ³ (Lorentz factor) |
    53|| Scaling | Discrete harmonics | Power-law continuum |
    54|| Phase | Different from ROM | — |
    55|| CEP sensitivity | Yes (few-cycle) | Weak (multi-cycle) |
    56|
    57|## CWE vs ROM: Distinct Mechanisms
    58|
    59|### CWE (sub-relativistic)
    60|- Driven by **resonance absorption** and **Brunel heating**
    61|- Requires p-polarization and oblique incidence
    62|- Harmonics up to ω_p only
    63|- Phase properties different from ROM
    64|
    65|### ROM (relativistic)
    66|- Driven by **ponderomotive force** on the electron surface
    67|- Works at any polarization (p more efficient)
    68|- Harmonics up to γ³ ω_L
    69|- Phase-locked attosecond pulses
    70|
    71|— doi: 10.1088/0953-4075/43/21/213001
    72|  [KB: /home/zhiping/knowledge_base/paper/2010/2010--High-order harmonic and attosecond pulse generation on plasma mirrors basic mechanisms]
    73|  §1: "Two main harmonic generation processes on PM have been identified in the literature... CWE starts occurring at moderately high intensities... The second mechanism, called 'relativistic oscillating mirror' (ROM), occurs at even higher intensities."
    74|
    75|## CWE as Gradient Diagnostic
    76|
    77|CWE harmonics can serve as a **diagnostic** of the plasma density gradient:
    78|- Harmonic spectrum shape encodes the density profile
    79|- Used to measure L in real-time during experiments
    80|
    81|— doi: 10.1103/PhysRevE.87.035101
    82|  [KB: /home/zhiping/knowledge_base/paper/2013/2013--Coherent wake emission spectroscopy as a probe of steep plasma density profiles]
    83|  (Full paper read — CWE as gradient diagnostic)
    84|
    85|## Historical Context
    86|
    87|### 2006: Discovery
    88|
    89|Quéré et al. first proposed and demonstrated CWE:
    90|- 50 fs, 1 TW laser at 45° oblique incidence
    91|- Observed harmonics 16-18 from solid target
    92|- Identified as distinct from ROM
    93|
    94|— doi: 10.1103/PhysRevLett.96.125004
    95|  [KB: /home/zhiping/knowledge_base/paper/2006/2006--Coherent Wake Emission of High-Order Harmonics from Overdense Plasmas]
    96|  (Full paper read — CWE discovery paper)
    97|
    98|### 2007: Systematic confirmation
    99|
   100|Thaury et al. provided systematic experimental evidence:
   101|- Clear separation of CWE and ROM regimes
   102|- Identified the role of plasma gradient
   103|
   104|— doi: 10.1038/nphys595
   105|  [KB: /home/zhiping/knowledge_base/paper/2007/2007--Plasma mirrors for ultrahigh-intensity optics]
   106|  (Full paper read — systematic CWE/ROM separation)
   107|
   108|## Relevance to Attosecond Source Development
   109|
   110|CWE harmonics have **different phase properties** than ROM harmonics, which affects:
   111|- Attosecond pulse formation (different timing)
   112|- Coherence properties
   113|- Pulse isolation
   114|
   115|For attosecond source development, CWE is generally **avoided** by using:
   116|- High-contrast pulses (to maintain steep gradient)
   117|- Relativistic intensities (a₀ > 1)
   118|- Short pulse durations (to prevent gradient expansion)
   119|
   120|## Links
   121|
   122|- [[rom-theory]] — Relativistic mechanism, distinct from CWE
   123|- [[cse-theory]] — Another relativistic mechanism
   124|- [[preplasma-scale-length]] — Gradient determines CWE vs ROM
   125|- [[scaling-laws]] — CWE has different scaling than ROM
   126|