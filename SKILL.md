---
name: wiki-laser-plasma-hhg
description: >
  Research wiki for relativistic laser-solid HHG and attosecond source physics.
  Load this skill whenever the conversation involves: ROM theory, CSE theory, CWE mechanism,
  coherent harmonic focusing (CHF), attosecond pulse generation from plasma mirrors,
  preplasma scale length effects, HHG scaling laws, efficiency optimization, target type
  comparisons (semi-infinite, thin foil, double foil), isolation techniques (lighthouse,
  intensity gating), two-color waveform engineering, or any reference to specific groups
  (Mikhailova, Quéré/Vincenti, Dromey, Baeva-Gordienko-Pukhov). Also load when writing
  EPOCH input decks or analyzing PIC simulation results related to HHG.
version: git
---

# Wiki: Laser-Plasma HHG & Attosecond Sources

Zhiping's living research wiki. Domain: relativistic laser-solid interaction for high-harmonic
generation and attosecond pulse production. Git-tracked at `/home/zhiping/research_wiki/`.

## Navigation

Start with **`index.md`** — full catalog of 24 pages, organized by type.

| Directory | Content |
|-----------|---------|
| `concepts/` | Physics mechanisms, theories, phenomena |
| `entities/` | Groups, facilities, codes |
| `comparisons/` | Side-by-side analyses |

## Key Entry Points by Topic

| Question | Start here |
|----------|-----------|
| What is ROM / CSE / CWE? | `concepts/rom-theory.md`, `concepts/cse-theory.md`, `concepts/cwe-mechanism.md` |
| Are ROM and CSE different? | `concepts/unified-hhg-picture.md`, `comparisons/rom-vs-cse.md` |
| HHG scaling laws (p exponent) | `concepts/scaling-laws.md` |
| How to maximize efficiency? | `concepts/efficiency-optimization.md` |
| Preplasma effects | `concepts/preplasma-scale-length.md` |
| Isolated attosecond pulses | `concepts/attosecond-lighthouse.md`, `comparisons/isolation-techniques.md` |
| Two-color / waveform shaping | `concepts/waveform-engineering.md` |
| Target geometry choice | `comparisons/target-types.md` |
| Path to Schwinger limit | `concepts/chf-mechanism.md` |
| Which PIC code to use? | `entities/pic-codes.md` |

## Schema

See **`SCHEMA.md`** for full conventions: frontmatter spec, tag taxonomy, page thresholds,
citation protocol, wikilink format. Follow this schema when creating or updating wiki pages.

## Citation Rules

See **`CITATION_PROTOCOL.md`**. Never fabricate DOIs or titles. Verify from knowledge base
metadata.json before citing.

## Updating the Wiki

When Zhiping reads a new paper or derives a new result that belongs here:
1. Check `index.md` — does the topic already have a page?
2. If yes: open the page, add content, bump `updated` date
3. If no: create page using SCHEMA.md frontmatter, add to `index.md`, append to `log.md`
4. Minimum 2 outbound `[[wikilinks]]` per page
5. Commit to git when session is done
