---
layout: default
title: Tutorial
parent: Learn the Basics of QGIS
nav_order: 6
---

# Tutorial
{: .no_toc }

Explore the cities of Holyoke and Chicopee in western Massachusetts to learn how their demographic makeup has changed in the last 80 years
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

### Data Source *1*{: .circle .circle-purple}
{:.no_toc}

Holyoke and Chicopee were mapped by Home Owners' Loan Corporation between 1935 and 1940 - the very program that originated the term “redlining” to describe reputedly ‘hazardous’ neighborhoods that mortgage lenders should avoid at all costs. The project [Mapping Inequality](https://dsl.richmond.edu/panorama/redlining/) has georeferenced the maps and made them available to the public as downloadable data (in shapefile and geoJSON format). The website is an interactive mapping platform that is a great learning tool in itself, but we're going to download just a selection of this data.

### Data Source *2*{: .circle .circle-purple}
{:.no_toc}

In order to explore how the population of Holyoke and Chicopee have changed over time, we'll take a look at the most recent election data from the precincts in these areas, along with data from the 2010 Decennial Census. The project [OpenPrecincts](https://openprecincts.org/ma/) is a great place to look for processed election data. The level of processing is variable by state, but for Massachusetts the data is excellent. The same data (for MA) can be found on the Metric Geometry and Gerrymandering Group's (MGGG) [GitHub repository](https://github.com/mggg-states/MA-shapefiles).

### 1. Download the data
{:.no_toc}

<br>
[Get the data pack](https://github.com/umass-gis/workshops/blob/main/content/basics-qgis/data/Data_QGIS_Fall2020.zip){: .btn .btn-purple }

This link will take you to a page on GitHub. Click the `download` button to save it to your computer.

![Viewing a zip file on GitHub](media/download_anno.png "Downloading a zip file from GitHub")

### 2. Unzip the file
{:.no_toc}

The file you download is zipped, so you'll need to unzip it before you can continue. 

**Windows users**: check out Microsoft's support page, [Zip and Unzip Files](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).<br>
**Mac users**: simply double-click the zip file to decompress it.

### 3. Create a workspace for your data
{:.no_toc}

This is a great time to start practicing good data management! In an ideal world, you'll create a folder just for this tutorial somewhere on your hard drive. Ideas for what to name the folder:
* QGIS_Workshop_Oct2020
* Holyoke_Chicopee_Tutorial_2020_1027
* Basics_of_QGIS_Fall20
* GIS_Data_Is_Awesome

*Just kidding, don't use that last one!*

### 4. Rename the original data folder
{:.no_toc}

Move the unzipped folder to that new workspace and rename it. The goal is to preserve a copy of the original data and let your future self know what the folder contains. Something like:
* Data_Original
* Raw
* Downloaded_Versions

---
## Open the data layers in QGIS
{:toc}

There are two shapefiles in the data pack you downloaded. Follow the instructions on the [Getting Started](https://umass-gis.github.io/workshops/content/basics-qgis/getting-started.html#open-a-layer) page to load the two shapefiles into a new map session in QGIS.

If you get a warning message asking you to **Select Transformation for [data layer]**, just click `OK`. 

Your map session should look something like this (probably with different colors!):

![Data layers in a new QGIS session](media/tutorial_1.png "Data layers in a new QGIS session")

---
## Check their CRS's
{:toc}

Follow the instructions on the [Coordinate Systems](https://umass-gis.github.io/workshops/content/basics-qgis/coordinate-systems.html#identify-a-layers-crs) page to identify the CRS's of the two data layers. 

Quiz time!
{: .label .label-blue }

<details>
<summary>What is the CRS of the layer MA_precincts12_16?</summary>
<br>
It's EPSG:4269 - NAD83.
</details>
<br>

<details>
<summary>What is the CRS of the layer cartodb-query?</summary>
<br>
It's EPSG:4326 - WGS84.
</details>
<br>

<details>
<summary>What is the Project CRS?</summary>
<br>
This should match the CRS of whichever layer you added first.
</details>
<br>

<details>
<summary>Bonus: Are these geographic or projected coordinate systems?</summary>
<br>
Both CRS's are geographic coordinate systems! Giveaways: the CRS unit is degrees, and in the Status Bar the coordinates are +/- values between 0 and 180.
</details>

---
## Sync their CRS's
{:toc}
<br>
Spoilers ahead!
{: .label .label-red }

Let's sync the CRS's of the two data layers and the Map View so they are all calling on the WGS84 datum. This is a good choice if you plan to use the free base imagery available through the [QuickMapServices plugin](https://umass-gis.github.io/workshops/content/basics-qgis/coordinate-systems.html#change-the-project-crs), since it generally should work if the Project CRS is based on the WGS84 datum.

### Change a layer's CRS
{:.no_toc}

The `cartodb-query` layer is okay as it is. Although its CRS is a geographic coordinate system (rather than projected, which is better for map-making), QGIS won't have any trouble readjusting it to look correct once we update the Project CRS.

As long as all your data layers have the same datum, QGIS can "project them on-the-fly" so that they appear to have the same CRS. Issues are much more likely if your data layers have different datums. In this case, the datum is NAD83.
{: .note}

Follow the instructions on the [Coordinate Systems](https://umass-gis.github.io/workshops/content/basics-qgis/coordinate-systems.html#change-a-layers-crs) page to export a new version of the `MA_precincts12_16` layer with a CRS of [EPSG:32618 - WGS 84 / UTM zone 18N](https://epsg.io/32618). You can remove the original `MA_precincts12_16` layer when you're done.

Remember to create a new folder within your project space that is dedicated to new files you've created. You could call it "Data_Processed" or just "Processed," or whatever else will help you remember that these are your original files.
{: .warn}

### Change the Project CRS
{:.no_toc}

Follow the instructions on the [Coordinate Systems](https://umass-gis.github.io/workshops/content/basics-qgis/coordinate-systems.html#change-the-project-crs) page to update the Project CRS to [EPSG:32618 - WGS 84 / UTM zone 18N](https://epsg.io/32618).

Now that everything is synced to a CRS that calls on the WGS84 datum, you can go ahead and load some rad, free base imagery! Follow the instructions on the [Getting Started](https://umass-gis.github.io/workshops/content/basics-qgis/getting-started.html#install-helpful-plugins) page to install the QuickMapServices plugin and add a basemap of your choice.

<img src='https://github.com/umass-gis/workshops/blob/main/content/basics-qgis/media/tutorial_2.png' alt='Data layers for the tutorial: precincts for the entire state and digitized neighborhoods from the HOLC maps, with OpenStreetMaps imagery as a background.'>
<figcaption>All the happy WGS84 layers, with OSM Standard imagery</figcaption>

---
## Change their symbology
{:toc}

---
## Make a map
{:toc}
