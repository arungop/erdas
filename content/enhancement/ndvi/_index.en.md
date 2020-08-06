---
date: 2020-08-05T16:50:16+02:00
title: Normalised Difference Vegetation Index(NDVI)
weight: 25
---
NDVI is a vegetation index to monitor the condition of vegetation or vegetation health. NDVI is the most commonly used vegetation index for monitoring vegetation globally. There are many other veg- etation indices such as Enhanced Vegetation Index (EVI), Ratio Vegetation Index (RVI) and Perpendicular Vegetation Index (PVI) that takes into account the soil emissivity (one of the major limitations of NDVI).


 To begin, open the NDVI dialog within the ERDAS IMAGINE.
 

![NDVI equation](http://www.sciweavers.org/tex2img.php?eq=NDVI%20%3D%20%5Cfrac%7BNIR%20-%20Red%7D%7BNIR%20%2B%20Red%7D%0A&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

Upon the classification of NDVI image in various ranges based on the NDVI value following significant information can be extracted from imagery.

1. Barren rocks, sand, or snow show very low NDVI values (**-0.1 to 0.1**)

2. Shurbs and grasslands or senescing crops (**– 0.2 to 0.5**)

3. Dense vegetation or tropical rainforest (**– 0.6 to 0.9**)

4. Deep water **(-1)**.

### Steps

* Click **Raster tab → unsupervised button → NDVI option**

![NDVI option in Raster tab](/en/enhancement/ndvi/images/ndvi.png?classes=shadow)


![Tab containing options for NDVI Index and file options](/en/enhancement/ndvi/images/index.png?classes=shadow)


* Dialogue box will appear. Give **input and output data**.

* Check the sensors were the appropriate information are taken. Select **index → ndvi → Select OK**.

* Comparison between Normal satellite image and NDVI are given below

![Satellite image obtained from USGS](/en/enhancement/ndvi/images/before.png?classes=shadow)


![NDVI](/en/enhancement/ndvi/images/after.png?classes=shadow)
