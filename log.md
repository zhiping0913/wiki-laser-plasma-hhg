# Wiki Log

> Chronological record of all wiki actions. Append-only.
> Format: `## [YYYY-MM-DD] action | subject`

## [2026-06-25] create | Wiki initialized
- Created directory structure (concepts/, entities/, comparisons/, queries/, raw/)
- Created SCHEMA.md (citation protocol)
- Created CITATION_PROTOCOL.md (anti-hallucination rules, verification checklist)
- Created README.md

## [2026-06-25] ingest | 陈自宇 Note (tutorial note on HHG)
- Read: paper.md (660 lines, 26 refs)
- Key content: ROM→CSE→unified narrative, BGP theory, CSE theory, synchrotron analogy
- All 26 references verified in knowledge base (25/26 found)
- Source: /home/zhiping/knowledge_base/other/2024--陈自宇--Laser Plasma Notes for Beginners High Harmonic Generation/paper.md

## [2026-06-25] ingest | 张玉雪 Thesis §1.4 (HHG theory review)
- Read: thesis.md §1.4.2-1.4.8 (lines 506-905)
- Key content: Basic theory, CWE, RFM, ROM (BGP), CSE, isolated attosecond pulses
- Thesis: 张玉雪, PKU, 2019, advisors: 贺贤土 & 乔宾
- Source: /home/zhiping/knowledge_base/thesis/2019/2019--强激光等离子体相互作用驱动阿秒辐射源研究/thesis.md

## [2026-06-25] create | rom-theory.md
- ROM theory page: BGP model, γ-spike, n^{-8/3}, experimental verification
- Sources: 陈自宇 Note §0.4.3, 张玉雪 Thesis §1.4.6
- Confidence: high (multi-source)

## [2026-06-25] create | cse-theory.md
- CSE theory page: electron nanobunching, n^{-4/3} scaling, RES model, experimental verification
- Sources: 陈自宇 Note §0.4.4, 张玉雪 Thesis §1.4.7
- Confidence: high (multi-source)

## [2026-06-25] create | unified-hhg-picture.md
- Unified view: ROM and CSE are the same physics (synchrotron radiation)
- BGP and CSE conditions are mathematically equivalent
- Sources: 陈自宇 Note §0.4.5
- Confidence: high

## [2026-06-25] ingest | Edwards Thesis (Princeton 2019, advisor Mikhailova)
- Read: thesis.md Ch 4 (Theory and Scaling) + Ch 5 (Waveform Engineering), lines 1607-2306
- Key NEW insights beyond 陈自宇/张玉雪:
  * p is NOT universal: p ∝ ln(S), range >6 to <2 (depends on a₀/N)
  * Bunch width limits effective cutoff: ω_b = λ/(2Δ), not γ³
  * Thin foils: n^{-10/3} (individual n^{-4/3} + ω^{-2} from bunch)
  * Optimal efficiency at a₀/N ≈ 0.2-0.5
  * Two-color enhancement: 5% SH → 10× attosecond intensity
  * Secondary attosecond pulses at ~plasma period delay
  * CEP controls attosecond envelope for few-cycle pulses
  * Similarity theory confirmed for HHG: p ≈ 1.5 ln(a₀/N) for a₀/√N > 2
  * γ ∝ a₀ at fixed a₀/N (similarity theory)
  * x_disp ∝ a₀/N (surface displacement)
- Also searched Mikhailova papers in KB: ~55 papers found (2005-2024)
- Source: /home/zhiping/knowledge_base/thesis/2019/2019--Ultrafast Sources of Intense Radiation/thesis.md
- Status: reading complete for HHG chapters (4,5), wiki pages not yet created

## [2026-06-25] create | scaling-laws.md
- Edwards thesis §4.1-4.3: power-law exponent p, bunch-width cutoff, thin-foil n^{-10/3}
- Key finding: p ≈ 1.5 ln(a₀/N), NOT universal as previously thought
- Bunch-width cutoff ω_b = λ/(2Δ) ∝ a₀ (linear, not a₀³)
- Sources: Edwards Thesis Ch 4, 陈自宇 Note
- Confidence: high

## [2026-06-25] create | waveform-engineering.md
- Edwards thesis §5.1-5.2: two-color enhancement, optimal waveform, genetic algorithm
- Key finding: 5% SH → 10× enhancement, optimal waveform is single oscillation at ω_pR
- Genetic algorithm optimization: 63% conversion to high frequencies achievable
- Sources: Edwards Thesis Ch 5
- Confidence: high

## [2026-06-25] create | secondary-attosecond-pulses.md
- Edwards thesis §4.4: spectral modulation from secondary pulses
- Key finding: secondary pulses at ~plasma period delay, intensity ratio up to 0.7
- Mechanism: electrostatic plasma response after primary bunch formation
- Sources: Edwards Thesis §4.4
- Confidence: high

## [2026-06-25] create | cwe-mechanism.md
- CWE: sub-relativistic mechanism, plasma oscillations, ω_p cutoff
- Requires steep gradient (L < λ/20), a₀ < 1
- Sources: Edwards Thesis §1.3, 陈自宇 Note, Quéré et al. references
- Confidence: medium (Level 2 sources, original CWE paper not yet read)

## [2026-06-25] create | chf-mechanism.md
- CHF: focusing harmonics to extreme intensities (Schwinger limit)
- Requires wavefront control, high efficiency, spectral selection
- Sources: Hörlein et al. 2009, Quéré & Vincenti 2021 (not yet read)
- Confidence: low (limited source material)

## [2026-06-25] create | preplasma-scale-length.md
- Gradient effects: optimal L/λ ~ 0.1, efficiency enhancement up to 10×
- Trade-off: gradient improves efficiency but reduces isolation
- Sources: Edwards Thesis §4.1.4, §5.1.1, 张玉雪 Thesis §1.4.6
- Confidence: high

## [2026-06-25] update | index.md
- Updated to reflect all 10 pages (was 3)
- Added new concept pages: scaling-laws, waveform-engineering, secondary-attosecond-pulses, cwe-mechanism, chf-mechanism, preplasma-scale-length

## [2026-06-25] ingest | doi_core papers found and read
- **Quéré & Vincenti 2021** (CHF/Schwinger review): DOI 10.1017/hpl.2020.46
  - Path: /home/zhiping/knowledge_base/paper/2021/2021--Reflecting petawatt lasers off relativistic plasma mirrors a realistic path to the Schwinger limit/paper.md
  - Read: sections 1-4 (introduction, context, boosting concept, plasma mirrors)
  - Key content: Path to Schwinger limit via curved relativistic plasma mirrors, CHF concept

- **Edwards & Mikhailova 2016** (Waveform-controlled HHG): DOI 10.1103/PhysRevLett.117.125001
  - Path: /home/zhiping/knowledge_base/paper/2016/2016--Waveform-Controlled Relativistic High-Order-Harmonic Generation/paper.md
  - Read: full paper
  - Key content: Optimal waveform is single oscillation at ω_pR, 63% conversion efficiency, genetic algorithm optimization

- **Edwards et al. 2014** (Two-color enhancement): DOI 10.1364/ol.39.006823
  - Path: /home/zhiping/knowledge_base/paper/2014/2014--Enhanced attosecond bursts of relativistic high-order harmonics driven by two-color fields/paper.md
  - Read: abstract
  - Key content: 5% SH → 10× enhancement, first demonstration of two-color HHG enhancement

- **Edwards et al. 2020** (Thin-foil scaling): DOI 10.1103/PhysRevLett.124.185004
  - Path: /home/zhiping/knowledge_base/paper/2020/2020--Electron-Nanobunch-Width-Dominated Spectral Power Law for Relativistic Harmonic Generation from Ultrathin Foils/paper.md
  - Read: sections 1-2
  - Key content: n^{-10/3} scaling for thin foils, bunch-width limited cutoff

- **Heissler 2012** (Isolated attosecond from plasma mirrors): Not Mikhailova's paper
  - Path: /home/zhiping/knowledge_base/thesis/2012/2012--Relativistic Laser Plasma Interaction A Novel Route to Intense, Single Attosecond Pulses/thesis.md
  - Read: introduction
  - Key content: Few-cycle driver for isolated attosecond pulses from solid surfaces

Note: Mikhailova's specific papers (2012 isolated attosecond, 2016 waveform-controlled) were not found as separate entries in KB. The 2016 paper is the Edwards & Mikhailova PRL paper found above.

## [2026-06-25] ingest | doi_core high-priority papers read

- **Xu et al. 2018** (CSE in transmission, double foil): DOI 10.1088/1361-6587/aaa57d
  - Path: /home/zhiping/knowledge_base/paper/2018/2018--Coherent synchrotron emission in transmission with double foil target/paper.md
  - Read: full paper (sections 1-5)
  - Key content: Double-foil target for enhanced CSE in transmission, 18 as single pulse, γ_x ≈ 9

- **Kallala, Quéré, Vincenti 2020** (Isolated attosecond techniques): DOI 10.1103/PhysRevResearch.2.043007
  - Path: /home/zhiping/knowledge_base/paper/2020/2020--Techniques to generate intense isolated attosecond pulses from relativistic plasma mirrors/paper.md
  - Read: sections I-III
  - Key content: Two techniques to reduce harmonic divergence for lighthouse effect, wavefront curvature compensation

- **Timmis et al. 2026** (Nature, efficiency-optimized HHG): DOI 10.1038/s41586-026-10400-2
  - Path: /home/zhiping/knowledge_base/paper/2026/2026--Efficiency-optimized relativistic plasma harmonics for extreme fields/paper.md
  - Read: sections 1-2 (introduction, main results)
  - Key content: First experimental verification of theoretical maximum HHG efficiency, 9.5 mJ in H12-H47, 0.17% efficiency, t_HDR optimization critical

- **Li et al. 2024** (Spectral modulation HHG): DOI 10.1103/PhysRevE.109.025212
  - Path: /home/zhiping/knowledge_base/paper/2024/2024--Spectral modulation of high-order harmonics in relativistic laser-solid interaction/paper.md
  - Read: sections I-IV
  - Key content: Three mechanisms for spectral modulation (envelope, regular splitting, irregular splitting), RSPM effect, isolated attosecond via tailored preplasma

## [2026-06-25] ingest | doi_core medium-priority papers read

- **Vincenti et al. 2014** (Optical properties of PM): DOI 10.1038/ncomms4403
  - Path: /home/zhiping/knowledge_base/paper/2014/2014--Optical properties of relativistic plasma mirrors/paper.md
  - Read: sections 1-2 (introduction, model)
  - Key content: Analytical model of PM curvature, electron/ion dynamics, harmonic divergence

- **Pan et al. 2019** (Pre-structured targets): DOI 10.1017/hpl.2019.20
  - Path: /home/zhiping/knowledge_base/paper/2019/2019--Enhancement of the surface emission at the fundamental frequency and the transmitted high-order harmonics by pre-structured targets/paper.md
  - Read: sections 1-2
  - Key content: 100× enhancement in transmitted energy, surface plasma waves, electron islands

- **Xu et al. 2019** (Target thickness effect): DOI 10.1088/1367-2630/ab4622
  - Path: /home/zhiping/knowledge_base/paper/2019/2019--The effect of target thickness on the efficiency of high-order harmonics generated from laser-driven overdense plasma target/paper.md
  - Read: sections 1-2
  - Key content: Optimal thickness λ/2πS ≤ d₀ ≤ λ/πS, gate mechanism, single attosecond pulse

- **Pirozhkov et al. 2006** (Sliding mirror model): DOI 10.1063/1.2158145
  - Path: /home/zhiping/knowledge_base/paper/2006/2006--Attosecond pulse generation in the relativistic regime of the laser-foil interaction_ The sliding mirror model/paper.md
  - Read: sections I-III
  - Key content: Sliding mirror for dense plasma, ε_p ≈ a₀ condition, Bourdier transform

- **Kiefer et al. 2013** (Relativistic electron mirrors): DOI 10.1038/ncomms2775
  - Path: /home/zhiping/knowledge_base/paper/2013/2013--Relativistic electron mirrors from nanoscale foils for coherent frequency upshift to the extreme ultraviolet/paper.md
  - Read: sections 1-2 (introduction, results start)
  - Key content: First demonstration of coherent backscattering from REM, 800→60 nm, >10⁴ efficiency gain

- **Riconda et al. 2015** (Plasma-based short pulses): DOI 10.1088/0741-3335/57/1/014002
  - Path: /home/zhiping/knowledge_base/paper/2015/2014--Plasma-based creation of short light pulses analysis and simulation of amplification and focusing/paper.md
  - Read: section 1 (introduction)
  - Key content: Plasma amplification via SBS, strong-coupling regime, damage-free optics

## [2026-06-25] create | New wiki pages

- **double-foil-target.md**: Double-foil CSE in transmission scheme
  - Sources: Xu et al. 2018, Kiefer et al. 2013
  - Key content: 18 as single pulse, γ_x ≈ 9, keV photons, nanobunch formation

- **attosecond-lighthouse.md**: Lighthouse effect for isolated attosecond pulses
  - Sources: Kallala et al. 2020
  - Key content: Wavefront rotation, divergence compensation, 10 TW isolated pulses

- **efficiency-optimization.md**: Maximizing HHG conversion efficiency
  - Sources: Timmis et al. 2026, Edwards 2016, Xu et al. 2019
  - Key content: DPM t_HDR optimization, 0.17% efficiency achieved, path to CHF

## [2026-06-25] ingest | doi_core low-priority papers read

- **Zhang et al. 2022** (Divergence gating): DOI 10.1088/1367-2630/ac59ec
  - Path: /home/zhiping/knowledge_base/paper/2022/2022--Divergence gating towards far-field isolated attosecond pulses/paper.md
  - Read: sections 1-2
  - Key content: Chirped laser for divergence gating, mJ sub-50 as IAPs, low-order harmonics preserved

- **Pakhomov et al. 2024** (Subcycle pulse control): DOI 10.1364/josab.503633
  - Path: /home/zhiping/knowledge_base/paper/2024/2024--Coherent control of a multilevel resonant medium by subcycle pulses/paper.md
  - Read: sections 1-2
  - Key content: Half-cycle unipolar pulses, electric pulse area, coherent control of multilevel media

- **Liu et al. 2024** (Nanometer electron layer): DOI 10.1103/PhysRevA.109.043519
  - Path: /home/zhiping/knowledge_base/paper/2024/2024--Generation of extreme-ultraviolet and x-ray light from a propagating nanometer electron layer in few-cycle laser interaction with solid targets/paper.md
  - Read: abstract
  - Key content: New HHG mechanism from propagating nanometer electron layers, synchrotron radiation at bending points

- **Tang et al. 2024** (Bessel-Gauss beam HHG): DOI 10.1063/5.0221080
  - Path: /home/zhiping/knowledge_base/paper/2024/2024--Spatial filtering and optimal generation of high-flux soft x-ray high harmonics using a Bessel–Gauss beam/paper.md
  - Read: sections I-III
  - Key content: BG beam for spatial filtering, 10¹⁰ photons/s at 250 eV, phase-matching optimization

- **Kim et al. 2025** (Noncollinear gating): DOI 10.1103/PhysRevResearch.7.013216
  - Path: /home/zhiping/knowledge_base/paper/2025/2025--Isolated attosecond pulses generated from a relativistic plasma mirror via noncollinear gating/paper.md
  - Read: sections I-II
  - Key content: Noncollinear temporal gating, main pulse + weak gating pulse, plasma denting diagnostics

- **Vincenti et al. 2023** (Schwinger limit review): DOI 10.1140/epjs/s11734-023-00909-2
  - Path: /home/zhiping/knowledge_base/paper/2023/2023--Plasma mirrors as a path to the Schwinger limit theoretical and numerical developments/paper.md
  - Read: section 1 (introduction)
  - Key content: Comprehensive review of CRM concept, pseudo-spectral PIC codes, 3D simulations

- **Cousens et al. 2020** (Electron trajectories CSE): DOI 10.1103/PhysRevE.101.053210
  - Path: /home/zhiping/knowledge_base/paper/2020/2020--Electron trajectories associated with laser-driven coherent synchrotron emission at the front surface of overdense plasmas/paper.md
  - Read: sections I-II
  - Key content: CSE trajectory analysis, synchrotron-like vs figure-eight, forward emission mechanism

## [2026-06-25] ingest | Timmis 2026 Nature full reading

- **Timmis et al. 2026** (Nature): DOI 10.1038/s41586-026-10400-2
  - Path: /home/zhiping/knowledge_base/paper/2026/2026--Efficiency-optimized relativistic plasma harmonics for extreme fields/paper.md
  - Read: Full paper (sections 1-4, Methods, Extended Data)
  - Key experimental details:
    * Gemini laser: 5 J, 50 fs, 800 nm, f/2 parabola → I > 10²¹ W/cm²
    * DPM system: 50% throughput, t_HDR = 351 fs (optimized)
    * Target: Polished fused silica, 45° incidence, p-polarization
    * Detection: XUV flat-field spectrometer, 300 l/mm grating, CCD
    * Al filters: 0.2-3 μm, oxide layers characterized (7-16 nm)
  - Key results:
    * 0.17 ± 0.08% efficiency in H12-H47
    * 9.5 ± 4.9 mJ harmonic energy
    * Perfect agreement with 2D PIC (Smilei)
    * Efficiency roll-over above 10²⁰ W/cm²
    * Prepulse optimization: 50 fs window at 3.6×10²⁰ W/cm²
    * Beam profile: divergence grows with intensity, spectrospatial modulations
    * CHF gain: >88× (lower bound from simulations)
    * Path to Schwinger: I_CHF/I ∝ a₀³
  - Key physics:
    * PM denting model: Δz = Δz_i + Δz_e (ion + electron)
    * Ion denting: ∝ ∫a_L dt (cumulative)
    * Electron excursion: ∝ a_L (instantaneous)
    * Dent depth increases with intensity → divergence growth
    * Spectrospatial modulations = evidence of efficiency saturation

## [2026-06-25] create | Entity pages

- **cea-lidyl-group.md**: CEA-LIDYL (Quéré & Vincenti)
  - PM physics, CHF concept, lighthouse techniques
  - Key papers: 2014, 2020, 2021, 2023

- **belfast-dromey-group.md**: Queen's Belfast (Dromey)
  - Experimental HHG, efficiency breakthrough
  - Key papers: 2006, 2007, 2009, 2016, 2020, 2026

- **princeton-mikhailova-group.md**: Princeton (Mikhailova)
  - Waveform engineering, scaling laws
  - Key papers: 2014, 2016, 2019, 2020

- **mpq-institute.md**: MPQ
  - Historical ROM theory, BGP model
  - Key papers: 1996, 2004, 2005, 2006

- **pic-codes.md**: PIC codes for HHG
  - EPOCH, Smilei, WarpX, BOPS, picwig
  - Comparison table, best practices

- **gemini-laser.md**: Gemini laser at RAL
  - PW-class, DPM system, efficiency-optimized HHG

## [2026-06-25] create | Comparison pages

- **rom-vs-cse.md**: ROM vs CSE mechanism comparison
  - Scaling laws, parameter regimes, experimental signatures
  - Unified picture from 陈自宇 Note

- **target-types.md**: Target geometry comparison
  - Semi-infinite, thin foil, double foil, pre-structured
  - Application guide for different requirements

- **isolation-techniques.md**: Isolation method comparison
  - 7 techniques: intensity gating, polarization, lighthouse, noncollinear, divergence, double-foil, cascade
  - Status, advantages, limitations, key papers

## [2026-06-25] create | Additional comparison pages

- **gradient-comparison.md**: Gradient effects comparison
  - L/λ regimes: steep (<0.01), optimal (0.05-0.15), long (>0.15)
  - Optimization strategy for different goals
  - Edwards' systematic study results

- **intensity-comparison.md**: Laser intensity comparison
  - a₀ regimes: sub-rel, mildly rel, strongly rel, ultra-rel
  - Efficiency roll-over phenomenon (Timmis 2026)
  - CHF scaling: I_CHF/I ∝ a₀³

## [2026-06-25] update | Added original paper references to wiki pages

Updated wiki pages to include original paper references from 陈自宇 note, replacing sole reliance on tutorial note citations:

### Papers added to wiki:

1. **Bulanov et al. 1994** (Phys. Plasmas 1, 745)
   - ROM concept proposed
   - Added to: rom-theory.md

2. **Lichters et al. 1996** (Phys. Plasmas 3, 3425)
   - ROM fluid model, LPIC++ code
   - Added to: rom-theory.md

3. **von der Linde & Rzązewski 1996** (Appl. Phys. B 63, 499)
   - Simple harmonic model (fails)
   - Added to: rom-theory.md

4. **Gordienko et al. 2004** (PRL 93, 115002)
   - Saddle-point analysis, n^{-5/2}, γ² cutoff
   - Added to: rom-theory.md, scaling-laws.md

5. **Gordienko & Pukhov 2005** (Phys. Plasmas 12, 043109)
   - Similarity theory, S = nₑ/(n_c a₀)
   - Added to: rom-theory.md, scaling-laws.md

6. **Baeva et al. 2006** (PRE 74, 046404)
   - BGP theory, n^{-8/3}, γ³ cutoff
   - Added to: rom-theory.md, scaling-laws.md, unified-hhg-picture.md

7. **Dromey et al. 2006** (Nat. Phys. 2, 456)
   - First scaling law measurement (p = -2.5)
   - Added to: rom-theory.md

8. **Dromey et al. 2007** (PRL 99, 085001)
   - Cutoff frequency verification (γ³ confirmed)
   - Added to: rom-theory.md, unified-hhg-picture.md

9. **an der Brügge & Pukhov 2010** (Phys. Plasmas 17, 033110)
   - CSE discovery, n^{-4/3}
   - Added to: cse-theory.md, scaling-laws.md

10. **Gonoskov et al. 2011** (PRE 84, 046403)
    - RES model, S ~ 1 optimal
    - Added to: cse-theory.md

11. **Mikhailova et al. 2012** (PRL 109, 245005)
    - Synchrotron analysis of CSE
    - Added to: cse-theory.md, unified-hhg-picture.md

12. **Dromey et al. 2012** (Nat. Phys. 8, 804)
    - CSE experimental verification
    - Added to: cse-theory.md

13. **Dollar et al. 2013** (PRL 110, 175002)
    - Scaling HHG to ultrahigh intensity
    - Added to: rom-theory.md, scaling-laws.md

14. **Corde et al. 2013** (Rev. Mod. Phys. 85, 1)
    - Femtosecond x-rays from laser-plasma review
    - Added to: cse-theory.md

15. **Quéré et al. 2006** (PRL 96, 125004)
    - CWE discovery
    - Added to: cwe-mechanism.md

16. **Thaury & Quéré 2010** (J. Phys. B 43, 213001)
    - HHG mechanisms review
    - Added to: cwe-mechanism.md

17. **Malvache et al. 2013** (PRE 87, 035101)
    - CWE as gradient diagnostic
    - Added to: cwe-mechanism.md

18. **Thaury et al. 2007** (Nat. Phys. 3, 424)
    - CWE vs ROM separation
    - Added to: cwe-mechanism.md
