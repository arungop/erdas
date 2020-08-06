---
date: 2020-08-05T16:50:16+02:00
title: Unsupervised classification
weight: 25
---
Unsupervised classifiers do not utilize training data as the basis for classification. Rather, this family of classifiers involves algorithms that examine the unknown pixels in an image and aggregate them into a number of classes based on the natural groupings or clusters present in the image val- ues.Hence it is also called as clustering.


The classes that result from unsupervised classification are spectral classes. Identity of the spectral classes will not be initially known.   The analyst must compare the classified data with some form    of reference data to determine the identity. There are numerous clustering algorithms that can be used to determine the natural spectral groupings present in a data set. One common form of clus- tering,called the **K-means approach**,accepts from the analyst the number of clusters to be located in the data.


A widely used variant on the K-means method for unsupervised clustering is an algorithm called Iterative Self-Organizing Data Analysis Techniques. The **Iterative Self Organizing Data Analysis
–ISODATA** clustering method uses spectral distance and iteratively classifies the pixels. After each iteration, ISODATA redefines the criteria for each class, and classifies again, gradually “discovering” the spectral distance patterns (i.e., the clusters)in the data.

### Steps
To perform Unsupervised Classification of a Multispectral Image in Erdas Imagine.

1. Open up the layer stacked Liss 4 image in Erdas Imagine.

2. Click on the **Raster tab → Classification → Unsupervised button → Unsupervised Classification** 

![Unsupervised classification tool in Classification tab](/en/classification/unsupervised/images/1.png?classes=shadow)

3. **A dialogue box will appear.Enter input raster file name and output cluster layer file name.**




Here Cluster options given as 80 Classes and 20 maximum iterations.
After entering values click **OK** button .Then, Process list dialogue box will appear. After processing Open the saved output image .

![Setting clusterring and processing options](/en/classification/unsupervised/images/2.png?classes=shadow)

4. Open attribute table.
Right-click for pop-up menu Select → **Display Attribute Table**.

5. **To identify the feature**


Click **Home tab → inquire button** → a dialogue box will appear as follows . Dialog box provide information about pixel value and class names .

![Inquire button to check pixel value](/en/classification/unsupervised/images/3.png?classes=shadow)

6. In order to identify a feature,compare the location with **Google Map**.
After comparing we can able to identify the exact class of the given feature.

7. For example , Here class 11 shows the pixel value of water body.

![Marking Class name as Waterbody](/en/classification/unsupervised/images/4.png?classes=shadow)


So we named the class 11 as “water body" in the attribute table and in order to identify it, the **colour also changed**.

8. In similar way we identify another class as vegetation. After comparing 80 classes with Google map the results: 

![Matching exact location using Google Earth](/en/classification/unsupervised/images/5.png?classes=shadow)


#### Masking-Correction in Spectral Signature

Here some classes show exact spectral signature of another one (_For example - Rock show same spectral signature of water body_.)



In order to change selected class number to another class we use ” **Thematic Recode**”  Select the **particular cell → create aoi layer → Drawing tool **_Draw the cell_

![Recode tool in Thematic tab ](/en/classification/unsupervised/images/6.png?classes=shadow)

9. Click on **Thematic button → Recode → Pop up window** will appear. Inside that dialogue box,

Click **New Value → Formula → vegetation as 1 Click OK**


Selected cell will change into same spectral signature of vegetation.**In similar method re- maining also corrected**.


10. After masking, to sort the given classes:
Click on** Raster tab → Thematic → Recode **→ click on “**Setup Recode**” button → A  dialog box will appear .

![Setup recode and Sorting in Thematic recode tab](/en/classification/unsupervised/images/7.png?classes=shadow)


Inside dialogue box → click on → **New Value → Sort → Sort by name**


11. After sorting, Value of each class are entered into the **”New value” column → click OK**



In recode dialogue box also Click OK.Processing of above take place and Process List dia- logue box will appear.


**Open the saved file.Attribute table appear and only main classes will appear**.Change  the colour according to class and save the layer.

![Attribute table before changing the colour based on the classes](/en/classification/unsupervised/images/8.png?classes=shadow)

Attribute table before ( above one ) and after ( below one ) changing the colour based on the classes

![Attribute table after changing the colour based on the classes](/en/classification/unsupervised/images/9.png?classes=shadow)


Table showing Class Name and their Value

| Class Name  |  Value |
|---|---|
| Barnen  | 1  |
| Planatation  | 2  |
| Urban  |  3 |
| Vegetation  |  4 |
|  Waterbody |  5 |


12. To insert Class names on the Attribute table
Click on **Table → Add Class Name** and hence class names also added.

![Class names based on the table ](/en/classification/unsupervised/images/10.png?classes=shadow)


13. After entering Class names, **_Save the layer and the classification of given area is done_**.



Five class names entered are **Barren,Plantation,Urban,Vegetation and Water body**.
