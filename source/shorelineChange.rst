.. _shorelinechange:

Shoreline Change Computation
=============================

 Once a user has obtained the shorelines, changes can be computed regardless of the technique chosen. 
 This section takes a baseline and comparison shoreline together with their respective years from which the rates of change can be computed.

 .. figure:: ./Images/SAR.png
    :alt: Shoreline Change Computation
    :align: center
    
    *Figure 5: Shoreline change computation*

 Shoreline change takes five parameters. That is:
 
 1. **Baseline Shoreline** - This is the shoreline at the beginning of you analysis period.
 2. **Baseline Year** - This is the year during which the baseline shoreline was generated.
 3. **Comparison Shoreline**- This is the shoreline to be used for comparison.
 4. **Comparison year** - This is the year during which the comparison shoreline was generated.
 5. **Output Directory**- This is the folder within which the shoreline change outputs will be stored.

 Shoreline change produces 4 files:

 * **Erosion** - This is poygon data showing the areas where the shoreline was eroded.
 * **Erosion Points** - This is point data highlighting the specific points where the shoreline was eroded. It also contains attribute data ``change_m`` showing the amount of erosion.
 * **Accreation** - This is polygon data showing the areas where accreation occured or simply where the shoreline grew.
 * **Accreation Points** - This is point data highlighting the specific points where the shoreline grew.It also contains attribute data ``change_m`` showing the amount of accreation.
 * **Shoreline Change** - This is a combination of ``erosion_points`` and ``accreation_points``. This quantifies the ``total shoreline change`` and ``change rates per year``. Negative changes indicate erosion while positie changes indicate accreation.
 
