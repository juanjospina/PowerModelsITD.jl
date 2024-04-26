# PowerModelsITD.jl

<img src="https://lanl-ansi.github.io/PowerModelsITD.jl/dev/assets/logo.svg" align="left" width="200" alt="PowerModelsITD logo">

[![CI](https://github.com/lanl-ansi/PowerModelsITD.jl/workflows/CI/badge.svg)](https://github.com/lanl-ansi/PowerModelsITD.jl/actions?query=workflow%3ACI) [![Documentation](https://github.com/lanl-ansi/PowerModelsITD.jl/workflows/Documentation/badge.svg)](https://lanl-ansi.github.io/PowerModelsITD.jl/stable/)

`PowerModelsITD.jl` is an extention package based on [PowerModels.jl](https://github.com/lanl-ansi/PowerModels.jl) and [PowerModelsDistribution.jl](https://github.com/lanl-ansi/PowerModelsDistribution.jl) for steady-state Integrated Transmission-Distribution (ITD) power network optimization. It is designed to enable the computational evaluation of emerging power network formulations and algorithms in a common platform. The code is engineered to decouple problem specifications (e.g. Power Flow, Optimal Power Flow, ...) from power network formulations (e.g. AC polar, AC rectangular, linear-approximation, SOC-relaxation, ...) on both transmission and distribution system(s). Thus, enabling the definition of a wide variety of ITD power network formulations and their comparison on common problem specifications.

## Core Problem Specifications

- Integrated T&D Power Flow (pfitd)
- Integrated T&D Optimal Power Flow (opfitd)
- Integrated T&D Optimal Power Flow with storage costs (opfitd_storage)
- Integrated T&D Optimal Power Flow with on-load tap-changer (opfitd_oltc)
- Integrated T&D Optimal power flow at transmission and minimum load delta at distribution system (opfitd_dmld)

## Core Network Formulations

**Note**: _left_ is the formulation used to model the transmission system - _right_ is the unbalanced formulation used to model the distribution system(s).

- Nonlinear
  - ACP-ACPU
  - ACR-ACRU
  - IVR-IVRU
- Relaxations
  - SOCBF-SOCUBF (W-space)
- Linear Approximations
  - NFA-NFAU
  - DCP-DCPU
- Hybrid
  - ACR-FOTRU (First-Order Taylor Rectangular)
  - ACP-FOTPU (First-Order Taylor Polar)
  - ACR-FBSU (Forward-Backward Sweep)
  - SOCBF-LinDist3Flow
  - BFA-LinDist3Flow

## Network Data Formats

- **Transmission**: Matpower ".m" and PTI ".raw" files (PSS(R)E v33 specification)
- **Distribution**: OpenDSS ".dss" files
- **Boundary**: JSON ".json" files

## Documentation

Please see our [online documentation](https://lanl-ansi.github.io/PowerModelsITD.jl/stable/) for information about how to install and use `PowerModelsITD`. Local documentation can also be generated by following instructions in `./docs`.

## Examples/Tutorials

Examples of how to use `PowerModelsITD` can be found in the main documentation in the [Beginners Guide](https://lanl-ansi.github.io/PowerModelsITD.jl/stable/tutorials/BeginnersGuide.html).

## Development

Community-driven development and enhancement of `PowerModelsITD` is welcomed and encouraged.
Please feel free to fork this repository and share your contributions to the main branch with a pull request.
When submitting a PR, please keep in mind the code quality requirements and scope of `PowerModelsITD` before preparing a contribution.
See [CONTRIBUTING.md] for code contribution guidelines.

## Acknowledgments

This code has been developed with the support of the Grant: "Optimized Resilience for Distribution and Transmission Systems" funded by the U.S. Department of Energy (DOE) Office of Electricity (OE) Advanced Grid Modeling (AGM) Research Program under program manager Ali Ghassemian. The research work conducted at Los Alamos National Laboratory is done under the auspices of the National Nuclear Security Administration of the U.S. Department of Energy under Contract No. 89233218CNA000001. The primary developers are Juan Ospina (@juanjospina) and David Fobes (@pseudocubic).

## Citing PowerModelsITD

If you find `PowerModelsITD` useful for your work, we kindly request that you cite the following [publication](https://doi.org/10.1109/TPWRS.2023.3234725):

```bibtex
@article{ospina2023modeling,
  author={Ospina, Juan and Fobes, David M. and Bent, Russell and Wächter, Andreas},
  journal={IEEE Transactions on Power Systems},
  title={Modeling and Rapid Prototyping of Integrated Transmission-Distribution OPF Formulations with PowerModelsITD.jl},
  year={2023},
  volume={},
  number={},
  pages={1-14},
  doi={10.1109/TPWRS.2023.3234725}}
```

## License

This code is provided under a BSD license as part of the Multi-Infrastructure Control and Optimization Toolkit (MICOT) project, C15024.
