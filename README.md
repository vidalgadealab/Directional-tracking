# Directional-tracking
Animal heading calculator

Bainbridge C., Stein, W., Vidal-Gadea A.G.

School of Biological Sciences, Illinois State University, Normal, IL

Purpose
Calculates average heading of moving animals using Spike2 software (Cambridge Electronic Design Ltd). 
 
Function
This script bins animal centroid tracks spatially and temporally to provide average headings over time. The script bins each track 20 times. Angle headings are calculated as a straight line from the first frame of the spatial bin to the last frame of the bin. Each angle is then placed into temporal bins from 10 minutes to 100 minutes based frame number in 10 minute intervals. The script generates an output log file of each spatially binned heading and its corresponding time bin.
 
Output
Output consists of a text file with columns containing track number, bin number, angular heading, and corresponding time stamp for each of the twenty track bins of each track.

Post hoc analysis
Post hoc analysis of heading data requires exporting log file output of the script into Microsoft Excel. Heading data is then sorted by time bin for each individual assay. Heading data for each time bin (mean angle) is then averaged across all animals within an assay using Matlab (Mathworks) circular statistics module. This results in each individual assay contributing one average mean heading per time bin. Averaged headings are then pooled across assays and sorted by their respective time bin so that there is one reported heading per time bin, per assay. Pooled data are then manually sorted into 10-30 minutes, 40-60 minutes, and 70-90 minute categories, according to their time bins. These categories are analyzed (Rayleigh test) and plotted using Matlab (Mathworks) circular statistics module. 
