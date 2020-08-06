---
date: 2020-08-05T16:50:16+02:00
title: Georeferencing
weight: 25
---

The process of assigning geographic coordinates to an image is known as georeferencing. The process of shifting pixel locations to remove  distortion is known as rectification.  Often the process  of rectification includes georeferencing, because one can both shift the pixels to remove distortion and assign coordinates to those pixels at the same time.

## Ground Control Points

A ground control point (GCP) is feature that you can clearly identify in the raw image for which you have  a known ground coordinate.   Ground coordinates can come from a variety of sources such   as the Global Positioning System (GPS), ground surveys, Geo coded images, vectors, geographic information systems (GIS), topographic maps, chip databases, or by using photogrammetric pro- cesses to extend the number of GCPs in your images. A GCP determines the relationship between the raw  image and the ground by associating the pixel (P) and line (L) image coordinates to the x, y and z coordinates on the ground.


GCPs are specific pixels in an image for which the output map coordinates (or other output coordinates) are known. GCPs consist of two X,Y pairs of coordinates:

* **Source coordinates** — usually data file coordinates in the image being rectified.

* **Reference coordinates** — the coordinates of the map or reference image to which the source image is being registered.



The term map coordinates is sometimes used loosely to apply to reference coordinates and rectified coordinates. These coordinates are not limited to map coordinates. For example, in image-to-image registration, map coordinates are not necessary.


### GCPs in ERDAS IMAGINE

Any ERDAS IMAGINE image can have one GCP set associated with it.  The GCP set is stored in  the image file along with the raster layers. If a GCP set exists for the top layer that is displayed in the Viewer, then those GCPs can be displayed when the Multipoint Geometric Correction tool (IMAGINE ribbon Workspace) or GCP Tool (Classic) is opened.



In the Cell Array of GCP data that displays in the Multipoint Geometric Correction tool or GCP Tool, one column shows the point ID of each GCP. The point ID is a name given to GCPs in separate files that represent the same geographic location. Such GCPs are called corresponding GCPs.



A default point ID string is provided (such as GCP #1), but you can enter your own unique ID strings to set up corresponding GCPs as needed. Even though only one set of GCPs is associated with an image file, one GCP set can include GCPs for a number of rectifications by changing the point IDs for different groups of corresponding GCPs.


### Entering GCPs

Accurate GCPs are essential for an accurate rectification. From the GCPs, the rectified coordinates for all other points in the image are extrapolated. Select many GCPs throughout the scene. The more dispersed the GCPs are, the more reliable the rectification is. GCPs for large-scale imagery might include the intersection of two roads, airport runways, utility corridors, towers,  or buildings.  For small-scale imagery, larger features such as urban areas or geologic features may be used. Landmarks that can vary (for example, the edges of lakes or other water bodies, vegetation, and so forth) should not be used.


The source and reference coordinates of the GCPs can be entered in the following ways: GCPs in IMAGINE Files.



GCPs that are digitized in a Viewer are stored with the raster data that are opened in the Viewer. However, GCPs can also be recorded from a digitizing tablet or straight from the keyboard. In these cases, they are stored alone in IMAGINE files with the extension _.gcc_.



The input image file can be set to:

* **Existing Viewer**

* **Image Layer (New Viewer)**
(Use the mouse to select a pixel from an image in the Viewer. With both the source and reference Viewers open, enter source coordinates and reference coordinates for image-to- image registration. The Multipoint Geometric Correction tool contains the both the source and reference Viewers within the tool)

* **Vector layer (New Viewer)**

* **Annotation Layer (New Viewer)**

* **GCP File (.gcc)**


(Use an existing Ground Control Coordinates file (.gcc file extension). This file contains the X and Y coordinates along with the GCP point ID, saved as an external file.)

* **ASCII File**

* **Digitizing Tablet (Current Configuration)**


Use a digitizing tablet to register an image to a hardcopy map.

* **Digitizing Tablet (New Configuration)**

* **Keyboard Only**


(They may be known a priori, and entered at the keyboard. To enter or edit a GCP from the keyboard, use the Cell Array of GCP coordinates. The X Source, Y Source, X Dest, and Y Dest cells are editable. When you edit a GCP in the Cell Array, the GCP will move in the Viewer if it is opened)


## Map Georeferencing

1. From the Main Icon Panel select the File option and select open from the file menu you have to select raster layer. In the dialog box that appears, select the file From Image File radio button and then select file.img. Click OK. This is the image that has not been georeferenced.
2. You know have a choice of geometric models. From the list of Geometric Models, select
Polynomial and click OK .

![Setting Polynomial as geometric model](/en/basics/georeferencing/images/1.png?classes=shadow)


3. Select the Projection Tab. Since a projection has not yet been defined, no projection will appear. Select the Set Projection from GCP Tool button. A dialog box will appear that gives you choices for the reference input.
4. Click Apply and Close to the Polynomial Model Properties dialog box.  You  would only need  to save the model parameters if you were performing repeated rectification .

![Projection chooser dialog box](/en/basics/georeferencing/images/2.png?classes=shadow)

From the GCP Tool Reference setup dialog box Select Keyboard only .

![ GCP Tools Reference Setup dialog box](/en/basics/georeferencing/images/2a.png?classes=shadow)

5. Move both link boxes so that they cover a common identifiable point feature. This feature should now be seen in both chip viewers. From the GCP Editor Tool bar click the Keep Current Tool icon. Then click the Create GCP icon. Now digitize the common point in each of the chip viewers. Once this is done you will need to click on the Select GCP icon to click and drag the link boxes to other identifiable features.
6. In order to make your GCPs stand out visually, you may want to change their display color. From the GCP Tool Color column, click and select a desired color for all or individual GCPs.

7. You have to select 4 GCPs. Remember to distribute the GCPs evenly throughout the image. Editing out unwanted GCPs is possible through the Cell Array. First select the point and then using hidden functions in the first column, select Delete Selection.
8. When you are satisfied with the accuracy of your GCPs, you can save them. Select File/Save Input. Select/Save Reference. You may need to click yes to saving the GCP tables and they will be added as another no in the .img file structure.
9. From the Geo Correction Tools dialog, click the Display Resample Image Dialog icon .

![Resample image icon](/en/basics/georeferencing/images/rectify.png?classes=shadow)

 In the Resample dialog box  enter the Output file name xrectify.img. For the Resample Method use Neighborhood / Bilinear Interpolation. Click on the Ignore Zeros in Stats. Check box. Ensure that the projection information is displayed at the top of the dialog. Click OK to start the rectification.
 
 
![Resampling dialog box](/en/basics/georeferencing/images/3b.png?classes=shadow)

10. When the job is done click OK on the status box. Then close all the Geo Correction dialogboxes.   If you have made any changes to the GCP Editor after the last save,  then you will   be prompted to save the edits. Click yes to saving current Geometric Model and name it xrectify.gms. In the viewers that remain, display xrectify.img in the viewer that contains the previously unrectified image and leaves the  viewer as is.


## Map to Image georeferencing

When rectifying an image, you will use ERDAS IMAGINE to:

* record **ground control points (GCPs)**
* compute a **transformation matrix**, and use that transformation matrix and a **resampling** method to rectify the image.

If you are **reprojecting** georeferenced data from one map projection to another, there is a shortcut for generating GCPs and calculating a transformation matrix using a reprojection  grid.

### steps

* Open **Satellite Image** in ERDAS IMAGINE 2013 
![ERDAS IMAGINE 2013 containing both Satellite image and Toposheet](/en/basics/georeferencing/images/map/viewer.png?classes=shadow)

* Then select **Multispectral → Control points**.


In the dialog box appears, select **Polynomial** as Geometrical model.

* From the dialog box appears click on **Image Layer** 


![Dialog box showing GCP Tool reference setup](/en/basics/georeferencing/images/map/imagelayer.png?classes=shadow)

* Then select required** Reference Map / Toposheet **(All file based raster format and Click OK. Then a dialog box named Polynomial Data Properties appears.

* In the Projection section select** Add/Change Projection**. 


A **Projection Chooser** tab appears .

![ Dialog box showing Projection setup where Projection and Zone can be selected](/en/basics/georeferencing/images/map/projection.png?classes=shadow)

* Select **UTM WGS 84 → Zone 43**, then select **Close**.



A new window containing both Satellite Image and Toposheet appears.

* Then select **create GCP tool**.

![ GCP tool](/en/basics/georeferencing/images/map/gcptool.png?classes=shadow)

* Click on dominant feature (Junctions, Road, and similar permanent objects) first on the Toposheet and then on Satellite image.
* Select such **four GCPs** .


_Each GCP point clicks create a new Row on the bottom of the window comprising Lat and Long values_.


* Select **Display Resample Image Dialog**.
* **Name the Output file** after selecting **Nearest Neighbour** as Resampling method.

![Dialog box showing Resampling options including Resampling method and Output file selection](/en/basics/georeferencing/images/map/Resampling.png?classes=shadow)
