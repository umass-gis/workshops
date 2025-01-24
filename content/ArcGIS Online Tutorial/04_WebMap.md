---
layout: default
title: Make a Web Map
parent: Learn the Basics of AGOL
nav_order: 4
---

# Making a Web Map in AGOL
{: .no_toc }

Now, the fun begins! Let's make a map.
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

## Opening MapViewer
{:toc}

To get started with making a web map, click **Map** in the top menu bar to launch the AGOL Map Viewer.

![Opening the Map Viewer](media/all_AGOL/WebMap_01.jpg "Opening the AGOL Map Viewer")

Within the map interface, you’ll notice there are two vertical menu bars on the left and right sides of the map.
* The left menu bar contains tabs for adding data, viewing and organizing layers and tables, changing the basemap, viewing any charts you may have created for your data, viewing the legend, and saving and sharing the map.
* The right menu bar has tabs that allow you to change the appearance of your data, edit your data, and analyze your data.

---

## Adding a layer from AGOL 
{:toc}

### What are layers?
{: .no_toc }

It can be helpful to think of GIS as a layer cake, which allows us to take the real world and turn it into a collection of abstract, spatial data layers. As in the image below, layers that are at the bottom of the list are drawn at the bottom of the cake. Layers at the top of the list are drawn on top.

<img src='https://saylordotorg.github.io/text_essentials-of-geographic-information-systems/section_05/f2619b76bb0d1d0f74b0e8d80ba33496.jpg' width='400' alt='Cartoon image of GIS layers, each representing a different type of feature in the real world: customers as points, streets as lines, parcels as polygons, elevation as continuous raster data, and land usage as categorigal raster data, with the "real world" below them.'>
<figcaption><a href="https://saylordotorg.github.io/text_essentials-of-geographic-information-systems/s05-03-geographic-information-systems.html">Campbell and Shin 2011: Figure 1.8</a></figcaption>

### Adding a Layer
{: .no_toc}

Let’s add a layer from AGOL. For this demo, we will be looking at <u>public schools<u> and <u>parks<u> in the United States, but feel free to search for any layer you like.
1. Navigate to the **Layers** tab on the left manu, then click the “Add” button.
1. The default search setting is set to **“My Content.”** Change it to **“Living Atlas”** to browse through Esri’s curated datasets. 
1. Use the search bar to look for “U.S. Public Schools (with Placekey).” 
1. When you find the layer, click “Add to Map.” When inserting a layer, AGOL will prompt you to pick a “style.” This simply refers to how the data will be visually displayed

  ![Adding USA Schools Layer](media/all_AGOL/WebMap_03.jpg "Adding USA Schools Layer from Living Atlas")
1. Let’s add a second layer. Search for “USA Parks.” Add that to your map as well.
1. Click the back arrow to exit out of the search menu. 

Your map should now have two layers spanning the entire United States - one showing the location of public schools and towns (points) and another showing parks (polygons).

---

## Navigating the Map
{:toc}

In this interface, you can **click and drag** the map to move around and see different locations. 

### Zooming in and out
{: .no_toc }

Use the scroll wheel on the mouse to **zoom in and out**. You can also zoom in and out using the + and - buttons in the lower right corner of the map.

Notice that as you zoom into the map, you can see more details about the specific area you’re viewing, such as roads and town names that are not present at a zoomed-out level. This is also the case with more complex layers. If a layer has many points in the same area, not all of them will be visible when the map is zoomed out.

You can also quickly zoom to the "extent" of any layer in the map:
1. In the **Layers** tab, click the **three dots** next to a layer's name.
1. Click **"Zoom to"** to zoom out to the extent of the whole layer. In this case, the mpa should zoom out to show the entire US. 

![Zoom in and out](media/all_AGOL/WebMap_05.jpg "Zooming features")

### Reordering Layers
{: .no_toc }

Layers in GIS, as mentioned before, function like layers in a cake; layers at the bottom of the list are drawn at the bottom and can therefore be "covered" by any layers above it in the case of spatial overlap. 

In our example, the U.S. Public Schools layer is being drawn below the USA Parks layer. Let’s change this so we can see the schools better:
1. In the **Layers** tab, click and drag the **six dots** to the left of the layer name.
1. Reorder the layers in the list to change the drawing order in the map.

![Reordering layers](media/all_AGOL/WebMap_06.jpg "Reordering Layers")

### Hide Layers
{: .no_toc }

You can also hide layers temporarily so you can focus on other layers by clicking the **eyeball symbol** to the right of the layer name.

![Hiding Layers](media/all_AGOL/WebMap_07.jpg "Hiding Layers")

### Using Basic Map Tools
{: .no_toc }

In the right menu, click the **wrench icon** to open the Map Tools menu. It will prompt you to select one of three tools: **Directions, Measurement** or **Location.**

![Directions, Measurement and Location Tools](media/all_AGOL/WebMap_08.jpg "Directions, Measurement and Location Tools")

* The **Directions** tool works the same way as any navigation app on your phone. Input a Start and End location, and the tool will automatically calculate the estimated drive time, distance, and directions from the first location to the second. You can also add in multiple destinations, change your departure time, and change the method from “driving time” to another transportation method. Notice that this tool outputs a new layer into your layers list called "Route." Every time you run this tool, it will be saved as a new Route layer.

![Directions Tool](media/all_AGOL/WebMap_09.jpg "'Directions' Tool")

* The **Measure** tool gives a rough distance between two points. Simply click at your starting location and double-click at your end location to calculate the distance. 

Because we are not using specific addresses or latitude/longitude coordinates, instead are relying on a rough mouse click, this will not be 100% accurate.
{.note}

!['Measure' Tool](media/all_AGOL/WebMap_10.jpg "'Measure' Tool")

* The **Location** tool displays a pop-up window in the top right corner of the map which shows the coordinates of the location where your cursor is hovering. You can change the units from XY (the latitude and longitude) to decimal degrees or another coordinate system (we don't cover coordinate systems in detail here). 

!['Location' Tool](media/all_AGOL/WebMap_11.jpg "'Location' Tool")

### Remove a layer
{: .no_toc }

Done with a layer? you can remove it from the map at any time.
1. In the **Layers** tab, click the **three dots** to the right of a layer name
1. Click **“Remove.”**

  ![Remove a Layer](media/all_AGOL/WebMap_12.jpg "Remove a Layer")

Remember that while Living Atlas layers are easy to find and re-add to your map, layers that you create from a map tool like Directions will need to be re-calculated if you decide you want to add them back in.

---

## Explore the Attribute Table
{:toc}

An attribute table is essentially a spreadsheet that stores information about the features in a vector layer. Features can be points, lines, or areas (polygons).

Each **row** in the attribute table corresponds to a specific feature. If we look at the U.S. Public Schools layer, each row represents one school. Each **column** (or “field”) contains a specific kind of information about that feature, such as the school’s name, address, type, etc. 

Let's look at the attribute table for the "U.S. Public Schools" layer:
1. Click on the **three dots** next to the layer name
1. Select **"Show Table."** The attribute table will appear at the bottom of the screen. 

  ![Attribute Table](media/all_AGOL/WebMap_13.png "View the Attribute Table")
1. Use the scroll bars to browse through the information this dataset has to offer! 
1. When you’re done, simply click the “x” at the top right corner of the attribute table to remove it from view.

![Click to show attribute table](media/all_AGOL/WebMap_14.jpg "Show Table")

### Show and Hide Fields
{: .no_toc }

At times you may want to show or hide fields in the attribute table to make it easier to find the information that is most relevant to you. 

In the top right corner of the table, click the **gear icon** to bring up the Field Visibility menu. Checking a field will make it visible, and unchecking it will hide it.

![Toggle Fields visibility](media/all_AGOL/WebMap_15.png "Toggle Fields View")

### Sort the Attribute Table
{: .no_toc }

Sorting the attribute table can be useful if you are looking for a specific feature in the layer. To sort the table, click a column heading and select **“Sort ascending”** or **“Sort descending.”** This will automatically sort the table alphabetically (for text fields) or in numerical order (for number fields).

![Sort Table by Ascending](media/all_AGOL/WebMap_16.png "Sort Table by Ascending")

### Zoom to Selection
{: .no_toc }

Once you find a specific feature, you can quickly pan and zoom the map to it using the attribute table.

Click the **checkbox** next to the desired feature to select it, then in the left panel click **“Zoom to selection.”** The map will automatically pan and zoom to your chosen feature.

![Table Zoom to Selection](media/all_AGOL/WebMap_17.png "Table Zoom to Selection")

### Filters
{: .no_toc }

Let’s say that we only need the information for schools in Hampshire County, Massachusetts. Looking at the entire dataset, which contains more than 102,000 features, might make it hard to find the information we need. To focus on the specific records we want, we can use a filter to specify which criteria we want to view, and exclude everything else.

In the right menu bar, the Filter menu (symbolized by a funnel) allows you to select specific values from any field in the attribute table. Let’s define our filters:
1. In the Layers list, click on the schools layer to select it
1. In the right menu bar, open the **Filter** and click **"Add New"**

  ![Filters Pop-up](media/all_AGOL/WebMap_18.jpg "Filters Pop-up Window")
1. Use the first drop-down menu to define the field that contains the information we are looking for. Since we are looking for schools in a specific state, we will use the **“State”** field. 
1. The second drop-down menu specifies the **operator,** which tells the tool how to look for the information. To look for an exact match, we will use the **“is”** operator.

  ![Filtering Query](media/all_AGOL/WebMap_19.jpg "Developing a Filter Query")

1. The last drop-down menu shows us all the unique values in our chosen field (State). From the list, select **“MA.”** Together, this builds the condition: “show us only the schools where the *State is MA.”* 

  ![Choosing Conditional Statements](media/all_AGOL/WebMap_20.jpg "Choosing Conditional Statements for Filtering Query")
1. We can add more conditions to refine the filter even more. Click **“Add new”** below the first filter and specify the condition “where *County is Hampshire.*” 

  ![Choosing Conditional Statements pt 2](media/all_AGOL/WebMap_21.jpg "Choosing Conditional Statments for Filtering Query, pt 2")
1. Zoom out to show the US and change the relationship from "“All of the following are true” to “Any of the following are true.” 
    * When *all* the conditions must be true, only schools in Hampshire County, MA will be shown – a total of 49 schools.
    * If *any* of the conditions can be true, the filter will show all the schools in any Hampshire County in the U.S., plus all the schools in Massachusetts – a total of 1, 881 schools.

1. Click **"Save"** to apply this filter to both the map and the attribute table. 

---

## Change Layer Appearance
{:toc}

There are many different ways to visualize your data in a map! Let’s try changing the way our schools layer looks. Note that we’ll be focusing on a **point layer,** but you can follow a similar workflow to change the way a **polygon layer** looks, too.

### Visibility
{: .no_toc }

Click on the **three dots** next to the layer name, and then click **“Show properties.”** The Properties tab will open on the right side of the screen.

![Showing Layer Properties](media/all_AGOL/WebMap_22.jpg "Showing Layer Properties")

The Properties menu contains a snapshot of how the layer is being displayed on the map. This includes the current *Symbology* of the layer and other traits such as *Appearance* and *Visibility*. You can quickly modify the layer’s transparency and visible range through this menu. 

Under **Appearance,** let’s change the transparency to 50% to see how it affects the school icons:

![Changing transparency for better visibility](media/all_AGOL/WebMap_23.jpg "Changing Transparency for Better Visibility")

Under **Visibility**, the Visible range is used to define the zoom levels at which the layer will be visible. Drag either end of the visible range to change the layer’s visibility range. The map’s current zoom level is indicated with a black triangle underneath the bar.  If your map’s zoom level is outside the visible range, the layer will be hidden.

This setting is especially useful when publishing web maps with lots of data displayed at different scales. Try experimenting with different ranges to visualize how this affects your map as you zoom in and out.

![Changing Visible Range](media/all_AGOL/WebMap_24.jpg "Changing a Layer's Visible Range")

### Styles
{: .no_toc }

The Styles menu (symbolized as a triangle, square, and circle) allows us to change the way a layer’s icons appear. In the right menu bar, open the **Styles** menu.

![Choosing Layer Styles](media/all_AGOL/WebMap_25.jpg "Choosing Layer Styles")

The default setting for point layers is for all the symbols to appear the same. To change the color and size of all points at the same time: 
1. under **Pick a style**, click **“Style options”** to open the Location (Single symbol) menu. 
1. Click on the symbol to open the Symbol style menu. This is where we can change the current symbol, change the size, fill color, outline color, etc.

  ![Changing Layer Symbology](media/all_AGOL/WebMap_26.png "Changing Layer Symbology")

Oftentimes, we want to use data in the attribute table to automatically change the way the points appear in the map. Let’s say we want the icons to reflect the level of education of each school.
1. In the main **Styles** menu, under **Choose attributes**, click **“+ Field”** to open the fields menu. 
1. Check the “Level” field, then click “Add.” The school icons automatically change to colored dots, and a legend appears in the lower left corner indicating which color represents which level. This is the default style when varying symbology is used.

  ![Changing Symbology by Field](media/all_AGOL/WebMap_27.jpg "Changing Symbology by Field")

  To modify the color scheme, under `Pick a style > Types (unique symbols)`, click on **“Style options”** to open the **Types (Unique symbols)** menu. 

  ![Selecting Color Scheme](media/all_AGOL/WebMap_28.jpg "Selecting Color Scheme")
1. Click on the **“Symbol style”** color ramp. This is where we can change the current symbol, change the size, color ramp, outline color, etc.

  ![Changing Symbology from Basic Point](media/all_AGOL/WebMap_29.jpg "Changing Symbology from Basic Point")
1. To change the current symbol, click on **“Basic point."**
1. In the category drop-down menu, select **“POI Basic.”**
1. Select the schoolhouse symbol, then click **“Done.”**

  ![Choosing New Point Symbol](media/all_AGOL/WebMap_30.jpg "Choosing New Point Symbol")
1. Change the color ramp by clicking on the **“Colors”** menu. In the category drop-down menu, you can filter specific kinds of color ramps, such as colorblind-friendly options.

  ![Colorblind-frieldly color schemes](media/all_AGOL/WebMap_31.jpg "Colorblind-Friendly Color Schemes")
1. The last thing we’ll do is change the size of our icons to make them easier to see. Set the **“Size”** to 30 px, then close the symbol style menu.

  Back in the Style options menu, under Level, notice that the default order of the schools is Elementary > High > Middle, with several additional categories after that. This is because the default order is dictated by the number of features within each category, ordered from most numerous to least numerous. In our case, it would make more sense for the icons to be ordered `Elementary > Middle > High > Other.` To change the order in which school types are displayed:
1. click and hold the six dots next to a level type and drag the item up or down the list.
1. To remove the schools from extraneous levels (like “Prekindergarten” or “Not reported”), click the **checkbox** next to its name and select **“Remove.”**

![Removing Points by Field](media/all_AGOL/WebMap_32.jpg "Remove Points by Field or Atrribute")

### Effects
{: .no_toc }

Effects are another way to change a layer’s appearance. In the right menu bar, click the **Effects** menu (symbolized as a sparkle). Here you will find a variety of options to further customize a layer’s appearance, from adding glows, blurs and shadows, to changing the saturation and hue of their colors. 

Here’s an example of what the Bloom effect looks like with the schools layer:

![Add 'Bloom' Effects](media/all_AGOL/WebMap_33.jpg "Add "Bloom" Effect")

Explore the different symbology options to customize your map in a unique way!

### Pop-ups
{: .no_toc }

If you are looking for information about a single feature in a layer, clicking that feature will bring up a pop-up window with a glimpse of that feature’s information stored in the attribute table. We can use the Pop-up menu to customize the way that information is displayed.

1. Click on a few different schools. Notice that the pop-up window displays information about each specific school we click on. This layer has a lot of attribute information, which makes the pop-up feel crowded. We can edit the pop-up to show only what we feel is relevant and leave the rest out.

  ![Identify Point attributes](media/all_AGOL/WebMap_34.jpg "Identifying Point Attributes through Pop-up")
1. In the right menu bar, click on the **Pop-ups** menu.

  ![Pop-ups menu](media/all_AGOL/WebMap_35.jpg "Toggling Pop-ups Settings")
1. There are a few different ways we can customize the pop-up:
    1. At the top, we can toggle the switch to **enable** or **disable** pop-ups altogether.
    1. Under Options, we can build an **attribute expression** to create custom messages based on existing data in the attribute table. This is a more advanced feature that you can explore beyond this workshop. 
    1. **Title** is used to automatically generate a heading at the top of the pop-up window. By default, the schools layer uses the {NAME} field to populate the title. To change which field shows up at the title, you can simply replace it with your field of choice. Make sure to enclose the field name in curly brackets {}. 
    1. The **Fields** list shows which fields from the attribute table are visible in the pop-up window.
1. Under **Fields list,** click **“Select fields”** to view all of the available fields.

  ![Select Fields to see Available Views](media/all_AGOL/WebMap_36.jpg "Select Fields to see Available Views")
1. To reduce the clutter in the pop-up window, uncheck the following fields: Placekey, NCESID, County FIPS, NAICS Code, Source, Source Date, District ID, and Shelter ID. Click “Done.”
1. Under **Fields list,** click and hold the six dots to the left of any field name to rearrange the field order. Move the Level field to the top of the list. Notice that any changes made in the Pop-up manu are immediately applied to the open pop-up window, allowing you to preview the changes you make. 

  ![Alter Fields List Order](media/all_AGOL/WebMap_37.jpg "Alter Fields List Order")
1. At the bottom of the Pop-ups menu, click “+ Add content” to include additional content like charts, images, and extra text.

  ![Adding Content to Fields List](media/all_AGOL/WebMap_38.jpg "Adding Content to Fields List")

### Labels
{: .no_toc }

Labels are a useful way to show relevant information from the attribute table directly on the map.
1. In the right menu bar, open the **Labels** menu (symbolized by a tag). 

  ![Enabling Labels](media/all_AGOL/WebMap_39.jpg "Enabling Labels")
1. In the **Label field** drop-down menu, select the field in the attribute table that will be used to populate the labels. The default for the schools layer is “Name,” which makes sense to leave as is.
1. Labels have their own visibility range. The default is usually set to a smaller zoom scale because labels tend to take up a lot of space, and the map can become crowded if many labels are being displayed at one time. Drag the **Visible range** slider so that the map’s current zoom level is within the range. Each school is now labeled using its corresponding information from the “Name” field in the layer’s attribute table. Since some of the labels are hard to see, let’s edit the label style.

  ![Altering Layer Visibility Range](media/all_AGOL/WebMap_40.jpg "Altering Layer Visibility Range")
1. Under **Label style,** click **“Edit label style”** to open the Label style menu.
1. Apply a halo effect by toggling on **Halo.** This adds a white background behind the label text to make it easier to read.
1. Under **Placement,** change the drop-down to “Center center.” This moves the position of the labels to be displayed on top of each point.

  ![Edit Layer Appearence and Properties](media/all_AGOL/WebMap_41.jpg "Edit Layer Appearence and Properties")
1. Continue experimenting with these settings to find a style that you like for your labels!

### Save and Export Your Map
{: .no_toc }

It is always a good idea to save our work. Save early, save often!

In the left menu bar, click the **Save and Open menu** (symbolized as a folder). Click **“Save as”** to give the map a title, then **“Save”** to save it to your AGOL content space. The next time you navigate to the **Contents** in your AGOL account, you will see your map saved there for future use.

![Save As](media/all_AGOL/WebMap_42.jpg "Save As")

To export a copy of the map as an image, in the left menu bar click the **Print** menu. 

Optionally give the map a title, specify the size and orientation of the output image, and choose the exported file format. 

Under **Advanced options,** we can include metadata (author, copyright), change the export resolution (DPI) or output spatial reference, and toggle on the legend and north arrow.

![Advanced Save Options](media/all_AGOL/WebMap_43.jpg "Advanced Save Options")

When your settings are to your liking, click the blue **“Export”** button. Your file will appear in the **Exports tab,** where you can then download it to your computer. Below is an example of an exported map, including necessary map elements such as a legend, North arrow, scale bar and title.

![Exported Final Map](media/all_AGOL/WebMap_44.png "Exported Final Map with Necessary Map Elements")

---

Now, you've made your first web map using data brought in from AGOL's databases. But what about creating our own spatial data? Check out the next tutorial in this series to learn how to import and use your own data. 

























