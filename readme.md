# secrdesignapp 1.3

secrdesignapp is a partial interactive interface to the R package [secrdesign](https://CRAN.R-project.org/package=secrdesign). See the Help tab for details.

The main new feature in version 1.1 was support for systematic and random designs within a region of interest. Version 1.2 has many small improvements, including traffic lights and other warnings. Version 1.3 (July 2019) introduces -

* user control of traffic light thresholds
* user-specified 2-D distribution models for *simulated* activity centres ('cluster' and 'even' as alternatives to Poisson)
* optional file input of habitat mask

along with other minor improvements.

Click this link to run secrdesignapp 1.2 in your web browser from a University of Otago server:

[secrdesignapp](https://www.stats.otago.ac.nz/secrdesignapp)

Simulations may run faster on your own machine, and the GitHub version is always the latest (now secrdesignapp 1.3). There is also a limit to the number of concurrent users on the server. To run in a local R session directly from GitHub, first install R packages 'shiny' and 'shinyjs'; then paste and run this code at the R command prompt:

```r
library(shiny)
runGitHub("secrdesignapp", "MurrayEfford")
```
Version 1.3 requires secr >= 3.2.0, openCR >= 1.3.4 and secrdesign >= 2.5.7. Various other R packages may be needed for specific operations.

If you intend to use bookmarking on your local machine to store the state of `secrdesignapp` then specify the 'port' and 'destdir' arguments, e.g.,

```r
library(shiny)
runGitHub("secrdesignapp", "MurrayEfford", port = 8000, destdir = "d:/density secr 3.2/testing")
```
The URL generated by pressing the Bookmark button may then be entered into your browser once you have started a new session with the same 'port' and 'destdir'. This restores all input settings and the Summary table, but not results on the Simulation or Spacing pages. 

----

Some test data are provided:

| File name | Description | Usage |
|--------|-------------------------------|------------------|
ovtrap.txt | Locations of possum traps in the Orongorongo Valley | Design - File input of detector array |
ovmask.txt | text file of possible mask for possum study | Habitat mask - File|
OVforest.dbf | ESRI polygon shapefile extent of habitat near possum traps | Design - Region and Options - Habitat clip to polygons |
OVforest.shp |||
OVforest.shx |||
excltest.txt | OV polygon to demonstrate exclusion feature | Options - Detector array - Excluded region |
regionxy.txt | text file of a hypothetical study area boundary |Design - Region and Options - Habitat clip to polygons|

### Reference

Efford, M. G. and Boulanger, J. (2019) Fast evaluation of study designs for spatially explicit capture-recapture. Methods in Ecology and Evolution (in press)
