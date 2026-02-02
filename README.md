# Karst Hazard and Infrastructure Exposure  
St. Louis Metropolitan Area

## Overview

![Karst Hazard Map](layouts/stl_karst_hazard_map.png)


[Download full-resolution map (PDF)](layouts/stl_karst_hazard_map_layout.pdf)






This project uses **GIS-based spatial analysis** to evaluate **relative karst hazard potential** and **infrastructure exposure** in the St. Louis metropolitan area.

The map integrates **bedrock geology**, **sinkhole point data**, **terrain derivatives**, and **transportation infrastructure** to identify areas of elevated karst-related risk. A **Kernel Density Estimation (KDE)** of sinkholes is used to derive a relative karst hazard surface, which is then interpreted alongside geologic and hydrologic context.

---

## Objectives
- Identify spatial clustering of sinkholes using kernel density estimation
- Provide geologic contetx for karst development using bedrock units
- Visualize potential overlap between karst-prone areas and major transportation infrastructure
- Demonstrate applied GIS and geoscience workflows in QGIS

---

## Data Sources

- **USGS Bedrock Geology** (1:100,000 and 1:500,000 scale)

- **Missouri Geological Survey** – Sinkhole Inventory

- **Missouri Spatial Data Service**

  - Major highways (filtered to interstates, U.S. highways, and state highways)

  - Gaining and losing streams (losing streams subset)

- **USGS 1/3 Arc-Second DEM** (ScienceBase Catalog)

- **OpenStreetMap** basemap for reference

---

## Methods & Spatial Analysis

- Reclassified bedrcok geology into karst-relevant categories using **attribute-based SQL CASE statements**
- Integrated **multi-scale geologic datasets** (100K and 500K) to ensure full spatial coverage
- Generated **hillshade** from DEM for terrain context
- Performed **Kernel Density Estimation (KDE)** on sinkhole locations to derive a relative karst hazard surface
- Applied **zonal statistics** by county (St. Louis City, St. Louis County, Jefferson County, and Franklin County)
- Designed a **three-pane cartographic layout** to separate:
  - Geologic context
  - Observed karst features
  - Derived hazard and infrastructure exposure

---

## Key Skills Demonstrated

- GIS and spatial analysis (QGIS)
- Raster and vector geoprocessing
- Kernel Density Estimation (KDE)
- Terrain analysis (DEM, hillshade)
- Attribute-based classification
- Cartographic design and layout
- Geologic hazard mapping
- Infrastructure exposure analysis

---

## Outputs
- High-resolution cartographic layout (PNG/PDF)
- Reproducible GIS workflow
- Documented data sources and processing decisions
- GDAL (via QGIS Processing)

---

## Notes

This project is intended as a **portfolio demonstration of applied GIS and geoscience analysis**, not a regulatory hazard assessment 

---

### Future Improvements
- Incorporate **sinkhole size and occurrence dates** to weight the Kernel Density Estimation and explore temporal trends in karst activity
- Integrate **additional hydrologic variables** (e.g., groundwater levels or precipitation intensity) to refine hazard interpretation
- Perform **network-based proximity analysis** to quantify infrastructure exposure along major transportation corridors
- Expand zonal statistics to include **municipal or watershed boundaries** for more granular spatial comparison
- Automate portions of the workflow using **PyQGIS or Python scripting** to improve reproducibility



