# Evapotranspiration Estimation Near Eppawala Phosphate Mine

Google Earth Engine (GEE) scripts developed for a final-year thesis estimating 
evapotranspiration (ET) patterns around the Eppawala Phosphate Mine, Sri Lanka, 
using satellite remote sensing and statistical analysis.

## Overview

This study estimates ET across distance buffer zones (0–3, 3–6, 6–9, 9–12 km) 
from the mine using the SEBAL (Surface Energy Balance Algorithm for Land) model, 
validates results against MODIS ET products, and applies land cover classification 
and trend analysis to characterize spatial and temporal ET patterns.

## Scripts

| File | Description |
|------|-------------|
| `classification_final.js` | Land cover classification (Water, Forest, Cropland, Bareland/Built-up) using Landsat 8 and Random Forest, with cropland patch selection across distance buffer zones |
| `SEBAL_ET_FINAL.js` | Monthly SEBAL evapotranspiration estimation using Landsat 8 surface reflectance, NDVI, albedo, and land surface temperature, with ERA5 radiation data and gap-filling |
| `MODIS_ET_FINAL.js` | Monthly ET extraction from MODIS MOD16A2GF product for validation against SEBAL estimates |
| `MANKENDALL_ANALYSIS.js` | Annual ET time series (2013–2025) and Mann-Kendall trend analysis across distance zones |

## Methodology

- **Classification:** Random Forest (500 trees) using spectral bands + NDVI/EVI/SAVI
- **ET Model:** SEBAL energy balance (Rn − G − H)
- **Data Sources:** Landsat 8 Collection 2 Level 2, MODIS MOD16A2GF, ERA5-Land
- **Validation:** Cross-comparison between SEBAL and MODIS ET products
- **Trend Analysis:** Mann-Kendall test on annual ET time series by distance zone

## Tools

Google Earth Engine JavaScript API

## Author

Hiruni — Final Year, Earth Resources Engineering, University of Moratuwa
