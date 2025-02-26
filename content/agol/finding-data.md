---
layout: default
title: Finding Data
parent: Learn the Basics of AGOL
nav_order: 3

---

# Finding Data
{: .no_toc }

Source data using AGOL, Living Atlas and external sites
{: .fs-6 .fw-300 }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## My Organization
{:toc}

When you have an account through a large organization like UMass, there is a wealth of geospatial data already available to you through your organization. In the **Content** tab, click **My Organization** to browse the items that other users have already published.

Try typing **keywords** into the search bar to look for specific content, and using **filters** to limit results to specific items, types, locations etc. 
{: .note}

!['Content' page](media/all_AGOL/replaceAGOL.png "Content Page")

--- 

## Living Atlas
{:toc}

The ArcGIS Living Atlas of the World is a collection of curated spatial data from around the world. It contains maps, apps, and data layers created by Esri and supported partners that are made available for free to all AGOL users. All Living Atlas layers have been verified by Esri, making it a reliable source of spatial data. 

<br>
### Finding Living Atlas Data via AGOL
{: .no_toc }

Navigate to the **Content** tab, then in the blue menu bar click **Living Atlas.** From here, you can use use keywords and filters to limit the results. Filters can be selected using the menus on the left side, and appear at the top when they are applied.

Notice that in between the “Modified” and “Owner” columns, there are green and blue icons next to some of the items:
* A **green** icon (a circle with a checkmark inside) indicates that the item is *authoritative,* meaning Esri, the company behind Arc products, recommends the dataset for use.
* A **blue** icon (a globe) indicates that the item was created by Esri itself. 
Finding data with either of these labels is a good way to ensure you're using reliable data in your maps. 

![Using Reliable Data](media/all_AGOL/FindData_02.jpg "Choose Reliable Data")

<br>
### Finding Living Atlas Data via the Living Atlas Gallery
{: .no_toc }

You can also access Living Atlas content through the [Living Atlas Gallery](https://livingatlas.arcgis.com/en/browse/). Similarly to the AGOL interface, filters can be applied through the menus to narrow down to a specific category. 


[Browse the Living Atlas Gallery](https://livingatlas.arcgis.com/en/browse/){: .btn .btn-green }


![Living Atlas](media/all_AGOL/FindData_03.jpg "Explore the Living Atlas")

---

## External websites
{:toc}

If you can’t find what you’re looking for in AGOL, chances are good that you can find it somewhere else on the web. For a non-exhaustive list of reputable external data sources, check out the [UMass GIS Hub](https://gis.library.umass.edu/data/subject/).

One of the main sources of authoritative spatial data are government agencies. Many states have open data portals where you can easily search for and download geospatial data within that state. For example, in Massachusetts we have the state’s GIS bureau, [**MassGIS**](https://www.mass.gov/info-details/massgis-data-layers), which is an excellent source of data for tax parcels, buildings, roads, open space, aerial imagery, elevation data, and anything else to do with state-level management. 

### Example from MassGIS
{: .no_toc}

In this example from MassGIS of the [2020 U.S. Census Boundaries](https://www.mass.gov/info-details/massgis-data-2020-us-census), there are three ways to access the data:
1. Download it directly.
2. View it in [MassMapper](https://maps.massgis.digital.mass.gov/MassMapper/MassMapper.html), an interactive map interface NOT associated with Esri or AGOL.
3. Access it via AGOL.

<img src="media/all_AGOL/FindData_04.jpg" alt="MassGIS Website" class="center" width="600">

You can also access these externally published layers through the AGOL interface itself. To find the above example, open a blank map in AGOL, go to **Add Layer** and click the dropdown menu to select **ArcGIS Online**. From here you can quickly search for a layer you're looking for. Typing in **"2020 U.S. Census Geography"** in the search bar will give you the same data layer that is shown above from MassGIS. 

<img src= "media/all_AGOL/FindData_05.png" alt="MassGIS data via AGOL" class="center" width="600">

Many (but not all) external websites make their data layers published as AGOL layers, which conveniently saves you the step of actually searching externally. Instead, you can search for layers directly in the AGOL web map. 
{: .note}

The most important aspect of looking for data, especially from external sources, is to use reliable sites. We already went over how to look for reliable datasets via the AGOL interface, but if you're looking for a good starting point for external sources, be sure to explore the [UMass GIS Hub](https://gis.library.umass.edu/data/), specially curated and fact-checked by our wonderful librarians!

---

Do some exploring on your own and find some datasets you'd like to work with, and when you're ready, tune in to the next tutorial where we will be covering how to make a web map!