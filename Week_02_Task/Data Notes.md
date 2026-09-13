# Week 2 Data Note

## Project Title

**Rural Healthcare Accessibility and Underserved Community Analysis in Adamawa State, Nigeria**

## Spatial Question

> Which rural settlements in Adamawa State are located more than 5 km by road from the nearest healthcare facility?

## Study Area

The study covers Adamawa State in North-Eastern Nigeria. The analysis will be conducted at the settlement and local government area levels.

## Overview of the Data

The datasets for this project were obtained from GRID3 and OpenStreetMap.

The GRID3 datasets originally covered Nigeria or multiple Nigerian states. They were downloaded as shapefiles, opened in QGIS and filtered to retain only the features within Adamawa State.

The road-network data was downloaded directly into QGIS from OpenStreetMap using the QuickOSM plugin. The temporary QuickOSM output was subsequently exported and saved as a permanent spatial file.

This data note records the following information for each dataset:

- Data source and source link
- Number of features
- Geometry type
- Missing values, gaps and other data-quality observations

---

## 1. Adamawa State Boundary

### Description

The state-boundary dataset defines the overall study area. It will be used to clip or filter all other datasets to Adamawa State.

### Source and Format

- **Dataset:** GRID3 Nigeria Operational States
- **Source:** GRID3
- **Source URL:** https://data.grid3.org/
- **Original coverage:** Nigeria
- **Extracted coverage:** Adamawa State
- **Downloaded format:** Shapefile
- **Geometry type:** Polygon
- **Number of features in the original dataset:** `[Insert count]`
- **Number of features after extracting Adamawa State:** `1`


### Processing Performed

The national state-boundary shapefile was opened in QGIS. Adamawa State was selected from the attribute table and exported using **Save Selected Features As**. The extracted layer was saved as a separate shapefile.

### Gaps and Missing Values

The extracted layer contains one polygon representing Adamawa State. `[No missing values were identified in the key fields / Insert the fields containing missing values.]`

Visual inspection showed `[no obvious gaps or geometry problems / describe any gaps, overlaps or invalid geometry noticed]`.

---

## 2. Adamawa Local Government Area Boundaries

### Description

This dataset represents the local government areas within Adamawa State. It will be used to summarise healthcare accessibility and potentially underserved settlements by LGA.

### Source and Format

- **Dataset:** GRID3 Nigeria Operational Local Government Areas
- **Source:** GRID3
- **Source URL:** https://data.grid3.org/
- **Original coverage:** Nigeria
- **Extracted coverage:** Adamawa State
- **Downloaded format:** Shapefile
- **Geometry type:** Polygon
- **Administrative level:** Admin Level 2



### Processing Performed

The national LGA layer was opened in QGIS. The attribute table was used to select all LGA features belonging to Adamawa State. The selected features were exported and saved as a separate shapefile.

### Gaps and Missing Values

The extracted dataset contains `[insert count]` LGA polygons. `[State whether all expected Adamawa LGAs are represented.]`


Any boundary gaps or overlaps will be considered when summarising results by LGA.

---

## 3. Adamawa Ward Boundaries

### Description

This dataset represents operational ward boundaries in Adamawa State. It provides a more detailed administrative layer for examining the distribution of settlements and healthcare facilities.

### Source and Format

- **Dataset:** GRID3 Nigeria Operational Wards
- **Dataset version:** `[Insert version shown on GRID3]`
- **Source:** GRID3
- **Source URL:** https://data.grid3.org/
- **Original coverage:** Selected states in Nigeria, including Adamawa State
- **Extracted coverage:** Adamawa State
- **Downloaded format:** Shapefile
- **Geometry type:** Polygon
- **Administrative level:** Admin Level 3



### Processing Performed

The operational ward dataset was opened in QGIS. All wards belonging to Adamawa State were selected from the attribute table and exported as a separate shapefile.

### Gaps and Missing Values

A visual inspection of the Adamawa ward layer showed `[visible overlapping boundaries]`.

The following issues were identified:

- **Boundary gaps:** `[None observed / describe locations.]`
- **Overlapping polygons:** `[None observed / describe locations.]`
- **Missing ward names:** `[0]`
- **Missing ward codes:** `[0]`
- **Other missing attributes:** `[“None identified.”]`

These limitations may affect analysis performed at ward level.

---

## 4. Healthcare Facilities

### Description

This dataset contains the geographic locations of healthcare facilities in Adamawa State. It will be used to identify the nearest healthcare facility to each rural settlement.

### Source and Format

- **Dataset:** GRID3 Nigeria Health Facilities
- **Dataset version:** `[Insert version shown on GRID3]`
- **Source:** GRID3
- **Source URL:** https://data.grid3.org/
- **Original coverage:** `[Nigeria / selected Nigerian states]`
- **Extracted coverage:** Adamawa State
- **Downloaded format:** Shapefile
- **Geometry type:** Point



### Processing Performed

The health-facility shapefile was opened in QGIS. Facilities located within Adamawa State were selected and exported as a separate layer.

The extracted layer was visually compared with the Adamawa State, LGA and ward boundaries to confirm that the facility points fell within the study area.

### Gaps and Missing Values

The GRID3 health-facility dataset should not automatically be treated as a complete list of every healthcare facility in Adamawa State. The layer represents the facilities recorded when the dataset was compiled or updated.


Some existing facilities may be absent, incorrectly located, duplicated or no longer operational. These limitations will be considered when interpreting the final accessibility results.

---



## 5. Road Network

### Description

The road-network dataset contains roads and paths within Adamawa State. It will be used to determine road connections and calculate the distance between settlements and healthcare facilities.

### Source and Format

- **Dataset:** OpenStreetMap road network
- **Source:** OpenStreetMap
- **Source URL:** https://www.openstreetmap.org/
- **Retrieval tool:** QuickOSM plugin in QGIS
- **QuickOSM key:** `highway`
- **QuickOSM value:** `[Blank/all values, or insert the selected road class]`
- **Query extent:** Adamawa State
- **Downloaded geometry:** Lines and multilines
- **Saved format:** `[Shapefile]`
- **Geometry type:** LineString/MultiLineString


### Processing Performed

The QuickOSM plugin was installed and opened in QGIS. The `highway` key was used to request road features from OpenStreetMap within the Adamawa State boundary.

The query returned temporary point, line, multiline or multipolygon layers depending on the available OSM features. The relevant road line layer was retained.

Because QuickOSM outputs are temporary scratch layers, the road layer was exported using **Save Features As** and saved as a permanent `[Shapefile]`.



## Overall Data Observations

The datasets were successfully downloaded, opened and inspected in QGIS. The GRID3 datasets provided the administrative boundaries, settlement information and healthcare-facility locations required for the project. OpenStreetMap provided more current road-network data through QuickOSM.

The main issues identified during the initial inspection were:

- Possible gaps or overlaps in some operational boundaries.
- Missing values in some healthcare-facility attributes.
- Possible omissions or outdated records in the healthcare-facility dataset.

Before distance analysis, all layers will be checked, cleaned and projected into an appropriate metric coordinate reference system.

