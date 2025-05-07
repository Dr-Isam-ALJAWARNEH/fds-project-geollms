# GeoBikeLLM: Healthiest Bike Route Finder in Chicago

This project combines geospatial data with environmental analysis to help users find the **healthiest biking routes** across Chicago. It uses data on **air quality (PM2.5)** and **green coverage (NDVI)** to compute optimal biking paths that prioritize clean air and greenery.

## 🚲 Project Overview

- **Objective**: Identify the best bike paths in Chicago by considering both distance and environmental quality.
- **Data Sources**:
  - Air Quality CSV files from PM2.5 sensors
  - NDVI (green coverage) data
  - Chicago bike network from OpenStreetMap

## 📂 Files

- `Final Code.ipynb`: The main notebook that:
  - Loads and processes NDVI and AQ datasets
  - Constructs a weighted network graph
  - Applies **Yen’s K-shortest paths algorithm**
  - Selects the cleanest and greenest path

## ⚙️ Features

- Merges real environmental data into a network graph
- Finds multiple route options and selects the healthiest one
- Visualizes results using **folium maps**
- Uses **NetworkX** and **Pandas** for graph and data handling

## 🛠️ Technologies

- Python
- Jupyter Notebook
- NetworkX
- Pandas
- Folium
- OpenStreetMap (via OSMnx)


