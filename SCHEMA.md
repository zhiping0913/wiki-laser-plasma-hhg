# Wiki Schema

## Domain
Relativistic laser-solid-density plasma interaction high harmonic generation (HHG) for attosecond source physics. Covers: ROM theory, CSE theory, CWE mechanism, near-critical density targets, coherent harmonic focusing, PIC simulation methods, experimental techniques.

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `rom-theory.md`)
- Every wiki page starts with YAML frontmatter
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- **Provenance markers:** On pages that synthesize 3+ sources, append `^[source_path]` at the end of paragraphs whose claims come from a specific source
- **Citation protocol:** See CITATION_PROTOCOL.md — never fabricate DOIs/titles, verify from metadata.json

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query
tags: [from taxonomy below]
sources:
  - path: /path/to/source
    doi: 10.xxxx/xxxx (or null for notes/theses)
    read: true/false
    sections: [1, 2, 3]
confidence: high | medium | low
contested: true  # optional
---
```

## Tag Taxonomy

### Physics
- `hhg` — High harmonic generation (general)
- `rom` — Relativistic oscillating mirror
- `cse` — Coherent synchrotron emission
- `cwe` — Coherent wake emission
- `rfm` — Relativistic flying mirror
- `bgp` — Baeva-Gordienko-Pukhov theory
- `attosecond` — Attosecond pulse generation
- `preplasma` — Preplasma scale length effects
- `ponderomotive` — Ponderomotive force
- `doppler` — Doppler effect / frequency upshift
- `synchrotron` — Synchrotron radiation analogy
- `nanobunching` — Electron nanobunch formation
- `coherent-radiation` — Coherent vs incoherent radiation

### Laser-Plasma
- `laser-plasma` — General laser-plasma interaction
- `relativistic-plasma` — Relativistic intensity regime (a₀ ≥ 1)
- `near-critical-density` — Near-critical density targets
- `solid-target` — Solid density targets
- `thin-foil` — Nanometre-scale foil targets
- `two-color` — Two-color laser schemes

### Methods
- `pic-simulation` — Particle-in-cell simulation
- `theory` — Analytical theory
- `experiment` — Experimental results
- `review` — Review/tutorial content

### Meta
- `comparison` — Side-by-side analysis
- `frontier` — Open research directions
- `chf` — Coherent harmonic focusing
- `schwinger-limit` — Path to Schwinger limit

## Page Thresholds
- **Create a page** when a concept appears in 2+ sources OR is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions
- **Split a page** when it exceeds ~200 lines

## Source Priority
1. Primary sources (papers/theses in knowledge base) — read directly
2. Cross-referenced sources (cited in a source you read) — mark as "cited in"
3. AGM-only (found in citation network) — mark as "not yet read"

## Missing Papers Protocol
- During reading: mark gaps with `[SKIPPED: reason]`
- After session: compile Missing/Problematic Papers Report for PI
- See CITATION_PROTOCOL.md for details
