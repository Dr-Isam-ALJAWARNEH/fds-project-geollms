# Chicago Visualization

## Overview
Visualize environmental data over the Chicago area using Python and Folium. It includes two key components:

1. **Air Quality Visualization (PM2.5 Heatmap)** – To identify areas with high pollution levels.
2. **Vegetation Visualization (NDVI Heatmap)** – To highlight greener regions with higher vegetation density.

These visualizations support public health insights, environmental planning, and sustainability initiatives.

---

## 1. PM2.5 Air Quality Heatmap

### Description
This code creates an interactive heatmap based on PM2.5 sensor data across Chicago, showing pollution hotspots using normalized PM2.5 values.

### Features
- Automatically downloads and merges 19 PM2.5 datasets from GitHub.
- Cleans the dataset by removing entries with missing latitude, longitude, or PM2.5 values.
- Normalizes PM2.5 values using `MinMaxScaler`.
- Generates a Folium-based heatmap centered on Chicago.


## 2. NDVI Green Zone Heatmap

### Description
This code visualizes vegetation coverage over the Chicago region using NDVI (Normalized Difference Vegetation Index) data. Areas with more greenery appear in green, and less vegetated regions appear in blue.

### Features
- Loads the most recent NDVI dataset (e.g., March 2023).
- Cleans the dataset by removing rows with missing coordinates or NDVI values.
- Normalizes NDVI values (grid_code) to a [0, 1] scale.
- Generates a Folium heatmap highlighting greener areas.
