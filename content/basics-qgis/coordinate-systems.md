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
{: .warn}

There are two kinds of  systems:
* **Geographic coordinate systems** are best suited for 3D surfaces like globes.
* **Projected coordinate systems** are designed to display locations on flat surfaces like maps and computer screens.

![Icons showing geographic coordinate systems as a globe and projected coordinate systems as a map](media/coordinate_icons.JPG "Geographic vs. projected coordinate systems")


Fake stats alert!
{: .label .label-yellow }

9 out of 10 problems with GIS are the result of pesky coordinate systems. Often one of these issues is at the heart of the problem:
* the data layer's CS information is wrong,
* the data layer's CS information is missing,
* the Map View is set to a different CS than the data layer,
* or there are multiple data layers and they all have different CS's.

---
## Geographic vs. projected coordinate systems
{:toc}

View this information as a slideshow:
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSGEAMvj797ZfrIWaxbA-2QcR96BZvFSvNuqk1BX9_KRXmUMBonSbD8msN2btH0UT2QRwFgAtOt9gcb/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="389" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

---
## Identify a layer's coordinate system
{:toc}


---
## Change a layer's coordinate system
{:toc}


---
## Change the map view's coordinate system
{:toc}



---
## Resources

These are some of my favorite coordinate system tools:

* [EPSG.io](https://epsg.io/): search for information about over 6,000 coordinate systems
* [FCC DMC-to-Decimal converter](https://www.fcc.gov/media/radio/dms-decimal): quickly convert coordinates from Degrees Minutes Seconds to Decimal Degrees (and vice versa)
* [Rick King's State Plane Coordinate System](https://www.ret3.net/p/state-plane-coordinate-system.html): look up the State Plane and UTM Zones for each county in the U.S.
