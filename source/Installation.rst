.. _installations:

Installation
==============

Package Installation
---------------------

 The CoGEOS Shoreline Extraction plugin works with external python libraries when handling most of its analysis. 
 Therefore, before the plugn is installed, you would have to install all external libraries with the following procedure.
 
 1. Open the QGIS python console.
 2. Click on show editor |editor|.
 3. Paste the following code into the untitled file.
 4. Click run.

.. literalinclude:: ./codes/package_install.py
   :language: python
   :linenos:
    

.. |editor| image:: /Images/showeditor.png
    :scale: 70%

Install the Plugin
--------------------

 To install the plugin, follow the following procedure.

 1. Download the plugin zip :download:`here <shoreline_extraction_plugin.zip>`.
 2. Open the QGIS plugin manager
 3. Click ``install from ZIP``.

 .. figure:: ./Images/install.png
    :alt: Install from ZIP
    :align: center

    *Install plugin from the zip*

 4. Browse to the download directory.
 5. Install the plugin.