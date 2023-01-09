# CometTrack
Code to analyze the EB1-GFP comet length at the end of growing microtubules from TIRF acquisitions.

# Comet tracking with Fiji
Using the Point tool in Fiji, mark the coordinate where the comet starts on the first slice where the comet appears and the coordinate where the comet ends on the last slice before it disappears.


organisation required: in Data folder folder, 1 subfolder/condition, named: SS_tubTTTuM_EBeenM_TXX_YYMMDD_R_AAA, 
SS: species, TTT concentration tubulin in uM, ee concentration EB1 in nM, XX temperature, YYMMDD date of assay, R # of reaction, AAA # of assay within reaction
in each subfolder, one .tif file with image sequence and one .zip file with ROIs
Data is available upon request: elladegaulejac@gmail.com

# Analysis
The Jupyter notebook CometTrack.ipynb generates profiles from the movies and ROIs stored in the data folder. It aligns, average and normalise the profiles per velocity bin and species. It fits an exponential decay function to retrieve the comet length.
Code written based on: https://github.com/brouhardlab/Chaaban-2018
