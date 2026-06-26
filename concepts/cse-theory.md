---
title: CSE Theory — Coherent Synchrotron Emission
created: 2026-06-25
updated: 2026-06-25
type: concept
tags: [hhg, cse, nanobunching, synchrotron, relativistic-plasma]
sources:
  - path: /home/zhiping/knowledge_base/paper/2011/2011--Ultrarelativistic nanoplasmonics as a route towards extreme-intensity attosecond pulses
    doi: 10.1103/PhysRevE.84.046403
    read: true
    sections: [II, IV]
  - path: /home/zhiping/knowledge_base/paper/2010/2010--Enhanced relativistic harmonics by electron nanobunching
    doi: 10.1063/1.3353050
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2012/2012--Isolated Attosecond Pulses from Laser-Driven Synchrotron Radiation
    doi: 10.1103/PhysRevLett.109.245005
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2012/2012--Coherent synchrotron emission from electron nanobunches formed in relativistic laser–plasma interactions
    doi: 10.1038/nphys2439
    read: true
    sections: [all]
  - path: /home/zhiping/knowledge_base/paper/2013/2013--Femtosecond x rays from laser-plasma accelerators
    doi: 10.1103/RevModPhys.85.1
    read: true
    sections: [II.A]
---

# CSE Theory — Coherent Synchrotron Emission

## Physical Picture

In the CSE model, dense electron nanobunches form at the plasma surface with thickness comparable to or smaller than the harmonic wavelength. These nanobunches are driven into curved (synchrotron-like) trajectories by the combined laser and plasma fields, emitting coherent synchrotron radiation.

The key difference from BGP ROM: the nanobunch is much denser and thinner, enabling **coherent** radiation (intensity ∝ N²_electrons) rather than incoherent (intensity ∝ N_electrons).

— Gonoskov et al., Phys. Rev. E 84, 046403 (2011)
  [KB: /home/zhiping/knowledge_base/paper/2011/2011--Ultrarelativistic nanoplasmonics as a route towards extreme-intensity attosecond pulses]
  §IV: "Depending on the thickness l_s of the radiating electron layer, the radiation can be either coherent, for l_s < τ_g, or incoherent, for l_s > τ_g."

## Historical Development

### 2010: CSE discovered

an der Brügge and Pukhov discovered that under certain parameters, the reflected field amplitude can be much larger than incident (violating BGP assumptions). They found:

1. Dense nanometer-scale electron sheets form at the surface
2. These produce **coherent** synchrotron radiation
3. Spectrum follows I_n ∝ n^{-4/3} (flatter than BGP's n^{-8/3})

— an der Brügge & Pukhov, Phys. Plasmas 17, 033110 (2010)
  [KB: /home/zhiping/knowledge_base/paper/2010/2010--Enhanced relativistic harmonics by electron nanobunching]
  (Full paper read — discovery of CSE mechanism)

### 2011: RES model (complementary)

Gonoskov et al. proposed the Relativistic Electronic Spring (RES) model, explaining when and why nanobunches form:

- **Optimal condition**: S = nₑ/(n_c a₀) ~ 1
- **BGP regime**: S >> 1 (too dense, shallow reflection)
- **Relativistic transparency**: S << 1 (too tenuous)

— Gonoskov et al., Phys. Rev. E 84, 046403 (2011)
  [KB: /home/zhiping/knowledge_base/paper/2011/2011--Ultrarelativistic nanoplasmonics as a route towards extreme-intensity attosecond pulses]
  §II: "The described process and concomitant energy conversion may be represented as a sequence of three stages: (1) pushing of electrons from the surface by the ponderomotive force... (2) backward accelerated motion... (3) radiation of attosecond pulses."
  §IV: Optimal parameters: "θ_g ≈ 62°, S_g ≈ 1/2, and the boundaries 50° < θ < 70°, 1/4 < S < 1"

### 2012: CSE experimental verification

Dromey et al. demonstrated CSE experimentally:
- Measured scaling exponent ~ -1.62 (between CSE's -4/3 and BGP's -8/3)
- Lower than theoretical -4/3 possibly due to not fully achieving coherent condition

— Dromey et al., Nat. Phys. 8, 804–808 (2012)
  [KB: /home/zhiping/knowledge_base/paper/2012/2012--Coherent synchrotron emission from electron nanobunches formed in relativistic laser–plasma interactions]
  (Full paper read — first experimental demonstration of CSE)

### 2012: Synchrotron analysis confirmed

Mikhailova et al. analyzed CSE from the perspective of classical synchrotron radiation theory, confirming that the emission characteristics match the synchrotron conditions.

— Mikhailova et al., Phys. Rev. Lett. 109, 245005 (2012)
  [KB: /home/zhiping/knowledge_base/paper/2012/2012--Isolated Attosecond Pulses from Laser-Driven Synchrotron Radiation]
  (Full paper read — synchrotron analysis of CSE)

## Synchrotron Radiation Physics

From the Liénard-Wiechert potential, the radiation from relativistic electrons has key properties:

— Corde et al., Rev. Mod. Phys. 85, 1 (2013)
  [KB: /home/zhiping/knowledge_base/paper/2013/2013--Femtosecond x rays from laser-plasma accelerators]
  §II.A: "(1) When β̇ = 0, no radiation is emitted. (2) The radiated energy is maximum when β·n→1. (3) Applying a transverse force F⊥β is more efficient than a longitudinal force [by a factor of γ²]."

## CSE Radiation Condition

At the moment of maximum HHG emission:

**v_∥ → max; a_∥ → 0; v_⊥ → 0; a_⊥ → max**

— Mikhailova et al., Phys. Rev. Lett. 109, 245005 (2012)
  [KB: /home/zhiping/knowledge_base/paper/2012/2012--Isolated Attosecond Pulses from Laser-Driven Synchrotron Radiation]
  "During the emission, the following requirements for synchrotron radiation parallel to the reflected laser axis are satisfied: (i) the electron velocity V_z is maximum, (ii) acceleration a_z is zero, (iii) velocity V_y vanishes, and (iv) acceleration a_y is around maximum."

## Coherent vs Incoherent

When the electron bunch size is smaller than the radiation wavelength:
- **Coherent radiation**: All electrons emit in phase, intensity ∝ N²
- **Incoherent radiation**: Random phases, intensity ∝ N

— Gonoskov et al., Phys. Rev. E 84, 046403 (2011)
  [KB: /home/zhiping/knowledge_base/paper/2011/2011--Ultrarelativistic nanoplasmonics as a route towards extreme-intensity attosecond pulses]
  §IV: "For coherent radiation, the bunch thickness must be smaller than the wavelength of the emitted radiation in the rest frame of the bunch."

## Links

- [[rom-theory]] — BGP model, historical predecessor
- [[unified-hhg-picture]] — BGP and CSE are equivalent conditions
- [[scaling-laws]] — Edwards' refinements (bunch-width effect)
- [[double-foil-target]] — CSE in transmission
- [[preplasma-scale-length]] — Optimal gradient for CSE
