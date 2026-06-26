---
title: PIC Codes for Relativistic HHG
created: 2026-06-25
updated: 2026-06-25
type: entity
tags: [pic-code, simulation, computational-physics]
---

# PIC Codes for Relativistic HHG

## Overview

Particle-in-Cell (PIC) codes are the primary computational tool for studying relativistic laser-plasma interactions and HHG. Several codes are used in the literature covered by our knowledge base.

## EPOCH

### Description
- **Full name**: Extendable PIC Open Collaboration
- **Origin**: UK EPSRC funded project
- **Type**: Open-source, massively parallel
- **Capabilities**: 1D/2D/3D, relativistic, QED modules

### Usage in Literature
- **Edwards thesis**: All scaling law simulations
- **Edwards & Mikhailova 2016**: Waveform optimization (genetic algorithm)
- **Edwards et al. 2020**: Thin-foil HHG simulations

### Key Features
- High resolution capability (λ/600 used by Edwards)
- Boosted frame for oblique incidence (Bourdier method)
- Particle tracking for trajectory analysis
- Flexible diagnostic output

### Limitations
- Standard FDTD solver has numerical dispersion
- High-resolution simulations computationally expensive

## Smilei

### Description
- **Full name**: Smilei (no acronym)
- **Origin**: CEA-LIDYL collaboration
- **Type**: Open-source, massively parallel
- **Capabilities**: 2D/3D, relativistic, QED, ionization

### Usage in Literature
- **Timmis et al. 2026**: Efficiency-optimized HHG (Nature paper)
- **CEA-LIDYL group**: Most of their recent work

### Key Features
- Bouchard solver for reduced numerical dispersion
- Optimized for exascale architectures
- Coupled with PICSAR library for performance
- High-resolution capability (512 cells/λ used)

### Advantages for HHG
- Better accuracy for Doppler harmonics in vacuum
- Reduced artificial numerical noise
- Enables 3D simulations at high resolution

## WarpX

### Description
- **Full name**: WarpX
- **Origin**: LBNL (Lawrence Berkeley National Laboratory)
- **Type**: Open-source, AMR-capable
- **Capabilities**: 3D, relativistic, exascale optimized

### Usage in Literature
- **Vincenti et al. 2023**: CRM simulations
- **CEA-LIDYL**: 3D plasma mirror simulations

### Key Features
- Coupled with PICSAR library
- Pseudo-spectral solver option
- Exascale architecture optimization
- AMR for multi-scale problems

## BOPS

### Description
- **Full name**: Berkeley Optics Plasma Simulator
- **Origin**: UC Berkeley / Pukhov group
- **Type**: Research code
- **Capabilities**: 1D/2D, relativistic

### Usage in Literature
- **Edwards thesis**: Cross-validation with EPOCH
- **Edwards et al. 2014**: Two-color HHG simulations

### Key Features
- Boosted frame implementation
- Efficient for 1D parameter scans
- Used for genetic algorithm optimization

## picwig

### Description
- **Origin**: Queen's University Belfast
- **Type**: Research code
- **Capabilities**: 1D

### Usage in Literature
- **Cousens et al. 2020**: CSE trajectory analysis

### Key Features
- Detailed particle tracking
- Used for trajectory visualization
- Efficient for single-parameter studies

## Code Comparison for HHG Research

| Code | Dimensions | Solver | Key Strength | Key Paper |
|------|------------|--------|--------------|-----------|
| EPOCH | 1/2/3D | FDTD | Flexibility, open-source | Edwards 2016 |
| Smilei | 2/3D | Bouchard | Accuracy, exascale | Timmis 2026 |
| WarpX | 3D | Pseudo-spectral | 3D capability | Vincenti 2023 |
| BOPS | 1/2D | FDTD | Speed, validation | Edwards 2014 |
| picwig | 1D | FDTD | Trajectory analysis | Cousens 2020 |

## Best Practices for HHG Simulations

### Resolution Requirements
- Spatial: ≥ 256 cells/λ for harmonics up to ~100ω₀
- Temporal: ≥ 512 steps/cycle for resolved harmonics
- Higher resolution needed for CHF studies (512+ cells/λ)

### Particle Count
- Minimum: 50-100 particles/cell for converged spectra
- Higher for detailed trajectory analysis (500+ particles/cell)

### Boundary Conditions
- Silver-Müller for open boundaries
- Perfectly matched layers (PML) for some codes

### Diagnostics
- Field snapshots for near-field analysis
- Spectral diagnostics for harmonic efficiency
- Particle tracking for trajectory studies

## Links

- [[scaling-laws]] — Results from PIC simulations
- [[waveform-engineering]] — Genetic algorithm optimization
- [[efficiency-optimization]] — Simulation-experiment comparison
- [[cea-lidyl-group]] — Smilei developers
