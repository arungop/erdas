---
date: 2020-08-05T16:50:16+02:00
title: Supervised classification
weight: 25
---
In supervised classification the image analyst supervises the pixel categorization process. In this approach, the users define useful information categories and then examine their spectral separability. This classification consists of three stages: Training stage, Classification stage and Output stage. Accuracy assessment is required to get an accurate classification.

## Training
In this stage, the analyst identifies representative training sites/areas (i.e., a particular land cover type), then the computer determines the spectral signatures of the pixels within each training are,and uses this information to define the mean and variance of each of the classes. The training stage requires close interaction between the image analyst and the image data. It also requires substantial reference data and a thorough knowledge of the geographic area to which the data apply. The more time and effort spent in collecting training site the better the classification results. To yield acceptable classification results, training data must be both representative and complete.



### Creating signature set
1. Open Erdas Imagine

2. Open satellite image (‘satdec.img’ (Landsat 8 OLI)) image in the viewer. **File → open →
select satellite image → Ok** .

![Satellite image in the Erdas imagine viewer](/en/classification/supervised/images/1.png?classes=shadow)
3. Subset the area of interest and change bands (True colour to False colour). To change bands: Multispectral → set layer- 3, 2, 1.

![False colour image representation after changing multispectral order - 3,2,1](/en/classification/supervised/images/2.png?classes=shadow)
4. Click on **Raster tab → Supervised → Signature Editor**.
A new ‘Signature Editor’ window will open .

![Signature editor in Supervised option](/en/classification/supervised/images/3.png?classes=shadow)

![ Signature editor tab dialog box ](/en/classification/supervised/images/3a.png?classes=shadow)

5. Now go back up to the top of the screen and click on **Drawing tab → Polygon Icon**

![Drawing toolbox ](/en/classification/supervised/images/4.png?classes=shadow)



6. Zoom the image. Click once within the water to start the polygon and then keep clicking to draw a polygon. These do not have to be large polygons but make sure that all the pixels within the polygon are of water. To finish the polygon just double click. **An AOI (Area of Interest) layer is formed**.

![ AOI layer formed on the Satellite image](/en/classification/supervised/images/5.png?classes=shadow)

7. Bring up the Signature Editor window and click on the button with a + sign and an arrow (+ ) (Create new Signature(s) from AOI . This will add the polygon just created.

![ Create new signature from AOI button](/en/classification/supervised/images/6.png?classes=shadow)


8. Repeat steps 5,6 and 7 for the rest of water. Increase in number of samples (AOI layer), will increase the accuracy of classification.
9 .Repeat the steps as water for rest of the classes (vegetation, grassland).

10. Once the preferable numbers of sample is selected the Signature Editor window should look like the image below.

![ Preferable numbers of sample is selected in the Signature Editor window](/en/classification/supervised/images/7.png?classes=shadow)



### Classification Stage


In classification, each pixel in the image data set is categorized into the land cover class it most closely resembles. If the pixel is insufficiently similar to any training data set, it is usually labeled ‘unknown’. After all pixels in the input image have been categorized, the results are presented in the output stage.


1. Click and hold on class 1, which is under the column ‘Class #’, and move the mouse down to the end of one class and then release.
2. This will highlight all of the samples in a single class just created and then click on the button
with three bars and the arrow (5th symbol in the tool bar) (merge selected signatures) to combine all the samples.


A new class should appear which a combination of all the samples collected .

![ Highlighting similar classes to a single class](/en/classification/supervised/images/8.png?classes=shadow)


3. Right click on any of the numbers in the selection and then click Delete Selection to delete   the samples since they are now combined into ‘new Class’. Rename the new class as ‘Water body’. Repeat the same for other classes (vegetation, grassland) also .

![Combined similar classes into three classes](/en/classification/supervised/images/9.png?classes=shadow)

4. Once completed, save signature set. **File → Save As** in the Signature Editor window. A new popup window **Signature File As** appear choose save place → Ok .

![Saving Signature file as .sig format](/en/classification/supervised/images/10.png?classes=shadow)


### Output

Output products are in the form of thematic maps, tables of statistics for the various land cover classes and digital data files amenable to inclusion in a GIS (GIS input).

1. Click on Raster → Supervised → Supervised classification
Define: Input file, input Signature file (Saved signature file ‘signature.sig’), Classified file (Out- put file (Select Save place).

![Raster file and Signature file are entered in this input dialog box](/en/classification/supervised/images/11.png?classes=shadow)


2. Enter Ok. A new process list window will appear, close it after the process is completed .

3. Open saved file .

![Output of Supervised Classification](/en/classification/supervised/images/13.png?classes=shadow)




