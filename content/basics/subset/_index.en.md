---
date: 2020-08-05T16:50:16+02:00
title: Subsetting an image
weight: 25
---
A typical Landsat scene covers an area of about 185km by 185km. At times, it makes sense to cut out a subset of  this larger image to simplify analysis  and focus on the portion of  the scene that is  of primary interest. By working with data that has a smaller file size it allows faster processing and display updates.

## Creating an AOI layer

These options allow to define an AOI (Area of Interest) in the image, excluding other parts of the image. Specific processes can be applied to this AOI only, which can save considerable time and disk space. The option to use a specified AOI for processing is available from many dialogs throughout ERDAS IMAGINE.


The exercise is about how to create an AOI layer that can be saved as a file and recalled for later use.

_ NOTE: Each viewer can display only one AOI layer at a time._


Select **File → New → 2D View → AOI layer from the viewer menu bar.
Open AOI Tools**

* Select **Drawing** button from the viewer menu bar.

* Click the Rectangle icon from **insert geometry** in the AOI tool palette.

* Move the cursor into the viewer window.

* Drag and the release to draw a rectangle over the AOI.
**Save AOI**

* Select File → Save → AOI layer as from the viewer menu bar.
* Enter the name for the AOI layer under **save AOI as** (the AOI extension is added automatically).

### Steps

* **Create an AOI layer** that we want to subset out.

* Select **Raster → Subset and chip → Create subset image** .

![Create Subset image tool in the Raster tab](/en/basics/subset/images/1.png?classes=shadow)

* From the **Subset** dialog box, select the input file and anoutput destination and file name
also add the **AOI layer**.

* When the job is done, push the **OK** button and your subset is ready to go.

![ Satellite image obtained from USGS ](/en/basics/subset/images/2.png?classes=shadow)

 Satellite image obtained from USGS is shown above and subset image is shown below

![Subset image](/en/basics/subset/images/3.png?classes=shadow)
