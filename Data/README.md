# Data Directory

## RTK Points
Historical RTK coordinate table for 38 control points monitored from September 2022 to September 2023. They are obtained from the *Landslides* Technical Note ["Spatial assessment of landslide risk using GNSS-based displacement analysis and a resident vulnerability index in northwestern Chilpancingo, Guerrero, Mexico"](https://link.springer.com/article/10.1007/s10346-025-02583-y). 

### [Original Data](https://github.com/joaquinsalas/chilpancingo_landslide/blob/main/README.md#:~:text=rtk_original_data.csv)

Unmodified project-source coordinate table. This is the authoritative RTK input
used by the reproducible workflow.

The project explicitly maps `X` to easting and `Y` to northing, based on the
supplied values and EPSG:32614 coordinates. 

### [Processed Data](https://github.com/joaquinsalas/chilpancingo_landslide/tree/main/Data#:~:text=rtk_processed_data.csv)

## ROI
ROI polygon in ESRI Shapefile format.

## NISAR
[Download](https://search.asf.alaska.edu/#/?dataset=NISAR&prodConfig=PR&sciProducts=GSLC&zoom=3.075&center=-73.771,-13.788) the six unique HDF5 products listed in [nisar_product.csv](https://github.com/joaquinsalas/chilpancingo_landslide/blob/main/README.md#:~:text=nisar_product.csv)
