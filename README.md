# LauraPuckett_Portfolio
A simple overview of my recent public projects

# [Project 1. Spruce Fractional Cover Mapping at NEON BONA Site](https://github.com/Laura-Puckett/spruce_mapping_NEON_BONA/tree/main)
This is an exploratory project to determine the utility of airborne data collected as part of NASA's ABoVE airborne campaign (AVIRIS-NG hyperspectral and LVIS waveform LiDAR data) for estimating percent cover of black spruce forest. 
While this workflow could be expanded over a larger area, this small project was focused on an area near Fairbanks, ALaska, where NEON field measurements of tree inventory are available across a gradient of environmental conditions. 
The NEON field data was manipulated and used as the "ground-truth" values for the proprtional cover of black spruce. 
AVIRIS-NG spectral bands and LVIS relative height metrics were used as predictors in a simple model. 
The main bottleneck in this project was loading and intersecting these large geospatial datasets to produce a training dataset containing plot-level values for all datasets. 

In order to continue this analysis, more field sites should be incorporated across a larger area. Hundreds of sites with AVIRIS, LVIS, and ground-truth would be required to train a model for a real mapping effort. Because this didn't seem feasible with field sites that I currently have access to, this project was discontinued and I've shifted to a similar project using Landsat and GEDI instead. 

| ![](https://github.com/Laura-Puckett/spruce_mapping_NEON_BONA/blob/main/figures/new_datasets_figure.PNG) | 
|:--:| 
| *Spatial Relationship of Datasets* |



# [Project 2. Comparing spaceborne LiDAR datasets](https://github.com/Laura-Puckett/lidar_comparisons)
This workflow is intended for comparing gedi, icesat-2, or both against airborne lidar data for an area. Because Icesat-2 and GEDI can't be compared directly against each other (due to mismatch in size/shape of footprints), comparing them against airborne lidar separately is used here to infer how similar they are to each other.

This workflow downloads the icesat-2 data, but assumes that you already have gedi and airborne lidar downloaded (unless using NEON lidar - there is a script for that)

| ![](https://github.com/Laura-Puckett/LauraPuckett_Portfolio/blob/ccf59588b8754a188497844d27fc999225798048/Screen%20Shot%202021-03-02%20at%2011.09.14%20AM.png) | 
|:--:| 
| *Example output comparing GEDI and Icesat-2 for a site in the Sierra Nevada Mountains* |

# [Project 3. Assessing LVIS airborne LiDAR Internal Consistency](https://github.com/Laura-Puckett/evaluate_LVISF2_internal_consistency)
The goal of this project was to determine if repeat measurements of LVIS airborne waveform lidar are sufficiently consistent to be used for change detection of soil burning in boreal forest wildfires. The removal of thick soil organic layer in the boreal forest is ecologically relevant for forest regeneration trajectory and also useful for estinmating carbon release due to the combustion of organic soil. If differences in ground elevation estimates of the same location are generally greater than 5cm over a period of time where no changes would be expected (such as consecutive days) then it will not be possible to use these data for detecting burn depth. Ultimately this was the case, and the project shifted direction to assess the use of UAV structure-from-motion data, rather than airborne waveform lidar data, to study burn depth resulting from a wildfire near Fairbanks, Alaska.

| ![](https://github.com/Laura-Puckett/LauraPuckett_Portfolio/blob/32c02a140bea2921dd4c509fd142b4208ec961b3/Screen%20Shot%202021-03-02%20at%2011.29.03%20AM.png) | 
|:--:| 
| *Comparison of LVIS elevation measurements. Values correspond to the difference in spatially matched pairs of LVIS footprints from different acquisitions* |
