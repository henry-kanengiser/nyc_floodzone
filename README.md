# nyc_floodzone
This repository contains the programs, files, and output from my analysis of residential housing in NYC's current and future flood zones. Conducted as part of NYU Wagner Course Spatial Analysis &amp; Visualization Fall 2022

The .csv file for NYC DCP's PLUTO is too large to store in this repository, but is free to download from DCP's Bytes of the Big Apple website here: https://www.nyc.gov/site/planning/data-maps/open-data/dwn-pluto-mappluto.page

The main task of this spatial analysis was to overlay the city’s flood zones with MapPLUTO, a shapefile containing information on every tax lot in the city. Using QGIS, I flagged all tax lots that fell within each flood zone and conducted analyses using mostly variables found on the MapPLUTO. To connect the flood zone maps to ACS estimates at the census tract level, I used the census tract codes within MapPLUTO to link the two. I decided to flag any census tract as a flood zone tract if it had at least one residential building flagged as falling within the flood zone.

To calculate the area of the flood zone within each borough, I used QGIS to identify the area of the flood zone within the land borders of each borough. I used R to do the rest of the data manipulation for this project, with some final data manipulation in Google Sheets for some summary statistics. My full R documentation can be found in the R Markdown files. My R scripts, QGZ files, and data used in this project can be found here.

Note that there were several other data sources that I worked with in this analysis (nycdb data on rent stabilization and NYCHA development locations, for example) that I ultimately did not use in the final version of this paper. I’m leaving these data intact in case someone else hopes to build on this analysis in the future and would find those data helpful.
