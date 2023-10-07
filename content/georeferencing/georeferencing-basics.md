---
layout: default
title: Georeferencing Basics
parent: Georeference a Historical Map
nav_order: 2
---

# Georeferencing Basics
{: .no_toc }

Source layers, target layers, and ground control points (GCPs)
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

The goal of georeferencing is to assign *coordinates* (locational information) to a scanned image so that GIS software knows what part of the world it is referencing (i.e. "where it lives").

Georeferenced imagery is all around you! Here are some examples:
* Satellite imagery layers in [Google Maps](https://www.google.com/maps)
* Historical redlining maps from the [Mapping Inequality project](https://dsl.richmond.edu/panorama/redlining/#loc=12/42.173/-72.638&city=holyoke-chicopee-ma)
* Historical spy-satellite images of the Near East from the [CAST Corona Atlas](https://corona.cast.uark.edu/atlas#zoom=13&center=4572043,4392721)

---
## Key terms to know
{:toc}

**Source layer**<br/>
The map or aerial photograph that you will georeference. This is inherently a *raster* file type, because all images are rasters. If you have a physical copy of the map, it should be scanned at high resolution (e.g. 600 dpi) and saved as an image file. Good formats for images include `.tif` and `.jpg`. Or you can find digital versions of maps/photos that have already been scanned.

**Target layer**<br/>
An existing spatial dataset (in the correct location) that you will use to georeference the source layer.

*What makes a good target layer?*
* It should cover the entire extent of the source layer. Put another way, the image you want to georeference should fit entirely within this target layer.
* It can be a vector dataset (like the outline or boundary of a state) or another raster (like a satellite image).
* The level of detail should be roughly the same as what is in the source layer. For example: a map of the state of Massachusetts could be georeferenced using just a state boundary file; but an aerial photo of Amherst will need to be georeferenced using a more detailed image, like a satellite image from Google Earth.

**Ground control points (GCPs)**<br/>
Common points that connect the two layers. You will look for and create GCPs during the georeferencing process.

*What makes a good GCP?*
* Good GCPs are points that stay the same over time, like the corners of buildings, intersections between two roads, or railroad lines.
* GCPs to avoid include points that are more likely to move, like the borders of land cover types (forested areas, water bodies), individual trees or bushes, the edges of roads, or moveable recreational features (like home plate in a baseball diamond).
* You should also avoid using points that could vary depending on the angle the photo was taken, such as anything very high in elevation (bridges, skyscraper roofs).

---
## Where to look for scanned maps and photos
{:toc}

Here are some great places to explore scanned imagery:

*Government sources*
* [MassGIS Oliver](http://maps.massgis.state.ma.us/map_ol/oliver.php)
* [State Library of Massachusetts Real Estate Atlases](https://www.mass.gov/service-details/massachusetts-real-estate-atlas-digitization-project-by-the-state-library)

*Private or public collections*
* [David Rumsey Historical Map Collection](https://www.davidrumsey.com)
* [Leventhal Map & Education Center Digital Collections](https://collections.leventhalmap.org)
* [Old Maps Online](https://www.oldmapsonline.org)
* [Digital Sanborn Maps (1867-1970)](http://silk.library.umass.edu/login?url=http://sanborn.umi.com/) (w/ UMass NetID)

*University map collections*
* [Perry-Castañeda Library Map Collection](http://legacy.lib.utexas.edu/maps/index.html)
* [UConn Library Historical Map Collection](http://magic.lib.uconn.edu/historical_maps.html)
