---
layout: default
title: Coordinate Systems
parent: Learn the Basics of QGIS
nav_order: 3
---

# Coordinate Systems
{: .no_toc }

The key to how geospatial data works
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
## Overview
{:toc}

If I told you it was 40 degrees today, what would you imagine?

![An adorable snowperson on the left, and a desert wasteland on the right](media/ice_vs_desert.png "40 degrees Fahrenheit vs. 40 degrees Celsius")

How you interpret "40" depends on the system of measurement. 40 degrees means one thing if the system is  Fahrenheit (super cold!) and something very different if the system is Celsius (super hot!).

Coordinate Reference System (CRS's) function in a similar same way. We use coordinate pairs - consisting of an **X value (longitude)** and a **Y value (latitude)** - to identify a location on the earth's surface.

The CRS is the key to understanding what those numbers mean. The same location could have thousands of different coordinate pairs - one for every CRS that exists today!

---
## The Geoid, Ellipsoids, and Datums
{:toc}

These are the building blocks of different CRS's.

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSGEAMvj797ZfrIWaxbA-2QcR96BZvFSvNuqk1BX9_KRXmUMBonSbD8msN2btH0UT2QRwFgAtOt9gcb/embed?start=false&loop=false&delayms=3000" frameborder="0" width="576" height="359" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

---
## Types of Coordinate Reference Systems
{:toc}

There are two types of CRS's:

* **Geographic CRS's** are used for 3D surfaces like globes.
* **Projected CRS's** are used for flat surfaces like maps and computer screens.

![Icons showing geographic coordinate systems as a globe and projected coordinate systems as a map](media/coordinate_icons.JPG "Geographic vs. projected coordinate systems")

---
### Geographic CRS's
{:toc}

These are used to map locations on a 3D surface. Measurements are in **degrees**.

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vS7B8-C2OpJ1m6Fbi5cA9erouBX68OD0AqLvTzRb9j4kczKS5oJCGD3NUVkoQDflsJe6WGulTBqOmIC/embed?start=false&loop=false&delayms=3000" frameborder="0" width="576" height="359" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

---
### Projected CRS's
{:toc}

These are used to map locations on a 2D surface. Measurements are in units like **meters, feet, miles, etc.**

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSOvKt84SI690sD9P802FjpQBulrvDa7WlFSGtN1I9BcSwBVN2yaLJWUzWl-z_uFdt7viBjGNb1jad1/embed?start=false&loop=false&delayms=3000" frameborder="0" width="576" height="359" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

---
### Common Projection Systems
{:toc}

These are the most common systems you're likely to encounter if you work with data from the US.

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSuTxX-KPYsD_Bvpx8EoC_say2DYeyrYJmizPT8eCTpU1zkrCQrl5VByTA0UyRj_ZBLHtR6u0f_eRZG/embed?start=false&loop=false&delayms=3000" frameborder="0" width="576" height="359" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

---
## Practice in QGIS
{:toc}

It is an excellent idea to use the same system for all the data in your project. This section will show you how to identify a data layer's CRS and how to change it, if necessary.

### Identify a layer's CRS
{:toc}

The quick way to find out a layer's CRS is to open it in QGIS and look at its information in the `Properties` window. These steps work for both vector and raster data.

Refer back to the [Getting Started page](https://umass-gis.github.io/workshops/content/basics-qgis/getting-started.html#explore-the-qgis-interface) to familiarize yourself with the QGIS interface and how to open layers.

In the Layers Panel, right-click the layer's name and select `Properties...` Information about the CRS will appear in the top part of the window.

<img src='https://umass-gis.github.io/workshops/content/basics-qgis/media/CRS_annotated.png' width='700' alt='Properties window of a vector data layer'>

In this example, the CRS is [EPSG:26986 - NAD83 / Massachusetts Mainland - Projected](https://epsg.io/26986), which the Commonwealth of Massachusetts uses for most of its GIS data. We know this is a **projected** CRS because it has "projected" in the name, but also because the unit is meters. Only projected CRS's use standard units of measurement, like feet, meters, etc.

---
### Change a layer's CRS
{:toc}

Generally, it is a great idea for all your data to have the same CRS.

Streamlining your data's coordinate systems helps avoid issues that stem from CRS mishaps (see [Troubleshooting](#troubleshooting) below), and it also helps you get into the habit of double- and triple-checking that your coordinate systems are in order.

Let's say you downloaded a data layer from the state government. You checked the layer's Properties information and found out that its CRS is [EPSG:26986 - NAD83 / Massachusetts Mainland - Projected](https://epsg.io/26986). However, all your other data is in [EPSG:32618 - WGS 84 / UTM zone 18N](https://epsg.io/32618).

Vectors
{: .label .label-green }

#### Vectors: Export the layer
{:.no_toc}

The quickest way to change the CRS of a vector layer is to make a copy by exporting it. During the export process, you have the option to define a new CRS for the new layer.

In the Layers Panel, right-click the layer's name and click `Export > Save Features As...` Fill out the dialog window:
* **Format**: ESRI Shapefile is the default option, but you can change this if you prefer a different format
* **File name**: click the three dots `...` to the right of the box, navigate to your output folder, and type in a name for the output file. Make sure to add the proper extension (.shp for shapefiles).
* **CRS**: click the globe icon to the right of the box, then type **32618** into the filter bar in order to quickly locate the CRS you want. Select it and click `OK`.

<img src='https://umass-gis.github.io/workshops/content/basics-qgis/media/CRS_selector.JPG' width='600' alt='Coordinate Reference System Selector dialog'>

Leave the rest of the fields as their default values, and click `OK`.

<img src='https://umass-gis.github.io/workshops/content/basics-qgis/media/save_vector_as.JPG' width='600' alt='Save Vector Layer As... dialog'>

Rasters
{: .label .label-green }

#### Rasters: Reproject the layer
{:.no_toc}

While it's possible to use the export tool to make a copy of a raster layer in a new CRS, the tool does not work well in most cases. The better option is to reproject it – a more refined process that helps ensure the accuracy of the copied data.

In the menu bar, click `Raster > Projections > Warp (Reproject)...` Fill out the dialog window:
* **Input layer**: select the raster layer you want to copy
* **Source CRS**: leave this blank - the tool will figure it out
* **Target CRS**: click the globe icon to the right of the box, then type **32618** into the filter bar in order to quickly locate the CRS you want. Select it and click `OK`.
* **Resampling method to use**: the specific method to choose depends on what kind of raster you are working with.
  * **Nearest Neighbor**: if the raster has categorical data (where the pixels represent discrete values like RGB colors in a photograph) and the computer should keep the values exactly the same in the new version.
  * **Bilinear** (faster) or **cubic** (more intense): if the raster has continuous data (where the values in the pixels are measurements, like rainfall data, elevations, etc.) and the computer needs to be able to blend the output values to create new ones.

Read more about raster resampling methods in this [StackExchange post](https://gis.stackexchange.com/questions/10931/what-is-lanczos-resampling-useful-for-in-a-spatial-context)
{: .note}

By default, the tool will save the new layer to a temporary file. This is a handy way to check that everyone worked according to plan before you save a copy to your hard drive (using the [export method discussed above](#vectors-export-the-layer)).

Alternatively, near the bottom of the window in the `Reprojected` box, you can ask the tool to save the file directly to your computer. Click the three dots `...` to the right of the box, navigate to your output folder, and type in a name for the output file. Make sure to add the proper extension (.tif is a good file type for rasters). When you're all set, click `Run`.

<img src='https://umass-gis.github.io/workshops/content/basics-qgis/media/warp.png' width='600' alt='Warp (Reproject) dialog'>

---
### Change the Project CRS
{:toc}

The Map View has a CRS of its own that is independent of the data layers. *Gasp!* What this means is that you can change the CRS for the map – thereby changing the way the data appear – without affecting the CRS of any of the data layers.

The CRS button in the lower right corner is where you can find out more about the Project CRS and change it. Click the button to open the Project CRS window.

<img src='https://umass-gis.github.io/workshops/content/basics-qgis/media/map_view_CRS_anno.png' width='700' alt='Map view, highlighting the CRS button in the bottom-right corner'>

By default, the Project CRS is set to the same CRS as whatever data layer you added first. So if you know that your data layers have all different CRS's, it's a good idea to click this button and check to make sure your Project CRS is set to your preferred format! Again, use the `Filter` bar to quickly search for the CRS you want, or choose from one of the lists.

Here's an example of why this matters for map display. This is a shapefile of towns in Massachusetts. The shapefile's CRS is [EPSG:26986 - NAD83 / Massachusetts Mainland - Projected](https://epsg.io/26986).

<img src='https://umass-gis.github.io/workshops/content/basics-qgis/media/MA_NAD83Projected.png' width='400' alt='Shapefile of towns in Massachusetts, with the Project CRS set to NAD83 Massachusetts Mainland Projected'>
<figcaption>MA in a projected CRS</figcaption>

<img src='https://umass-gis.github.io/workshops/content/basics-qgis/media/MA_WGS84.png' width='400' alt='Shapefile of towns in Massachusetts, with the Project CRS set to WGS84'>
<figcaption>MA in a geographic CRS</figcaption>

In the first image, the Project CRS is set to the same CRS. It appears "correct" – this is how Massachusetts normally shows up on maps! It looks so great because this particular CRS is a projected CRS (so it's intended to be used for flat, 2D displays, like maps and computer screens) and because it is tailored to the location of Massachusetts.

In the second image, the Project CRS is set to [EPSG:4326 - WGS84](https://epsg.io/4326). Now the state looks squished! The problem here is that the CRS is a geographic coordinate system that is intended for global mapping. It isn't really meant to be used for making maps.

---
## Troubleshooting
{:toc}

Faulty coordinate systems are very often to blame for a GIS that stops working properly.

These are some of the most common issues that pop up. If your data isn't displaying properly, check to see if one of these could be the cause:

| Problem | Possible solution |
| :--- | :--- |
| The data layer's CRS is wrong | Right-click, Set CRS |
| The data layer's CRS is missing | Right-click, Set CRS or Export |
| The Map View is set to a different CRS than the data layer | Update Project CRS |
| There are multiple data layers and they all have different CRS's | Sync those layers! |

---
## Resources

These are some of my favorite coordinate system tools:

* [EPSG.io](https://epsg.io/): search for information about over 6,000 coordinate systems
* [FCC DMC-to-Decimal converter](https://www.fcc.gov/media/radio/dms-decimal): quickly convert coordinates from Degrees Minutes Seconds to Decimal Degrees (and vice versa)
* [Rick King's State Plane Coordinate System](https://www.ret3.net/p/state-plane-coordinate-system.html): look up the State Plane and UTM Zones for each county in the U.S.

For a fun and interactive crash-course in map projections, check out [Squashing the Globe](https://www.leventhalmap.org/digital-exhibitions/bending-lines/how-to-bend/projections/) from the digital exhibit *Bending Lines*, by the Leventhal Map & Education Center.
