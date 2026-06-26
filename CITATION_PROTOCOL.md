# Wiki Citation Protocol

> Every citation in the wiki must be **traceable, verifiable, and contextualized**.
> This protocol exists because LLMs hallucinate references. The only defense is discipline.

---

## Citation Format Standard (MANDATORY)

### Primary Rule: Use DOI as Citation Identifier

**All citations must use DOI as the primary identifier.** Do NOT use "Author et al." format.

**Why DOI?**
1. **Unique**: DOI is the only globally unique, persistent identifier for academic papers
2. **Verifiable**: Can be instantly verified via `search.py --doi "10.xxx/xxx"`
3. **Traceable**: Direct path to knowledge base: `python3 search.py --doi "10.xxx/xxx"` returns exact KB path
4. **No hallucination**: DOI cannot be fabricated (unlike author names, titles, years)
5. **Direct access**: Can be opened as https://doi.org/10.xxx/xxx

### Citation Format

**For papers with DOI:**
```
— doi: 10.1103/PhysRevE.74.046404
  [KB: /home/zhiping/knowledge_base/paper/2006/2006--Theory of high-order...]
  §3: "exact quote or precise paraphrase"
```

**For theses (no DOI):**
```
— Edwards' thesis (Princeton 2019)
  [KB: /home/zhiping/knowledge_base/thesis/2019/2019--Ultrafast Sources...]
  §4.1: "exact quote or precise paraphrase"
```

### How to Find DOI from Knowledge Base

```bash
# Search by DOI (preferred)
python3 /home/zhiping/knowledge_base/utility/search.py --doi "10.1103/PhysRevE.74.046404"

# Search by title (when DOI unknown)
python3 /home/zhiping/knowledge_base/utility/search.py --title "Theory of high-order harmonic generation"

# Search by author + year
python3 /home/zhiping/knowledge_base/utility/search.py --author "Baeva" --year 2006
```

### What NOT to Write

❌ `— Baeva et al., Phys. Rev. E 74, 046404 (2006)`
❌ `— Baeva, Gordienko, Pukhov, PRE 74, 046404 (2006)`
❌ `— "Title of paper" (Author, Year)`

✅ `— doi: 10.1103/PhysRevE.74.046404`

---

## The Problem

An LLM writing "see Baeva et al. [PRE 74, 046404 (2006)]" may be:
- Correct (remembered from training data)
- Plausible but wrong (right authors, wrong DOI)
- Completely fabricated (hallucinated paper)

There is no way to tell which case it is without verification. Therefore:

**NEVER write a citation you have not verified against an actual source.**

---

## Citation Levels

### Level 1: Primary Source (strongest)

You have read the actual paper text in the knowledge base.

Format in wiki:
```
The BGP theory predicts I_n ∝ n^{-8/3} with cutoff at ω_max ∝ γ_max^3.
— doi: 10.1103/PhysRevE.74.046404
  [KB: /home/zhiping/knowledge_base/paper/2006/2006--Theory of high-order...]
  §3, saddle-point analysis of the reflected field integral (7),
  leading to the stationary-phase condition γ_ARP → ∞.
```

What's required:
- ✅ **DOI** (from metadata.json) — this is the primary identifier
- ✅ KB path where you read it
- ✅ Specific section/figure/equation you're referencing
- ✅ Paraphrase or quote of the relevant passage

### Level 2: Cross-referenced (strong)

You haven't read the paper, but another source you DID read cites it with specific claims.

Format in wiki:
```
The CSE scaling n^{-4/3} was first derived by an der Brügge and Pukhov.
— cited in doi: 10.1103/PhysRevE.74.046404
  [KB: /home/zhiping/knowledge_base/paper/2006/2006--Theory of high-order...]
  §I: "The high-harmonic spectrum intensity scaling is I_n ∝ n^{-4/3}"
  Original: doi: 10.1063/1.3353050
  [KB: /home/zhiping/knowledge_base/paper/2010/2010--Enhanced relativistic...]
```

What's required:
- ✅ The intermediate source you actually read (with path + location)
- ✅ The specific claim from that source
- ✅ The original paper's DOI (verified via search.py or metadata)
- ✅ Mark as "cited in [source]" so reader knows you didn't read the original

### Level 3: AGM-only (weak, use sparingly)

You found the paper in AGM citation network but haven't read it or seen it cited in a primary source.

Format in wiki:
```
Several papers have extended CSE theory to oblique incidence.
— AGM citation network analysis: 14 papers cite an der Brügge 2010
  [AGM: 10.1103/physplasmas.17.033110, 14 citations as of 2026-06-25]
  Specific papers not yet read.
```

What's required:
- ✅ Clearly mark as "not yet read"
- ✅ DOI verified in AGM
- ✅ Citation count and date
- ❌ Do NOT claim specific results from papers you haven't read

---

## Verification Checklist

Before writing any citation in the wiki, ask yourself:

1. **Have I read this paper's text?** → Level 1
2. **Have I seen it cited in a source I read, with a specific claim?** → Level 2
3. **Have I only seen its DOI in AGM?** → Level 3
4. **Am I remembering it from general knowledge?** → DO NOT CITE. Go verify first.

---

## How to Verify a Reference

```bash
# Step 1: Find the paper in knowledge base
python3 /home/zhiping/knowledge_base/utility/search.py --doi "10.1103/physreve.74.046404"

# Step 2: Read metadata.json for exact title, authors, journal
cat "/path/to/paper/metadata.json" | python3 -m json.tool

# Step 3: Read the actual text (paper.md or paper.pdf.md)
# Find the specific section/claim you want to cite

# Step 4: Record the evidence
# - Exact quote or precise paraphrase
# - Section number, equation number, figure number
# - Line number in the .md file (for traceability)
```

---

## Anti-Hallucination Rules

1. **Always use DOI as citation identifier.** Never use "Author et al." format.
2. **Never write a DOI from memory.** Always look it up via search.py or metadata.json.
3. **Never say "paper X shows Y" unless you can point to the specific passage.**
4. **If you can't verify a claim, write "[NEEDS VERIFICATION]" and move on.**
5. **When multiple papers exist on a topic, verify you're citing the right one via DOI.**
6. **Use `search.py --doi` to locate papers in KB before citing them.**
5. **If you can't verify a claim, write "unverified — needs checking" explicitly.**
6. **When multiple papers exist on a topic, verify you're citing the right one.**
   (e.g., Gordienko has both 2004 [n^{-5/2}] and 2005 [similarity theory] papers)

---

## Handling Missing or Unreadable Papers

During reading, you will encounter references that you cannot access. Common cases:

| Case | Example | Action |
|------|---------|--------|
| Paper not in knowledge base | search.py returns empty | Skip, log to missing report |
| paper.md has no body text (old papers, <2000) | Only title + abstract in paper.md | Try paper.pdf.md; if also missing/broken, skip |
| paper.pdf.md is garbled OCR | Math symbols mangled, columns scrambled | Attempt extraction; if unreadable, skip |
| paper.md exists but too short (<500 chars body) | Publisher HTML had no full text | Try paper.pdf.md as fallback |
| metadata.json exists but no md files listed | `"md": []` | Cannot read — skip, log |
| Supplemental files missing | Expected supplemental dir absent | Note as incomplete, continue |

**Protocol:**

1. **During reading:** Mark the gap with `[SKIPPED: reason]` in your notes. Do not stop the reading flow.
2. **After the session:** Compile a **Missing/Problematic Papers Report** and deliver to the PI (主人).

### Missing/Problematic Papers Report Template

At the end of each reading session, produce:

```
## Missing/Problematic Papers Report — [date]

### Not in Knowledge Base (need download)
- [ ] 10.xxxx/xxxxx — Title (cited in: source X, line Y)
- [ ] 10.xxxx/xxxxx — Title (cited in: source X, line Y)

### In KB but Unreadable
- 10.xxxx/xxxxx — paper.md empty body, paper.pdf.md garbled (cited in: source X)
- 10.xxxx/xxxxx — no md files in metadata.json (cited in: source X)

### Partially Readable (some content extracted, gaps remain)
- 10.xxxx/xxxxx — paper.md missing figures/equations, paper.pdf.md partial (sections 3-4 unreadable)

### Action Items
- Priority downloads: [list DOIs most critical for wiki completeness]
- OCR re-runs needed: [list papers that need better paper.pdf.md conversion]
```

This report goes to the PI, who decides what to download/fix. The agent does NOT attempt to download anything.

---

## Reading Supplemental Materials

Many papers have supplementary information that contains critical details not in the main text:

| Content Type | Where to Find | Why It Matters |
|-------------|---------------|----------------|
| Detailed derivations | supplemental--*.pdf.md | Full mathematical proofs omitted from main text |
| Simulation parameters | supplemental--*.pdf.md | PIC setup, grid resolution, boundary conditions, particle numbers |
| Experimental methods | supplemental--*.pdf.md | Laser specs, target fabrication, detector calibration |
| Additional data | supplemental--*.pdf.md | Extended figures, parameter scans, error analysis |
| Errata/corrections | erratum--paper.pdf.md | Fixes to published results |

**Protocol:**

1. After reading the main paper text (paper.md or paper.pdf.md), **always check `metadata.json` for supplemental files:**
   ```python
   meta = json.load(open("metadata.json"))
   for md_file in meta.get("md", []):
       if md_file.startswith("supplemental/"):
           # Read this file
   ```

2. **Prioritize supplemental reading when:**
   - The main text says "see supplementary material for details" on a derivation you need
   - You need simulation parameters (grid size, dt, particle count, etc.)
   - You need experimental details (laser energy, pulse duration, target specs)
   - The paper presents a model but the derivation is in the supplement

3. **When citing supplemental content, specify it explicitly:**
   ```
   The PIC simulation used a 2000×4000 grid with Δx = λ_L/200,
   100 particles per cell, and absorbing boundaries.
   — from supplementary material of [paper DOI]
     [KB: .../supplemental/supplemental--supplement.pdf.md, §S.II]
   ```

4. **Errata supersede the main text.** If `erratum--paper.pdf.md` exists and addresses a claim you're citing, the erratum takes priority.

---

## Wiki Frontmatter for Citations

Every wiki page with citations must include in frontmatter:

```yaml
---
sources:
  - path: /home/zhiping/knowledge_base/paper/2006/2006--Theory of.../
    doi: 10.1103/physreve.74.046404
    read: true                    # have I actually read this?
    sections: [3, 4]              # which sections I referenced
  - path: /home/zhiping/knowledge_base/other/2024--陈自宇--.../paper.md
    read: true
    sections: [0.4.3, 0.4.4, 0.4.5]
---
```

---

## What Happens When I Catch Myself About to Hallucinate

1. **STOP** — do not write the unverified claim
2. **CHECK** — use search.py, metadata.json, or AGM to verify
3. **If verified** — write with full provenance (Level 1 or 2)
4. **If not found** — write "[NEEDS VERIFICATION]" and move on
5. **If contradicted** — flag it explicitly

---

## Example: Bad vs Good Citation

### ❌ Bad (hallucination-prone)
```
The ROM mechanism was first proposed by Bulanov et al. [Phys. Plasmas 1, 745 (1994)],
who showed that the Doppler shift from an oscillating plasma mirror generates harmonics.
```
(Problem: Did I actually read this? Can I point to the specific passage? What exactly did Bulanov show?)

### ✅ Good (verified, DOI-based)
```
The ROM concept was first proposed to explain PIC simulation results.
— doi: 10.1063/1.870766
  [KB: /home/zhiping/knowledge_base/paper/1994/1994--Interaction of an ultrashort...]
  Abstract: "We interpret it as due to the Doppler effect produced by a reflecting
  charge sheet, formed in a narrow region at the plasma boundary, oscillating under
  the action of the relativistically strong laser pulse."
```
(Verified: DOI found via search.py, KB path confirmed, exact quote from abstract)
