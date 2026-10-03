# Awesome Meshless CAE [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of CAE tools that work **without a traditional mesh** (meshless / mesh-free / mesh-light): particle methods, lattice Boltzmann, MPM, peridynamics, isogeometric analysis, voxel / immersed boundary, and AI surrogates.

## Contents

- [Particle Methods (SPH / MPS)](#particle-methods-sph--mps)
- [Lattice Boltzmann Method (LBM)](#lattice-boltzmann-method-lbm)
- [Meshfree Solid Mechanics (EFG / Peridynamics / MPM)](#meshfree-solid-mechanics-efg--peridynamics--mpm)
- [Voxel / Immersed Boundary](#voxel--immersed-boundary)
- [Isogeometric Analysis (IGA)](#isogeometric-analysis-iga)
- [AI / Surrogate Models](#ai--surrogate-models)
- [How to Choose](#how-to-choose)
- [Caveats](#caveats)
- [Contributing](#contributing)

Legend: 🆓 Open source (GitHub / GitLab) · 💼 Commercial

## Particle Methods (SPH / MPS)

Best for free surface, splashing, sloshing, lubrication, large deformation.

- 🆓 [DualSPHysics](https://github.com/DualSPHysics/DualSPHysics) - GPU-accelerated SPH solver.
- 🆓 [SPlisHSPlasH](https://github.com/InteractiveComputerGraphics/SPlisHSPlasH) - SPH fluid simulation library.
- 🆓 [PySPH](https://github.com/pypr/pysph) - Python framework for SPH.
- 💼 [Particleworks](https://www.prometech.co.jp/en/) - MPS-based particle solver (Prometech).
- 💼 [Altair nanoFluidX](https://altair.com/nanofluidx) - GPU SPH for powertrain / e-motor lubrication.
- 💼 [LS-DYNA (SPH)](https://www.ansys.com/products/structures/ansys-ls-dyna) - SPH for fluid-structure interaction and high-speed impact.

## Lattice Boltzmann Method (LBM)

Best for external aerodynamics and aeroacoustics on complex geometry with fast pre-processing.

- 🆓 [Palabos](https://gitlab.com/unigespc/palabos) - Parallel lattice Boltzmann solver.
- 🆓 [waLBerla](https://www.walberla.net) - Massively parallel LBM framework.
- 🆓 [OpenLB](https://www.openlb.net) - Open source LBM library.
- 🆓 [Sailfish](https://github.com/sailfish-team/sailfish) - GPU LBM (no longer actively maintained).
- 💼 [Dassault PowerFLOW](https://www.3ds.com/products/simulia/powerflow) - Automotive aerodynamics / aeroacoustics.
- 💼 [Simcenter XFlow](https://plm.sw.siemens.com/en-US/simcenter/fluids-thermal-simulation/xflow/) - LBM CFD (Siemens).

## Meshfree Solid Mechanics (EFG / Peridynamics / MPM)

Best for fracture, crack propagation, soil / granular flow, extreme deformation.

- 🆓 [Peridigm](https://github.com/peridigm/peridigm) - Peridynamics code (Sandia).
- 🆓 [PeriPy](https://github.com/alan-turing-institute/PeriPy) - Python peridynamics.
- 🆓 [Taichi MPM](https://github.com/yuanming-hu/taichi_mpm) - High-performance MPM on Taichi.
- 🆓 [Taichi](https://github.com/taichi-dev/taichi) - Parallel programming language used by many MPM / particle codes.
- 🆓 [Anura3D](https://www.anura3d.com) - MPM for geomechanics.
- 💼 [LS-DYNA (EFG)](https://www.ansys.com/products/structures/ansys-ls-dyna) - Element-Free Galerkin for large-deformation solids.

## Voxel / Immersed Boundary

Best for fast early-stage design evaluation straight from CAD.

- 💼 [Altair Inspire](https://altair.com/inspire) - Simulation-driven design from CAD geometry.
- 💼 Ansys Discovery - Real-time simulation (see Ansys website).

## Isogeometric Analysis (IGA)

Uses CAD NURBS geometry directly, removing geometric approximation from meshing.

- 🆓 [igakit](https://github.com/dalcinl/igakit) - Python toolkit for IGA.
- 🆓 [GeoPDEs](https://github.com/rafavzqz/geopdes) - Octave/MATLAB IGA package.
- 🆓 [G+Smo](https://github.com/gismo/gismo) - C++ IGA library.
- 💼 [LS-DYNA (IGA)](https://www.ansys.com/products/structures/ansys-ls-dyna) - Isogeometric elements.

## AI / Surrogate Models

Instant prediction after training. Training data usually comes from conventional mesh-based CAE.

- 🆓 [NVIDIA PhysicsNeMo](https://github.com/NVIDIA/physicsnemo) - Physics-ML framework.
- 🆓 [neuraloperator](https://github.com/neuraloperator/neuraloperator) - Fourier Neural Operators and related models.
- 🆓 [DeepXDE](https://github.com/lululxvi/deepxde) - Physics-informed neural networks (PINNs).
- 💼 [Ansys SimAI](https://www.ansys.com/products/simai) - Cloud AI surrogate.
- 💼 [Altair physicsAI](https://altair.com/physicsai) - AI surrogate inside HyperWorks.
- 💼 [Neural Concept](https://www.neuralconcept.com) - Engineering deep learning platform.

## How to Choose

| Need | Method |
|------|--------|
| Large deformation, free surface, splash | SPH / MPS |
| External aero, aeroacoustics | LBM |
| Fracture, crack growth | Peridynamics / EFG |
| Soil, granular, extreme deformation | MPM |
| Fast early-stage design | Voxel / AI surrogate |
| Certified structural strength | Conventional FEM (still mainstream) |

## Caveats

- Meshless saves pre-processing, but boundary conditions, particle count (cost), and validation remain challenges.
- Many OSS research codes lack verified, standards-compliant validation; commercial tools are the norm in production automotive CAE.
- Some OSS projects are no longer maintained. Check the last commit before adopting.
- Links may change. Please open a PR if you find a broken one.

## Contributing

Pull requests are welcome. Please add one tool per line with a short description and mark it 🆓 or 💼.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
