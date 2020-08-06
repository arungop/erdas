---
title: Processes in digital image processing
weight: 10
disableToc: true
---

## Preprocessing

These operations aim to correct distorted or degraded image data to create a more faithful representation of the original scene and to improve an image’s utility for further manipulation later on. This typically involves the initial processing of raw image data to eliminate noise removal, radiometric correction, geometric correction, and image subsetting, layer stacking and mosaicking.


## Image Enhancement
The primary goal of image enhancement is to improve the visual interpretability of an image  by increasing the apparent distinction between the features in the scene. Most enhancement techniques may be categorized as either point or neighborhood operations. Point operations modify the brightness value of each pixel in an image data set independently. Neighborhood operations modify the value of each pixel based on neighboring brightness values. Either form of enhancement can be performed on single-band (monochrome) images or on the individ-  ual components of multi-image composites. The resulting images may also be recorded or displayed in black and white or in color. Choosing the appropriate enhancement(s) for any particular application is an art and often a matter of personal preference.

## Feature Extraction


Image interpretation keys such as size, shape, texture, pattern, tone/colour, shadow, location and spatial association are used to extract features from imagery.

## Classification

The overall objective of image classication procedures is to automatically categorize all pixels in an image into land cover classes or themes.  Often this is done using spectral patterns;   that is, pixels that share similar combinations of spectral reectance or emissivity are grouped together in classes that are assumed to represent particular categories of surface features.  No attention is paid to the neighbors or surroundings of the pixel being classied. The term spectral pattern recognition refers to the family of classication procedures that utilizes this pixel by-pixel spectral information as the basis for automated land cover classication. This is  of two types: Supervised and Unsupervised classification. In contrast, the decision rules may be based on the geometric shapes, sizes, and patterns present in the image data. These procedures fall into the domain of spatial pattern recognition. Hybrid methods (object-based image analysis (OBIA)), in which both spatial and spectral patterns are used for classication, are increasingly common.

## Post processing

Post-processing is the process of adjusting a previously-captured image to obtain a desired look. It encompasses everything from simple whole-image adjustments to detailed per-pixel touch-up work. Post-processing techniques are filtering and change detection.

## Accuracy Assessment

One of the most important final steps at classification process is accuracy assessment. The aim of accuracy assessment is to quantitatively assess how effectively the pixels were sampled into the correct land cover classes. Accuracy assessments are commission and omission error, sensitivity and specificity, positive and negative predictive power and Kappa statistics. Accuracy assessment can be done by ground truthing, compare with high resolution image, Google earth and Google Map.

### Digital image processing softwares
Digital image processing (DIP) is carried out by using softwares such as ERDAS IMAGINE, ENVI. Here ERDAS IMAGINE software is used for the processing of digital images. ERDAS IMAGINE is an image processing software package that allows users to process both geospatial and other imagery as well as vector data. Erdas can handle multi-spectral imagery, hyperspectral imagery and LiDAR from various sensors. Erdas also offers a 3D viewing module (VirtualGIS) and a vector module for modeling. The native programming language is EML (Erdas Macro Language). Erdas is integrated within other GIS and remote sensing applications and the storage format for the imagery can be  read in many other applications (*.img files).
