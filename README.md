<!--
SPDX-FileCopyrightText: 2026 Sultan Al-Maskari
SPDX-FileCopyrightText: PyPSA-Earth and PyPSA-Eur Authors

SPDX-License-Identifier: AGPL-3.0-or-later
-->

# PyPSA-Oman: An Open, Spatially Resolved Model of Oman’s Electricity Transition to 2050

<p align="left">
  <strong>Developed by Sultan Al-Maskari</strong><br>
  Brandenburg University of Technology Cottbus–Senftenberg
</p>

## Development Status: **Research and Active**

<!-- Replace USERNAME after creating the public GitHub repository. -->

[![License: AGPL v3](https://img.shields.io/badge/License-AGPLv3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Built with PyPSA](https://img.shields.io/badge/Built%20with-PyPSA-2f6fbb.svg)](https://pypsa.org/)
[![Based on PyPSA-Earth](https://img.shields.io/badge/Based%20on-PyPSA--Earth-3a8f5b.svg)](https://github.com/pypsa-meets-earth/pypsa-earth)
[![Workflow](https://img.shields.io/badge/Workflow-Snakemake-039475.svg)](https://snakemake.github.io/)
<!--
[![Repository size](https://img.shields.io/github/repo-size/USERNAME/pypsa-oman)](https://github.com/USERNAME/pypsa-oman)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)
-->

**PyPSA-Oman is an open-source, Python-based electricity-system model developed to study Oman’s transition toward a low-carbon and net-zero power system.**

The model is derived from the [PyPSA-Earth](https://github.com/pypsa-meets-earth/pypsa-earth) workflow and uses the [PyPSA](https://pypsa.org/) optimisation framework. It combines open geospatial, weather, power-plant, demand and technology data with Oman-specific calibration and validation.

PyPSA-Oman represents the national transmission system through **30 clustered AC buses** and uses **2,920 weighted three-hourly snapshots** representing a full year. The current model includes a validated **2024 base-year case**, a preliminary **2030 transition scenario**, and a **2050 zero-direct-emission scenario**.

The model can be used to analyse:

- electricity generation and demand;
- renewable-energy capacity expansion;
- solar and wind integration;
- battery and hydrogen storage;
- direct power-sector CO₂ emissions;
- renewable-energy curtailment;
- transmission reinforcement; and
- long-term electricity-system planning.

PyPSA-Oman is intended to provide a transparent and reproducible foundation for testing alternative assumptions on demand, technology costs, renewable resources, storage, hydrogen conversion and network development in Oman and comparable Gulf electricity systems.

<p align="center">
  <img src="doc/figures/oman_electricity_transmission_network_2024.png" width="72%" alt="Oman Electricity Transmission Network 2024">
</p>

<p align="center">
  <b>Figure:</b> Oman Electricity Transmission Network 2024. Source: Oman Electricity Transmission Company.
</p>

> This official map provides the geographical and infrastructure context for PyPSA-Oman.  
> The model itself uses a simplified, clustered 30-bus AC representation rather than reproducing every individual substation and line shown in the map.

## Current Scenarios

### 2024 — Base-Year Validation

The fixed-capacity 2024 model supplies **46.282 TWh** without virtual load shedding, which is **1.36% above** the official electricity total. Modelled renewable generation is **1.747 TWh**, **6.83% below** the reported value.

### 2030 — Preliminary Transition Scenario

The model produces **21.578 TWh** from solar and wind, equivalent to **42.28% of electricity demand**. Direct emissions fall by **36.0%** from 2024, while renewable curtailment reaches **11.39% of available VRE**.

### 2050 — Zero Direct Generator Emissions

The model supplies all generator output from solar and wind, deploying **58.264 GW of solar PV** and **34.740 GW of onshore wind**. The scenario requires substantial storage, hydrogen conversion and transmission reinforcement.

> The current techno-economic assumptions and annualised cost accounting are still under review. Results should be interpreted as scenario-based planning signals rather than forecasts or construction-ready designs.

## Model Framework

PyPSA-Oman uses:

- [PyPSA](https://github.com/PyPSA/PyPSA) for power-system optimisation;
- [PyPSA-Earth](https://github.com/pypsa-meets-earth/pypsa-earth) for global data preparation and workflow structure;
- [Snakemake](https://github.com/snakemake/snakemake) for workflow management;
- [xarray](https://github.com/pydata/xarray) for labelled multidimensional data;
- [atlite](https://github.com/PyPSA/atlite) and ERA5 data for renewable-resource profiles; and
- Python-based scripts for validation, analysis and visualisation.

## Paper

The model is described in the working paper:

> **Sultan Al-Maskari. _PyPSA-Oman: An Open, Spatially Resolved Model of Oman’s Electricity Transition to 2050._ Working paper, 2026.**

The manuscript includes the model architecture, data sources, validation procedure, scenario definitions, results, limitations and future development priorities.

## Repository Status

This repository is being prepared as a reproducible research release. The public version will include:

- scenario configuration files;
- Oman-specific processed inputs;
- analysis and visualisation scripts;
- solved-network outputs;
- validation results;
- model documentation;
- the working paper; and
- a versioned archive and DOI.

## Related Projects

PyPSA-Oman builds on the open-source work of:

- [PyPSA](https://github.com/PyPSA/PyPSA)
- [PyPSA-Earth](https://github.com/pypsa-meets-earth/pypsa-earth)
- [PyPSA-Eur](https://github.com/PyPSA/pypsa-eur)
- [atlite](https://github.com/PyPSA/atlite)
- [Snakemake](https://github.com/snakemake/snakemake)
- [xarray](https://github.com/pydata/xarray)

## Citation

```bibtex
@article{almaskari_pypsa_oman_2026,
  author      = {Al-Maskari, Sultan},
  title       = {PyPSA-Oman: An Open, Spatially Resolved Model of Oman's Electricity Transition to 2050},
  year        = {2026},
  note        = {Working paper},
  institution = {Brandenburg University of Technology Cottbus--Senftenberg}
}
```

## Image Credit

The transmission-network map displayed above is credited to the **Oman Electricity Transmission Company**.  
Before redistributing the image publicly, confirm that its use in the repository is permitted and retain the source attribution.

## Contact

**Sultan Al-Maskari**  
PhD Researcher, Environmental and Resource Management  
Brandenburg University of Technology Cottbus–Senftenberg  
Email: almassul@b-tu.de  
ORCID: [0009-0003-3913-1411](https://orcid.org/0009-0003-3913-1411)

---

**PyPSA-Oman is an open research initiative for transparent electricity-system analysis in Oman.**
