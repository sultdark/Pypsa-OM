# Data

This folder contains small, curated Oman-specific input files required to understand or reproduce the public model setup.

## Included input

- `powerplants.csv` — processed generation fleet used across the 2024, 2030 and 2050 model cases. Scenario-year and retirement filters determine which records are active in each run.
- `licenses/LICENSE_EEZ_v11.txt` — licence, terms of use and citation information for Marine Regions EEZ data.

Large automatically downloaded or generated datasets are not stored directly in this repository. These include ERA5 cutouts, OpenStreetMap extracts, intermediate resources and full solved-network files. They should be recreated through the PyPSA-Earth workflow or distributed separately in a versioned research archive.

The public model uses 2013 ERA5 weather profiles and a processed Oman power-plant fleet. Users should review the source licences and cite the original data providers.
