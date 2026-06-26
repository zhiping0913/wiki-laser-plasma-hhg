---
title: Target Types Comparison — Semi-infinite, Thin Foil, Double Foil
created: 2026-06-25
updated: 2026-06-25
type: comparison
tags: [target, thin-foil, double-foil, semi-infinite, comparison]
sources:
  - path: /home/zhiping/knowledge_base/paper/2020/2020--Electron-Nanobunch-Width-Dominated Spectral Power Law for Relativistic Harmonic Generation from Ultrathin Foils
    doi: 10.1103/PhysRevLett.124.185004
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2018/2018--Coherent synchrotron emission in transmission with double foil target
    doi: 10.1088/1361-6587/aaa57d
    read: true
    sections: [1-5]
  - path: /home/zhiping/knowledge_base/paper/2019/2019--Enhancement of the surface emission at the fundamental frequency and the transmitted high-order harmonics by pre-structured targets
    doi: 10.1017/hpl.2019.20
    read: true
    sections: [1-2]
---

# Target Types Comparison

## Overview

Different target geometries offer distinct advantages for relativistic HHG. The choice depends on the application requirements: efficiency, photon energy, spatial quality, or pulse isolation.

## Semi-Infinite Targets

### Description
- Bulk solid targets (d >> λ)
- Typical materials: fused silica, silicon, metals
- Density: N = 100-1000 n_c

### Characteristics

| Property | Value/Range |
|----------|-------------|
| Optimal a₀/N | 0.2-0.5 |
| Power-law p | 1.5 ln(a₀/N) (Edwards) |
| Cutoff | ω_b = λ/2Δ (bunch-width limited) |
| Efficiency | High (when optimized) |
| Spatial quality | Good (flat targets) |
| Isolation | Difficult (multiple cycles) |

### Advantages
- Well-understood physics
- High absolute efficiency possible
- Good spatial coherence
- Easy to fabricate

### Disadvantages
- Requires few-cycle pulses for isolation
- Gradient sensitive
- No transmission harmonics

### Optimal Conditions
- L/λ ≈ 0.05-0.15 (preplasma)
- High contrast laser
- a₀/N ≈ 0.2-0.5

## Thin Foil Targets

### Description
- Nanometer-scale foils (d ~ 10-100 nm)
- Can be freestanding or supported
- Typical materials: diamond-like carbon, silicon nitride

### Characteristics

| Property | Value/Range |
|----------|-------------|
| Optimal S·D | 0.1-0.2 |
| Power-law p | 10/3 (bunch-width dominated) |
| Cutoff | ω_γ = √8α · γ³ |
| Efficiency | Higher than semi-infinite (for moderate a₀) |
| Spatial quality | Good |
| Isolation | Possible (transmission) |

### Advantages
- Higher efficiency for moderate a₀ (1-40)
- Transmission harmonics available
- Tunable effective density (via thickness)
- Single attosecond pulse possible

### Disadvantages
- Fabrication challenge (nm-scale)
- Limited to moderate a₀ for optimal efficiency
- Coulomb explosion limits duration
- More complex dynamics

### Key Scaling
The characteristic parameter S·D describes effective thickness:

**η = f(ND/a₀)**

For S·D < 0.1: efficiency curves collapse onto single line.

— doi: 10.1103/PhysRevLett.124.185004 [KB: .../paper.md]
  "for S · D < 0.1, the efficiency curves collapse onto a single line"

## Double Foil Targets

### Description
- Two thin foils separated by vacuum gap
- First foil: ultrathin (d₁ ~ 10 nm)
- Gap: 0.125-0.25 λ
- Second foil: thicker (d₂ ~ 100 nm)

### Characteristics

| Property | Value/Range |
|----------|-------------|
| Optimal gap | 0.125-0.25 λ |
| Power-law p | CSE-like (4/3 per electron) |
| Cutoff | > 2000ω₀ (enhanced) |
| Efficiency | Very high |
| Spatial quality | Moderate (2D effects) |
| Isolation | Natural (single pulse) |

### Advantages
- Single attosecond pulse in transmission
- High photon energy (keV)
- High γ_x (≈ 9)
- Natural isolation mechanism

### Disadvantages
- Fabrication challenge (precise gap)
- High contrast laser required
- Complex alignment
- Limited experimental demonstrations

### Key Physics
1. Electrons blown out from first foil
2. Accelerated through vacuum gap
3. Self-compressed into dense nanobunch
4. Interacts with reflected laser from second foil
5. Single attosecond pulse emitted
6. Nanobunch disperses when hitting second foil

— doi: 10.1088/1361-6587/aaa57d [KB: .../paper.md]
  "the dense electron nanobunch is formed by the electrons blown out from the first ultrathin foil"

## Pre-Structured Targets

### Description
- Periodic surface structures (gratings)
- Structure period ≈ λ (for SPW excitation)
- Can be on front or rear surface

### Characteristics

| Property | Value/Range |
|----------|-------------|
| Enhancement | ~100× in transmitted energy |
| Mechanism | Surface plasma wave excitation |
| Harmonics | Enhanced via SPW coupling |
| Complexity | Higher fabrication |

### Advantages
- Dramatic enhancement of transmitted harmonics
- Can control SPW excitation
- Compatible with other optimizations

### Disadvantages
- Complex fabrication
- Limited to specific geometries
- Not yet widely demonstrated

— doi: 10.1017/hpl.2019.20 [KB: .../paper.md]
  "the transmitted laser energy behind the pre-structured target is increased by about two orders of magnitude"

## Comparison Summary

| Target | p | Efficiency | Isolation | Photon Energy | Complexity |
|--------|---|------------|-----------|---------------|------------|
| Semi-infinite | 1.5 ln(a₀/N) | High (optimized) | Difficult | Moderate | Low |
| Thin foil | 10/3 | Higher (moderate a₀) | Possible | Moderate | Medium |
| Double foil | ~4/3 | Very high | Natural | High (keV) | High |
| Pre-structured | Variable | Enhanced | Depends | Moderate | High |

## Application Guide

### For Maximum Efficiency
- Semi-infinite with optimal gradient
- Or thin foil for moderate a₀

### For Isolated Attosecond Pulses
- Double foil (transmission)
- Or semi-infinite with gating techniques

### For High Photon Energy
- Double foil (keV capable)
- Or semi-infinite with high a₀

### For CHF Applications
- Semi-infinite (proven in Timmis 2026)
- Pre-shaped targets for curvature control

## Links

- [[scaling-laws]] — How efficiency varies with parameters
- [[double-foil-target]] — Detailed double-foil physics
- [[efficiency-optimization]] — Optimization strategies
- [[preplasma-scale-length]] — Gradient effects
