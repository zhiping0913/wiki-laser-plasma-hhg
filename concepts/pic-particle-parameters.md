---
title: PIC Particle Count — Physically-Meaningful Metrics
created: 2026-07-15
updated: 2026-07-15
type: concept
tags: [pic-simulation, convergence, particle-weight, numerical-parameters]
---

# PIC Particle Count — Beyond "Particles Per Cell"

## Motivation

The standard PIC convention is **macro-particles per cell** (ppc). This is
grid-dependent: ppc=100 with Δx = λ₀/10 is vastly different sampling quality
from ppc=100 with Δx = λ₀/1000, because the cell volume differs by a factor of
10⁶ in 3D.

A physically meaningful alternative that eliminates the grid dependence is:

> **Number of macro-particles per nc·λ₀³** (3D) or **per nc·λ₀** (1D)

where nc is the critical density and λ₀ is the laser wavelength. For λ₀ = 800 nm:
nc ≈ 1.74×10²¹ cm⁻³, so nc·λ₀³ ≈ 8.9×10⁸ real electrons.

## Standard Definition: Particles Per Cell

Almost all PIC literature reports ppc together with spatial resolution
separately. The EPOCH manual (2015 — Contemporary particle-in-cell approach to
laser-plasma modelling, 10.1088/0741-3335/57/11/113001) defines the *particle
weight* as "the number of real particles represented by each simulation
particle":

$$w = \frac{n_0 \cdot V_{\text{cell}}}{\text{ppc}}$$

where V_cell is the physical cell volume. Typical weights for relativistic
laser-plasma simulations range from 10⁶ to 10¹⁴ real electrons per macro-particle.

This is the inverse of what we seek — weight w is "real electrons per
macro-particle", while macro-particles per nc·λ₀³ is "macro-particles per unit
physical volume."

## Proposed Metric: Macro-Particles per nc·λ₀³

### Derivation

For a cubic grid with cell size Δx = λ₀/N (where N = cells/λ):

Real electrons per cell: $n_0 \cdot (\lambda_0/N)^d$ (d = 1, 2, 3)

Macro-particle weight: $w = n_0 (\lambda_0/N)^d / \text{ppc}$

Macro-particles in volume λ₀^d at density n_c:

$$N_d = \frac{n_c \cdot \lambda_0^d}{w} = \text{ppc} \times \frac{n_c}{n_0} \times \left(\frac{\text{cells}}{\lambda}\right)^d$$

### Explicit Forms

| Dimension | Formula | Unit |
|-----------|---------|------|
| 1D | N₁D = ppc × (nc/n₀) × (cells/λ) | macro-particles per nc·λ₀ (per unit area) |
| 2D | N₂D = ppc × (nc/n₀) × (cells/λ)² | macro-particles per nc·λ₀² (per unit length) |
| 3D | N₃D = ppc × (nc/n₀) × (cells/λ)³ | macro-particles per nc·λ₀³ |

### Reference Values from Literature (1D, n₀ = 100 nc)

| Paper | Code | cells/λ | ppc | N₁D | Weight (e⁻/macro) | Purpose |
|-------|------|---------|-----|-----|--------------------|---------|
| Edwards §4.1 | BOPS | 833 | 70 | 583 | 2.4×10¹⁴ | Efficiency scans |
| Edwards §4.3 | EPOCH | 3000 | 500 | 15,000 | 9.3×10¹² | Trajectory analysis |
| Edwards §5 | BOPS | 833 | 150 | 1,250 | 1.1×10¹⁴ | Double plasma mirror |
| 2015 — Self-consistent theory of HHG by relativistic plasma mirror, 10.1103/PhysRevE.92.053108 | custom | 2400 | 300 | 7,200 | 1.9×10¹³ | Model validation |
| 2014 — Optical properties of relativistic plasma mirrors, 10.1038/ncomms4403 | EUTERPE | 1500 | 500 | 7,500 | 1.9×10¹³ | Model validation (1D) |

Edwards thesis: Princeton Dataspace handle 88435/dsp01z316q4466.

Note: Weight is in electrons per macro-particle per unit area (1D).

## Literature Search: Has Anyone Used This?

**No published paper explicitly uses "macro-particles per nc·λ₀³" as a
particle-count definition.** The community universally reports ppc and
resolution separately.

However, several papers discuss the physical meaning of macro-particle sampling
in ways relevant to this metric:

1. **Particle weight** (the inverse of our metric): EPOCH's design paper
   (2015 — Contemporary particle-in-cell approach to laser-plasma modelling,
   10.1088/0741-3335/57/11/113001) defines weight $w$ as real electrons per
   macro-particle and discusses its interpretation and bounds.

2. **Particles per Debye length (N_D)**: The classical physically-meaningful
   PIC metric for thermal plasmas. Langdon (1970, kinetic theory) and Turner
   (2006 — Kinetic properties of particle-in-cell simulations compromised by
   Monte Carlo collisions, 10.1063/1.2180687) discussed convergence in terms of
   $N_D$. But for cold, overdense HHG plasmas, λ_D is often unresolved or
   sub-grid, making the nc·λ₀³ metric more natural.

3. **Kinetic theory of PIC particle weight**: 2022 — Kinetic theory of
   particle-in-cell simulation plasma and the ensemble averaging technique,
   10.1088/1361-6587/ac9016, treats the macro-particle weight δN_a as the
   fundamental sampling parameter in a formal kinetic theory. This is the
   closest theoretical work to our proposal, though it does not use the nc·λ₀³
   unit.

## Practical Usage

The nc·λ₀³ metric is best used as a **convergence diagnostic**, not an input
parameter:

1. Set up simulation with conventional ppc + resolution
2. Compute N₁D (or N₃D) from the formula above
3. Compare to reference ranges to assess sampling quality
4. When comparing results across different resolutions or densities, normalize
   by N₁D to isolate genuine physical effects from sampling artifacts

### Recommended 1D Ranges (n₀ ≈ 100 nc)

| Task | N₁D |
|------|-----|
| Quick exploratory scan | 200 – 500 |
| Efficiency / parameter scan | 500 – 2,000 |
| Spectrum convergence | 2,000 – 5,000 |
| Trajectory / nanobunch analysis | 10,000+ |

These ranges scale linearly with n₀/nc — for n₀ = 400 nc, multiply N₁D by 4.

## Comparison with Particles per Debye Length

For overdense, cold HHG plasmas, the nc·λ₀³ metric is more natural than N_D
because:

1. **λ_D is sub-grid**: For typical overdense plasmas at n₀ = 100 nc with
   T ≈ 100 eV, λ_D ≈ 0.008 λ₀, which is far below the typical cell size
   (Δx ≈ λ₀/500 = 0.002 λ₀). The Debye sphere is poorly resolved.

2. **nc·λ₀³ is the natural plasma scale**: At the critical surface, the laser's
   electromagnetic energy density balances the electron's rest mass energy
   density. The volume nc·λ₀³ corresponds to ~10⁹ electrons — the scale at which
   collective laser-plasma dynamics occur.

3. **Directly comparable across simulations**: N₁D allows direct comparison of
   sampling quality between simulations with different resolutions, densities,
   and dimensionalities.

## Links

- [[scaling-laws]] — Efficiency scans using these simulation parameters
- [[pic-codes]] — PIC code descriptions and resolution requirements
