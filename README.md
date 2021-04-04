# MERFISH
This repository contains scripts that were used in Favuzzi et al., GABA receptive microglia selectively sculpt developing inhibitory circuits.

These scripts run on the output mosaics generated by Merlin. At this point, the data should be in a repository of the following structure. Stiched mosaics for smFISH and MERFISH data should be saved in the matching folders.
- Control1
  - Slice1
    - Analysis
    - SmFISH_mosaics
    - Merfish_mosaics
  - Slice2
    - Analysis...


First run groupdsmFISH.m to sum smfish images, run maskFOV to create a mask and only run the analysis on your region of interest.
Then run Main_analysis.m to generate count and intensity matrix for respectively MERFISH encoded genes and smFISH.
To count the smFISH transcripts for 4 genes as done in the paper, run countsmFISHHIGH.m
To recount Gabbr1 and Gabbr2 in only the Z that are part of the microglia, run recountwithZ.m
Then run the R script for downstream analysis (MERFISH_downstream.R)
After running clustering, edit ExtractCells2plot.m to choose which cluster to generate maps for, then run makecontrolmaps.m to generate maps of all microglia in this cluster for all control slices
