---
title: Gemini Laser — Rutherford Appleton Laboratory
created: 2026-06-25
updated: 2026-06-25
type: entity
tags: [laser-facility, uk, pw-class, gemini]
---

# Gemini Laser — Rutherford Appleton Laboratory

## Overview

The Gemini laser at the Central Laser Facility (CLF), Rutherford Appleton Laboratory (RAL), UK, is a high-power Ti:sapphire laser system used for relativistic laser-plasma experiments, including the breakthrough HHG efficiency demonstration in 2026.

## Specifications

### Main Parameters
- **Peak power**: ~1 PW (5 J in 50 fs)
- **Pulse duration**: 50 ± 5 fs
- **Wavelength**: 800 nm
- **Repetition rate**: 1 shot per minute
- **Polarization**: P-polarization available

### Focusing
- **Focal spot**: ~2 μm FWHM (f/2 parabola)
- **Maximum intensity**: > 10²¹ W/cm²
- **Contrast**: Enhanced with DPM system

### Contrast Enhancement
- **DPM system**: Double plasma mirror
- **Throughput**: ~50%
- **Contrast**: > 10⁸ at >1 ps before peak
- **t_HDR**: 351 ± 25 fs (optimized configuration)

## Key Experiments

### 2026: Efficiency-optimized HHG (Nature)
- First verification of theoretical maximum efficiency
- 0.17% conversion to H12-H47
- 9.5 mJ in harmonic beam
- Critical: DPM rise time optimization

### Experimental Setup
- Polished fused silica targets
- 45° incidence angle, p-polarization
- XUV flat-field spectrometer (300 l/mm grating)
- Aluminium filters (0.2-3 μm)
- CCD detection (Andor DV436)

## DPM System Details

### Configuration
- Two plasma mirrors in series
- Anti-reflection coated substrates (initial)
- Uncoated substrates (optimized)

### Performance Optimization
- **Slow rise time**: t_HDR = 711 fs (coated first PM)
- **Fast rise time**: t_HDR = 351 fs (uncoated first PM)
- **Key insight**: Materials science of coating breakdown

### Prepulse Control
- 25 mm diameter, 3 mm thick fused silica substrate
- Anti-reflection coating on front, high reflectivity on rear
- Inserted in beam path before last mirror
- Timing control: ±25 fs

## Historical HHG Experiments at RAL

### 2006-2007: Dromey et al.
- First HHG scaling law measurements
- Cutoff frequency verification (γ³)
- Vulcan laser facility

### 2009: Diffraction-limited harmonics
- Spatial coherence demonstration
- Dromey et al., Nat. Phys.

## Links

- [[belfast-dromey-group]] — Primary user group
- [[efficiency-optimization]] — Breakthrough experiment
- [[preplasma-scale-length]] — DPM controls gradient
- [[smilei-pic-code]] — PIC code used for simulations
