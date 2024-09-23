# topographic-basemap
#Author: Herenga ā Nuku GIS Team
#Date: Sepetember 2024.

# This repo contains example scripts used in this project by the Herenga ā Nuku Aotearoa GIS team to manage the topographic basemap used in Pocket Maps and other offlien ArcGIS Field App workflows. This basemap is published on ArcGIS Online here: https://walkingaccess.maps.arcgis.com/home/item.html?id=6a63808e8b434e13a96d326788bc45f8

#NOTE: Actual datasets, itemIDs, services and endpoints have been removed for privacy and security purposes. 

# The contents of this repo includes:
# 1. RunTask_MasterUpdateBasemapOffline.py
# 2. Update_Datasets.py
# 3. Update_VectorTileService.py
# 4. Update_OfflineAreas.py
# 5. WFS_Download.py

Description: 
RunTask_MasterUpdateBasemapOffline.py runs scripts 2-4 in sequence in order to update local featureclasses from hosted sources via WFS and/or ArcGIS Python API, generate a new .vtpk file from your ArcGIS Pro project and overwrite an existing vector tile service with it (project and target itemID must be specified), then finally any offline areas and webmaps using the vector tile service can be automatically updated (webmaps must be specified). Part of the Update_Datasets.py WFS process utilises the WFS_Download.py script to call each dataset in the list. 

How to use:
1. Downlaod to your local or virtual environment
2. Place in folder near your update.gdb and data.gdb, ensure all scripts are in the same folder. 
3. Install any packages listed that are not already present in your chosen python enviornment 
4. Create a new basemap in ArcGIS Pro and publish it to ArcGIS Online via the vector tile workflow: https://pro.arcgis.com/en/pro-app/latest/help/mapping/map-authoring/author-a-map-for-vector-tile-creation.htm
5. If using any datasets from external sources via WFS or ArcGIS webservices, use the Update_Datasets.py to list all datasets to be updated.
6. #Look through scripts 2-4 and update any variables that have " #Add your own" next to them (including your target Env - ensure you have the correct priveleges to perform edit/udpate actions to target items).
7. #Test the pipeline on a test/DEV service using the the RunTask_MasterUpdateBasemapOffline.py file.

If you have any questions about implementing this pipeline or creating / customising vector basemaps in ArcGIS, feel free to get in touch: gis@herengaanuku.govt.nz. 


