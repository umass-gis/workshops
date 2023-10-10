---
layout: default
title: Visualizing Data
parent: Learn the Basics of QGIS
nav_order: 5
---

# Visualizing Data
{: .no_toc }

Change the way data appears to explore spatial patterns
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

The way geospatial data is styled - including its color, shape, and size - is called its **symbology**.

At its most basic, symbology can be set so that all the data appears exactly the same way. For example, we might map the US Census block groups in Massachusetts, and all the block groups are the same color: gray with a black outline.

<img src='media/ma_cb.png' width='600' alt='Block groups in MA from the 2020 US Census, all styled as gray polygons'>

More advanced symbology will draw on the *data itself* to style the layer. For example, we might apply a color spectrum so that block groups with lower population densities are **purple** and higher population densities are **yellow**.

<img src='media/ma_cb_pop.png' width='600' alt='Block groups in MA from the 2020 US Census, using the Viridis color scheme to highlight areas with higher population density'>

---
## Vector symbology
{:toc}

Vectors are neat because any data in their **attribute tables** can be used to change the symbology.

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRxmJZRxpq-L3hWxxARiIXQRCM0IPN8URktRQGBevJKTpeCaOtVnMO9SpROoJpY6yLUKeUpE1cEQf2B/embed?start=false&loop=false&delayms=3000" frameborder="0" width="576" height="359" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

---
## Raster symbology
{:toc}

Raster values can also be used to change the way the data is visualized.

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQ_WVGpS3BfDRHK5lzek-6lnlZoJposG7lSgcvTctvm11yTyJyYG1nnw0BWegourEt9qGjhx28JwJA4/embed?start=false&loop=false&delayms=3000" frameborder="0" width="576" height="359" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
