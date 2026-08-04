# NISAR InSAR–RTK/GNSS Validation for the Chilpancingo Landslide

This repository is a material based on the Technical Note *Seismic Deformation Analysis of a Landslide in Chilpancingo, Guerrero, Mexico, using NISAR Observations*.

## Scientific objective

The workflow derives line-of-sight displacement from six NISAR L-band Level-2 Geocoded Single Look Complex (GSLC) acquisitions, combines ascending and descending observations to estimate vertical and east–west displacement, and compares the results with measurements transcribed from a previously published 38-station RTK-GNSS campaign.

## Important scope statement

The RTK-GNSS campaign (2022–2023) and the NISAR observations (2025–2026) are not contemporaneous. The current comparison can support an assessment of directional and historical kinematic consistency, but it must not be described as direct event-time ground-truth validation without additional evidence.

## Repository structure

- `notebooks/`: portable working notebooks; untouched originals are in `notebooks/archived/`.
- `src/`: reusable configuration, input-validation, and geometry utilities.
- `scripts/`: data and notebook checks.
- `Data/`: data documentation, manifest, RTK tables, ROI files, and derived products. Official NISAR HDF5 files are not distributed.
- `Results/`: figures used in the manuscript draft, tables, metrics, and provenance records.
- `docs/`: manuscript draft, audit notes, and traceability records.
- `tests/`: lightweight tests that do not require full NISAR products.

## Data acquisition

1. Register for NASA Earthdata access and download the six exact NISAR products listed in `Data/data_manifest.csv` through the ASF search interface.
2. Preserve the complete official filenames.
3. Place the files under `Data/NISAR/products/`, or copy `config/config.example.yml` to `config/config.yml` and set a different local directory.
4. Run `python scripts/verify_data.py`.

## RTK-GNSS source

The 38-station values are transcribed from Vázquez-Jiménez et al. (2025), *Spatial assessment of landslide risk using GNSS-based displacement analysis and a resident vulnerability index in northwestern Chilpancingo, Guerrero, Mexico*, DOI: `10.1007/s10346-025-02583-y`. They are published measurements, not raw receiver observations.

## Reproduction workflow

Run `notebooks/01_nisar_interferometric_processing.ipynb` first and `notebooks/02_insar_rtk_validation.ipynb` second. Full clean execution still requires the six original products and the exact environment captured from the processing server.
