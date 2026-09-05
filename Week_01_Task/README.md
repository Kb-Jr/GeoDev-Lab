# Topic: Rural Healthcare Accessibility and Underserved Community Analysis in Adamawa State, Nigeria

## Project Brief

Access to healthcare remains difficult for many rural communities in Adamawa State because healthcare facilities are unevenly distributed, while some settlements are isolated by limited road connectivity and challenging terrain.

This project will use geospatial analysis to identify rural settlements with limited physical access to healthcare facilities. Accessibility will primarily be measured using the distance between each settlement and the nearest healthcare facility through the available road network.

Settlements located more than 5 km by road from the nearest healthcare facility will be classified as potentially underserved. Elevation and slope will also be examined to identify communities where difficult terrain may create additional barriers to healthcare access.

The results could support healthcare planning by showing communities where new facilities, improved roads or mobile healthcare services may be required.

## Spatial Question

> **Which rural settlements in Adamawa State are located more than 5 km by road from the nearest healthcare facility, and where does steep terrain create additional barriers to access?**

## Study Area

The study covers Adamawa State in North-Eastern Nigeria. The analysis will be conducted at the settlement and local government area levels.

## Required Datasets

### 1. Healthcare Facilities

This dataset will provide the names, locations and types of healthcare facilities in Adamawa State.

- **Source:** Nigeria Health Facilities – Humanitarian Data Exchange
- **URL:** https://data.humdata.org/dataset/nigeria-health-facilities

### 2. Road Network

The road-network dataset will be used to calculate the distance between rural settlements and their nearest healthcare facilities.

- **Source:** OpenStreetMap Nigeria Extract – Geofabrik
- **URL:** https://download.geofabrik.de/africa/nigeria.html

### 3. Settlements

This dataset will provide the names and geographic coordinates of villages, towns and cities in Adamawa State. It will be filtered using the Adamawa State boundary before the accessibility analysis.

- **Dataset:** Nigeria – Settlements (Villages, Towns and Cities)
- **Source:** Humanitarian Data Exchange
- **URL:** https://data.humdata.org/dataset/nigeria-settlements-villages-towns-cities

This point-based dataset is sufficient for measuring the road distance from each settlement to its nearest healthcare facility.

An alternative OpenStreetMap populated-places dataset is available at:

- **Alternative URL:** https://data.humdata.org/dataset/hotosm_nga_populated_places

### 4. Elevation Data

ALOS-PALSAR terrain data will be used to obtain elevation information and derive slope for identifying areas where difficult terrain may restrict access to healthcare.

- **Dataset:** ALOS-PALSAR Radiometrically Terrain-Corrected High-Resolution Product
- **Spatial resolution/pixel spacing:** 12.5 metres
- **Source:** Alaska Satellite Facility
- **Information URL:** https://asf.alaska.edu/datasets/daac/alos-palsar-radiometric-terrain-correction/
- **Download portal:** https://search.asf.alaska.edu/

### 5. Administrative Boundaries

The administrative-boundary dataset will provide the Adamawa State and local government area boundaries. It will be used to clip the other datasets and summarise underserved settlements by LGA.

- **Source:** United Nations Second Administrative Level Boundaries – Nigeria
- **URL:** https://salb.un.org/en/data/nga

## Proposed Outputs

- Map of healthcare facilities and rural settlements in Adamawa State.
- Road-based healthcare accessibility map.
- Map of settlements located more than 5 km from the nearest healthcare facility.
- Elevation and slope map showing potential terrain barriers.
- Summary of potentially underserved settlements by local government area.