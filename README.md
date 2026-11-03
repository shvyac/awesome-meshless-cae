# Awesome Meshless CAE [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**English** | [日本語](README.ja.md)

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
- [Related Lists](#related-lists)
- [Contributing](#contributing)
- [shvyac's awesome lists](#shvyacs-awesome-lists)

Legend: 🆓 Open source (GitHub / GitLab) · 💼 Commercial

⭐ badges show live GitHub star counts (via shields.io); release badges show the date of the latest GitHub release (YYYY/MM/DD, as of the last refresh); last-commit badges show live commit activity (via shields.io).

## Particle Methods (SPH / MPS)

Best for free surface, splashing, sloshing, lubrication, large deformation.

- 🆓 [DualSPHysics](https://github.com/DualSPHysics/DualSPHysics) ![GitHub stars](https://img.shields.io/github/stars/DualSPHysics/DualSPHysics?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/DualSPHysics/DualSPHysics?style=flat) - GPU-accelerated SPH solver.
- 🆓 [SPlisHSPlasH](https://github.com/InteractiveComputerGraphics/SPlisHSPlasH) ![GitHub stars](https://img.shields.io/github/stars/InteractiveComputerGraphics/SPlisHSPlasH?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/InteractiveComputerGraphics/SPlisHSPlasH?style=flat) - SPH fluid simulation library.
- 🆓 [PySPH](https://github.com/pypr/pysph) ![GitHub stars](https://img.shields.io/github/stars/pypr/pysph?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2022%2F03%2F01-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/pypr/pysph?style=flat) - Python framework for SPH.
- 🆓 [SPHinXsys](https://github.com/Xiangyu-Hu/SPHinXsys) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/Xiangyu-Hu/SPHinXsys?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F12-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Xiangyu-Hu/SPHinXsys?style=flat) - C++ multi-physics SPH library (fluid-structure interaction, solid dynamics, SYCL GPU).
- 💼 [Particleworks](https://prometech.co.jp/en/) - MPS-based particle solver (Prometech).
- 💼 [Altair nanoFluidX](https://help.altair.com/hwcfdsolvers/nfx/topics/nanofluidx/overview_nanofluidx_r.htm) - GPU SPH for powertrain / e-motor lubrication (Altair, now part of Siemens).
- 💼 [LS-DYNA (SPH)](https://www.ansys.com/products/structures/ansys-ls-dyna) - SPH for fluid-structure interaction and high-speed impact.

## Lattice Boltzmann Method (LBM)

Best for external aerodynamics and aeroacoustics on complex geometry with fast pre-processing.

- 🆓 [Palabos](https://gitlab.com/unigespc/palabos) - Parallel lattice Boltzmann solver.
- 🆓 [waLBerla](https://www.walberla.net) - Massively parallel LBM framework.
- 🆓 [OpenLB](https://www.openlb.net) - Open source LBM library.
- 🆓 [Sailfish](https://github.com/sailfish-team/sailfish) ![GitHub stars](https://img.shields.io/github/stars/sailfish-team/sailfish?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/sailfish-team/sailfish?style=flat) - GPU LBM (no longer actively maintained).
- 🆓 [XLB](https://github.com/Autodesk/XLB) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/Autodesk/XLB?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F01%2F12-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Autodesk/XLB?style=flat) - Differentiable lattice Boltzmann in Python (JAX / NVIDIA Warp) for physics-based ML (Autodesk).
- 🆓 [FluidX3D](https://github.com/ProjectPhysX/FluidX3D) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/ProjectPhysX/FluidX3D?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F05-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/ProjectPhysX/FluidX3D?style=flat) - Fast, memory-efficient LBM on any GPU / CPU via OpenCL (source-available; free for non-commercial use only).
- 💼 [Dassault PowerFLOW](https://www.3ds.com/products/simulia/powerflow) - Automotive aerodynamics / aeroacoustics.
- 💼 [Simcenter XFlow](https://plm.sw.siemens.com/en-US/simcenter/fluids-thermal-simulation/xflow/) - LBM CFD (Siemens).

## Meshfree Solid Mechanics (EFG / Peridynamics / MPM)

Best for fracture, crack propagation, soil / granular flow, extreme deformation.

- 🆓 [Peridigm](https://github.com/peridigm/peridigm) ![GitHub stars](https://img.shields.io/github/stars/peridigm/peridigm?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/peridigm/peridigm?style=flat) - Peridynamics code (Sandia).
- 🆓 [PeriPy](https://github.com/alan-turing-institute/PeriPy) ![GitHub stars](https://img.shields.io/github/stars/alan-turing-institute/PeriPy?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/alan-turing-institute/PeriPy?style=flat) - Python peridynamics (no longer actively maintained; last commit 2021).
- 🆓 [Taichi MPM](https://github.com/yuanming-hu/taichi_mpm) ![GitHub stars](https://img.shields.io/github/stars/yuanming-hu/taichi_mpm?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/yuanming-hu/taichi_mpm?style=flat) - High-performance MPM on Taichi.
- 🆓 [Taichi](https://github.com/taichi-dev/taichi) ![GitHub stars](https://img.shields.io/github/stars/taichi-dev/taichi?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F07%2F31-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/taichi-dev/taichi?style=flat) - Parallel programming language used by many MPM / particle codes.
- 🆓 [CB-Geo MPM](https://github.com/cb-geo/mpm) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/cb-geo/mpm?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/cb-geo/mpm?style=flat) - High-performance parallel material point method (C++) for geomechanics.
- 🆓 [Anura3D](https://www.anura3d.com) - MPM for geomechanics.
- 💼 [LS-DYNA (EFG)](https://www.ansys.com/products/structures/ansys-ls-dyna) - Element-Free Galerkin for large-deformation solids.

## Voxel / Immersed Boundary

Best for fast early-stage design evaluation straight from CAD.

- 💼 [Altair Inspire](https://altair.com/inspire) - Simulation-driven design from CAD geometry (Altair, now part of Siemens).
- 💼 [Ansys Discovery](https://www.ansys.com/products/3d-design/ansys-discovery) - Real-time simulation with interactive modeling.

## Isogeometric Analysis (IGA)

Uses CAD NURBS geometry directly, removing geometric approximation from meshing.

- 🆓 [igakit](https://github.com/dalcinl/igakit) ![GitHub stars](https://img.shields.io/github/stars/dalcinl/igakit?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/dalcinl/igakit?style=flat) - Python toolkit for IGA.
- 🆓 [GeoPDEs](https://github.com/rafavzqz/geopdes) ![GitHub stars](https://img.shields.io/github/stars/rafavzqz/geopdes?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F11%2F28-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/rafavzqz/geopdes?style=flat) - Octave/MATLAB IGA package.
- 🆓 [G+Smo](https://github.com/gismo/gismo) ![GitHub stars](https://img.shields.io/github/stars/gismo/gismo?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/gismo/gismo?style=flat) - C++ IGA library.
- 💼 [LS-DYNA (IGA)](https://www.ansys.com/products/structures/ansys-ls-dyna) - Isogeometric elements.

## AI / Surrogate Models

Instant prediction after training. Training data usually comes from conventional mesh-based CAE.

- 🆓 [NVIDIA PhysicsNeMo](https://github.com/NVIDIA/physicsnemo) ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/physicsnemo?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F11-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/NVIDIA/physicsnemo?style=flat) - Physics-ML framework.
- 🆓 [neuraloperator](https://github.com/neuraloperator/neuraloperator) ![GitHub stars](https://img.shields.io/github/stars/neuraloperator/neuraloperator?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F10%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/neuraloperator/neuraloperator?style=flat) - Fourier Neural Operators and related models.
- 🆓 [DeepXDE](https://github.com/lululxvi/deepxde) ![GitHub stars](https://img.shields.io/github/stars/lululxvi/deepxde?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F02-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/lululxvi/deepxde?style=flat) - Physics-informed neural networks (PINNs).
- 💼 [Ansys SimAI](https://www.ansys.com/products/ai/simai) - Cloud AI surrogate (Ansys, now part of Synopsys).
- 💼 [Altair physicsAI](https://altair.com/physicsai) - AI surrogate inside HyperWorks (Altair, now part of Siemens).
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

## Related Lists

Other curated lists on CAE and simulation (none focus on meshless methods specifically):

- [qd-cae/awesome-CAE](https://github.com/qd-cae/awesome-CAE) ![GitHub stars](https://img.shields.io/github/stars/qd-cae/awesome-CAE?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/qd-cae/awesome-CAE?style=flat) - CAE frameworks, libraries and software in general.
- [kimimgo/awesome-ai-cae](https://github.com/kimimgo/awesome-ai-cae) ![GitHub stars](https://img.shields.io/github/stars/kimimgo/awesome-ai-cae?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/kimimgo/awesome-ai-cae?style=flat) - AI-ready CAE tools (CFD, FEA, SPH, DEM, neural operators, PINNs, MCP servers).
- [anlijun/awesome-CAE-software](https://github.com/anlijun/awesome-CAE-software) ![GitHub stars](https://img.shields.io/github/stars/anlijun/awesome-CAE-software?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/anlijun/awesome-CAE-software?style=flat) - CAE software across the full workflow, including AI.
- [shvyac/awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shvyac/awesome-cad-cae?style=flat) - CAD / CAE topics (same maintainer).
- [tkoyama010/awesome-lattice-boltzmann-method](https://github.com/tkoyama010/awesome-lattice-boltzmann-method) ![GitHub stars](https://img.shields.io/github/stars/tkoyama010/awesome-lattice-boltzmann-method?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/tkoyama010/awesome-lattice-boltzmann-method?style=flat) - Lattice Boltzmann method resources (no description yet).
- [tkoyama010/awesome-open-source-cae](https://github.com/tkoyama010/awesome-open-source-cae) ![GitHub stars](https://img.shields.io/github/stars/tkoyama010/awesome-open-source-cae?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/tkoyama010/awesome-open-source-cae?style=flat) - Open source CAE (not updated since 2023).

## Contributing

Pull requests are welcome. Please add one tool per line with a short description and mark it 🆓 or 💼. See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

## shvyac's awesome lists

All curated lists maintained by [shvyac](https://github.com/shvyac):

- [awesome-AI-Powered-Executive-Dashboards](https://github.com/shvyac/awesome-AI-Powered-Executive-Dashboards) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-AI-Powered-Executive-Dashboards?style=flat&label=%E2%AD%90)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat&label=%E2%AD%90)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat&label=%E2%AD%90)
- [awesome-azure-ai-dynamics365-security](https://github.com/shvyac/awesome-azure-ai-dynamics365-security) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-azure-ai-dynamics365-security?style=flat&label=%E2%AD%90)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat&label=%E2%AD%90)
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat&label=%E2%AD%90)
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat&label=%E2%AD%90)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat&label=%E2%AD%90)
- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat&label=%E2%AD%90)
- [awesome-hpc](https://github.com/shvyac/awesome-hpc) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hpc?style=flat&label=%E2%AD%90)
- [awesome-iso27001-isms-tools](https://github.com/shvyac/awesome-iso27001-isms-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-iso27001-isms-tools?style=flat&label=%E2%AD%90)
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat&label=%E2%AD%90)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat&label=%E2%AD%90)
- [awesome-mcp-ai](https://github.com/shvyac/awesome-mcp-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-mcp-ai?style=flat&label=%E2%AD%90)
- [awesome-meshless-cae](https://github.com/shvyac/awesome-meshless-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat&label=%E2%AD%90)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat&label=%E2%AD%90)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat&label=%E2%AD%90)
- [awesome-quantum](https://github.com/shvyac/awesome-quantum) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-quantum?style=flat&label=%E2%AD%90)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat&label=%E2%AD%90)
- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat&label=%E2%AD%90)
