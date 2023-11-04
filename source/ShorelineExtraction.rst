.. _shorelineextraction:

Shoreline Extraction
===============================

 The development of this plugin has been specifically designed to extract shorelines utilizing a flexible approach, making use of both radar and optical imagery sources. The selection of which type of imagery to use is contingent upon the particular focus and requirements of the user. 

Extraction with Optical Imagery
--------------------------------
 
 Shoreline Extraction using optical imagery is configured to follow the following steps.
 
    * :ref:`Download multiband Sentinel 2 Imagery <downloadimagery>`
    * Load the Image onto QGIS
    * On the plugin select **Extract Shoreline >>** :ref:`**Automatic Shoreline Extraction** <shorelineextractionoptical>`
    * Run the plugin

.. _downloadimagery:

Download Optical Imagery
_________________________

 Multiband Sentinel 2 Images at a resolution of 10m are downloaded with the help of the *earthengine-api*. The result is an image with **4 bands**, that is, *Red,Green, Blue and NIR*. For shoreline extraction, the NIR band is of importance. The Red, Green and Blue band can be used to create a basemap for confirmation.

 .. figure:: ./Images/Download.png
    :alt: Download Imagery on the plugin
    :align: center
   
    *Figure 1: Image Downloader Page*

 The *Image Downloader* takes 4 parameters. That is :-

 1. **Bound** - This is a vector representation of you area of interest. The file format is limited to Esri Shapefiles.
 2. **Start Date** - This is the beginning of the analysis period. 
 3. **End Date** - This is the end of the analysis period
 4. **Output Directory** - This is the folder in which the image will be stored.

 .. admonition:: Note!

    - The image being downloaded is **Sentinel 2A**. This means that the analysis period is limited to **2015 - present**.
    - The plugin may create additional directories in your output folder. You can delete them after the image has been downloaded.

.. _shorelineextractionoptical:

Shoreline Extraction
_________________________

 Shoreline extraction with optical imagery uses the Near Infrared band to delineate land and water masses. It takes a singleband or multiband raster image from which the
 Near Infrared band can be selected for use in the analysis. The output is a **GeoJSON** file with a polygon showing the land mass including the shoreline. From this, the shoreline can be extracted.

 .. figure:: ./Images/Optical.png
    :alt: Shoreline Extraction with Optical Imagery
    :align: center

    *Figure 2: Shoreline Extraction with Optical Imagery*

 Automatic Shoreline Extraction with optical imagery takes 3 parameters. That is:

 1. **Multiband Raster** - This is the image that was initially downloaded from the image downloader. For purposes of consistency, please use the downloaded image.
 2. **NIR Band** - The plugin counts the number of bands in the multiband raster image. You will be required to select the band number that represents the NIR band.
 3. **Output Foder** - This is the directory where you want to save the extracted shoreline. 


.. _sarextraction:

Extraction with SAR Imagery
----------------------------

 This method of shoreline extraction uses **Synthetic Aperture Radar** imagery from **Sentinel 1** to delineate water masses. The result is a **GeoJSON** file showing the edges from which shorelines can be estimated.
 This tehnique uses the **earthengine-api** meaning the image doesn't necessarily have to be within your local directory. You only have to provide a **gridded** shapefile showing your Area of Interest (AOI).

 .. figure:: ./Images/SAR.png
    :alt: Shoreline Extraction with SAR imagery
    :align: center

    *Figure 3: Shoreline Extraction with Optical Imagery*


 This method of shoreline extraction takes 4 parameters. That is:

 1. **Bound** - This is a **gridded** shapefile showing your area of interest. 
 2. **Start Date** - This is the beginning of your analysis period.
 3. **End Date** - This is the end if your analysis period.
 4. **Output Directory** - This is the folder that will hold the output results of your work.

 .. admonition:: Note!
   
   The bound in should be **gridded** to reduce download and processing time.


