.. _shorelineextraction:

Shoreline Extraction
===============================

 
.. _sarextraction:

Extraction with SAR Imagery
----------------------------

 This method of shoreline extraction uses **Synthetic Aperture Radar** imagery from **Sentinel 1** to delineate water masses. The result is a **GeoJSON** file showing the edges from which shorelines can be estimated together
 a modified version of the **SAR** image for validation purposes.
 This tehnique uses the **earthengine-api** meaning the image doesn't necessarily have to be within your local directory. You only have to provide a  shapefile showing your Area of Interest (AOI).

 .. figure:: ./Images/SAR.png
    :alt: Shoreline Extraction with SAR imagery
    :align: center

    *Figure 3: Shoreline Extraction with Optical Imagery*


 This method of shoreline extraction takes 4 parameters. That is:

 1. **Bound** - This is a shapefile showing your area of interest. 
 2. **Start Date** - This is the beginning of your analysis period.
 3. **End Date** - This is the end if your analysis period.
 4. **Output Directory** - This is the folder that will hold the output results of your work.

 .. admonition:: Note!
   
   This requires access to the internet.


