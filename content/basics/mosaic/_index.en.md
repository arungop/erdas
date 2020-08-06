---
date: 2020-08-05T16:50:16+02:00
title: Mosaic
weight: 25
---
**Mosaicking** is a final step in the image preprocessing sequence often involves **subsetting** the image to reduce the data volume, **layer stacking** to combine multiple separate bands or layers in a single image, and/or mosaicking multiple images to cover a broader area.



**Subsetting** may be used to reduce the spatial extent of an image, cropping the image to cover only the specific area of interest, and it may also involve selecting only certain spectral bands.



The **subset images** need to be precisely georeferenced so that after Mosaicking the boundary between two subsets can be avoided.


## Steps

Once opened, from the View group on the Home tab select the Swipe tool to easily see where the two images overlap.



Now start the mosaic workflow.


* From the Raster tab, select **Mosaic → Mosaic Pro**.
![MosaicPro tool from the Raster tab](/en/basics/mosaic/images/step1.png?classes=shadow)

* Add **two Subset images** (Georefereced images).
![Add images tool in MosaicPro tab](/en/basics/mosaic/images/step2.png?classes=shadow)
* If necessary, navigate to the directory that contains the first image, select it but do not click OK.

* Add **two subset images → Process → Run mosaic**.

![Run mosaic option in the process menu](/en/basics/mosaic/images/step3.png?classes=shadow)
* Moasaic image will be saved in the output folder.
