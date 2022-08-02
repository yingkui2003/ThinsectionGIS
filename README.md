# ThinsectionGIS: An ArcGIS model to delineate grain boundary from thin section photos
This document provides a guide on how to perform thin section GIS analysis using ArcGIS Modelbuilder. The ArcGIS used in the analysis should have ArcInfo license, support spatial analysis extension and with version of 9.1 or later. 

# How to download and use this toolbox in ArcGIS or ArcGIS Pro
The github site includes a GIS model file (Thin Section GIS.tbx) and three thin section images taken from different angles (-15, 0, +15). These image files will provide an example of the thin section GIS analysis. You can also find a pdf file of the instruction and a published paper about this toolbox.

![image](https://user-images.githubusercontent.com/24683137/182475181-006e8429-384e-4683-b47a-9f5f7778686a.png)


A zip file of the while github folder will be downloaded to the local computer. Unzip this file will create a ThinsectionGIS-main folder with both the tbx file and all other files. Note that the original models were developed in ArcGIS 9.1 and some functions may need to change or replaced using other functions in the recent versions of ArcGIS or ArcGIS Pro. Please report any errors or questions to Yingkui Li (yli32@utk.edu).

# Load the GIS model into ArcGIS

Unzip the zipped file into a folder your computer. This folder is the place you perform the thin section GIS analysis. If you want to run the analysis using your own thin section images, it is better to put your own thin section images into this folder. 

Open the ArcGIS and make sure the ArcToolBox is available. In the ArcToolBox, right click the “ArcToolBox” and choose “Add Toolbox…”. Then, an Add Toolbox Dialog shows up, you can browse the folder with the GIS model and choose the GIS model to add it into the ArcToolBox. The following figure shows how to do this step in ArcGIS.

![image](https://user-images.githubusercontent.com/24683137/182475379-4295f105-a3d8-4c6a-9421-21ab1f4b490d.png)


You can also find this toolbox in the Catalog Panel and you can run the tools by double clicking the tools there.

# Thin section GIS model

After you add the toolbox into the ArcToolBox, you will see a new toolbox (Thin Section GIS) in the ArcToolBox. This toolbox includes three GIS models. Please read the paper published in the Journal of Structural Geology for detail description of these models. The “Single Image/Raster Boundary” is for the process of extract boundary (1/0 values for boundary and inside grain) for a single image or a single band of the image. The “Noise Reduction” is to reduce the noise of the image in order to extract the grain boundary. The “Thin Section Analysis(3 Images)” model is a whole model to perform the thin section GIS analysis based on three images taken from different angles (same with the published paper).

![image](https://user-images.githubusercontent.com/24683137/182475444-802ce392-6fe6-49ea-bf84-4ee122b666c3.png)



# Thin Section Analysis (3 Images) Model

If you double click the “Thin Section Analysis (3 Images)” model, the model dialog will show up (the following figure), so you can assign your images into the model, specify the model output and adjust the model parameters.
![image](https://user-images.githubusercontent.com/24683137/182475579-0299f50f-b418-4628-af3d-af3a7279f1a8.png)


Basically, you need input three images taken from different angles. Each image will have three bands (RGB). So you have totally 9 input image bands. There are also two neighborhood windows for the filtering process inside the GIS model. The default value is 7 and 5. You can use these values when you first run this model, and you can also change these values to test the differences of the results. This model has two outputs: one the grain boundaries (line feature, shapefile), the other is the coverage of the grain polygons. To report these two features is because not all grain boundaries can close up and form the grain polygons. If you want to do additional editing work on the boundaries to make sure more grain polygons will be generated or get rid of some small polygons, you can edit the linear shapefile of the grain boundaries and then use the edited boundaries to generate the grain polygon coverage.

If you want to edit the model to change numbers of images used for the analysis, you can right click the model and choose “Edit”. The modelbuilder window will show up and show the model (See the following figure).

Following the help of the modelbuilder, you can easily add more thin section images in to the model and even adjust the steps of the analysis process.

# Single Image/Raster Boundary Model

This model is for the boundary extraction process of a single image or a single band of the image. This is a sub-model for the whole thin section GIS analysis. However, you can also run it individually and even modified it if you want to include more functions into the boundary extraction. The following figure shows this model.

# Noise Reduction Model
The “Noise Reduction” is to reduce the noise of the image in order to extract the grain boundary. This is also a sub-model for the whole thin section GIS analysis and you can also run it individually and modified it if you want. The following figure shows this model.

# Cite this work
Yingkui Li, Charles M. Onasch, Yonggui Guo, 2008. GIS-based detection of grain boundaries. Journal of Structural Geology 30(4), 431-443. https://doi.org/10.1016/j.jsg.2007.12.007.

# Contact info
Yingkui Li

Department of Geography & Sustainability

University of Tennessee

Knoxville, TN 37996

Email: yli32@utk.edu

Website: https://geography.utk.edu/about-us/faculty/dr-yingkui-li/

Google Scholar: https://scholar.google.com/citations?user=JoNuyCMAAAAJ&hl=en&oi=ao
