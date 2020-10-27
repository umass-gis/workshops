---
layout: default
title: Tutorial
parent: Learn the Basics of QGIS
nav_order: 6
---

# Tutorial
{: .no_toc }

info here
{: .fs-6 .fw-300 }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---
## Setup
{:toc}

This tutorial will give you a chance to practice the lessons covered in this workshop:
* becoming familiar with the QGIS interface
* opening data layers
* organizing data on your hard drive
* managing CRS's
* changing layer symbology
* exporting a map

We'll focus on the cities of Holyoke and Chicopee in western Massachusetts to explore how the demographic makeup of these places has changed in the last 80 years. 

[Download the data pack](https://github.com/umass-gis/workshops/blob/main/content/basics-qgis/data/Data_QGIS_Fall2020.zip){: .btn .btn-purple }

#### Data Source 1: Historical Redlining
{:.no_toc}
Holyoke and Chicopee were mapped by Home Owners' Loan Corporation between 1935 and 1940 - the very program that originated the term “redlining” to describe reputedly ‘hazardous’ neighborhoods that mortgage lenders should avoid at all costs. The project [Mapping Inequality: Redlining in New Deal America](https://dsl.richmond.edu/panorama/redlining/#loc=13/42.182/-72.631&mapview=graded&city=holyoke-chicopee-ma) has georeferenced the maps and made them available to the public as downloadable data (in shapefile and geoJSON format). The website is an interactive mapping platform that is a great learning tool in itself, but we're going to download just a selection of this data.

#### Data Source 2: Contemporary Demographics (+ Politics)
{:.no_toc}
In order to explore how the population of Holyoke and Chicopee have changed over time, we'll take a look at the most recent election data from the precincts in these areas, along with data from the 2010 Decennial Census. The project [OpenPrecincts](https://openprecincts.org/ma/) is a great place to look for processed election data. The level of processing is variable by state, but for Massachusetts the data is excellent. The same data (for MA) can be found on the [Metric Geometry and Gerrymandering Group's (MGGG) GitHub repository](https://github.com/mggg-states/MA-shapefiles).

### Unzip the file
{:.no_toc}

The file you download is zipped, so you'll need to unzip it before you can continue. 

**Windows users**: check out Microsoft's support page, [Zip and Unzip Files](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).<br>
**Mac users**: simply double-click the zip file to decompress it.

### Create a workspace for your data
{:.no_toc}

This is a great time to start practicing good data management! In an ideal world, you'll create a folder just for this tutorial somewhere on your hard drive. Ideas for what to name the folder:
* QGIS_Workshop_Oct2020
* Holyoke_Chicopee_Tutorial_2020_1027
* Basics_of_QGIS_Fall20
* GIS_Data_Is_Awesome

*Just kidding, don't use that last one!*

### Rename the original data folder
{:.no_toc}

Move the unzipped folder to that new workspace and rename it. The goal is to preserve a copy of the original data and let your future self know what the folder contains. Something like:
* Data_Original
* Raw
* Downloaded_Versions

---
## Open the data layers in QGIS
{:toc}

---
## Check their CRS's
{:toc}

---
## Change their symbology
{:toc}

---
## Make a map
{:toc}
