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
- Read: thesis.md Ch 4 (Theory and Scaling) + Ch 5 (Waveform Engineering), lines 1607-2207
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
