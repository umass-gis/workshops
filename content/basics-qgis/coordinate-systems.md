---
layout: default
title: Coordinate Systems
parent: Learn the Basics of QGIS
nav_order: 3
---

# Coordinate Systems
{: .no_toc }

One of the most mind-bending aspects of GIS, coordinate systems are key to how geospatial data works.
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

Coordinate systems (CS) allow us to locate any place on the earth’s surface.

At their most basic, a coordinate pair consists of two numbers: an **X value (longitude)** and a **Y value (latitude)**. The CS is the key to understanding what those numbers mean. The same location could have thousands of different coordinate pairs - one for every CS that exists today!

It is a good idea to use the same system for all the data in your project. This section will show you how to identify a data layer's CS and how to change it, if necessary.
{: .note}

There are two kinds of  systems:
* **Geographic coordinate systems** are best suited for 3D surfaces like globes.
* **Projected coordinate systems** are designed to display locations on flat surfaces like maps and computer screens.

![Icons showing geographic coordinate systems as a globe and projected coordinate systems as a map](media/coordinate_icons.JPG "Geographic vs. projected coordinate systems")

---
## Geographic vs. projected
{:toc}

View this information as a slideshow:
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSGEAMvj797ZfrIWaxbA-2QcR96BZvFSvNuqk1BX9_KRXmUMBonSbD8msN2btH0UT2QRwFgAtOt9gcb/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="389" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

---
## Identify a layer's CS
{:toc}

The quick way to find out a layer's CS is to open it in QGIS and look at its information in the `Properties` window.

Refer back to the [Getting Started page](https://umass-gis.github.io/workshops/content/basics-qgis/getting-started.html#explore-the-qgis-interface) to familiarize yourself with the QGIS interface.

### 1. Open the layer in QGIS
{:.no_toc}

There are several ways to open a data layer in QGIS:
1. Navigate to the layer in the Browser Panel, then drag and drop it into the Map View.
1. Click `Layer > Add Layer > Add Vector Layer...` then to the right of the `Vector Dataset(s)` box, click the three buttons `...` to open the file explorer. Navigate to the file, click `Open`, then `Add`.
1. Click the `Add Vector Layer...` button and follow the instructions from step 2.

![Manage layers toolbar, with the "Add Vector Layer" button outlined in red](media/manage_layers_annotated.png "Manage layers toolbar")


---
## Change a layer's CS
{:toc}


---
## Change the map view's CS
{:toc}


---
## Troubleshooting
{:toc}

Faulty coordinate systems are very often to blame for a GIS that stops working properly. 

These are some of the most common issues that pop up. If your data isn't displaying properly, check to see if one of these could be the cause:
* the data layer's CS information is wrong,
* the data layer's CS information is missing,
* the Map View is set to a different CS than the data layer,
* there are multiple data layers and they all have different CS's.

---
## Resources

These are some of my favorite coordinate system tools:

* [EPSG.io](https://epsg.io/): search for information about over 6,000 coordinate systems
* [FCC DMC-to-Decimal converter](https://www.fcc.gov/media/radio/dms-decimal): quickly convert coordinates from Degrees Minutes Seconds to Decimal Degrees (and vice versa)
* [Rick King's State Plane Coordinate System](https://www.ret3.net/p/state-plane-coordinate-system.html): look up the State Plane and UTM Zones for each county in the U.S.
