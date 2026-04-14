# 🚂 Indian Railways Geospatial Analytics

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![MongoDB](https://img.shields.io/badge/Database-MongoDB%20Atlas-green.svg)](https://www.mongodb.com/)
[![Folium](https://img.shields.io/badge/Mapping-Folium-orange.svg)](https://python-visualization.github.io/folium/)

## 📌 Project Overview
This project provides a comprehensive spatial analysis of the Indian Railways network using **MongoDB Atlas** as the spatial engine. It processes thousands of station records and train schedules to perform complex proximity, region-based, and 3D geospatial queries.

## 🛠️ Tech Stack
- **Database:** MongoDB Atlas (NoSQL) with `2dsphere` indexing.
- **Language:** Python 3.x
- **Libraries:** 
  - `pymongo`: Database connectivity.
  - `folium`: Interactive map visualizations.
  - `geopy`: Geodetic distance calculations.
  - `shapely`: Geometric operations (Union/Intersects).
  - `kagglehub`: Automated dataset retrieval.

## 🗺️ Geospatial Operations Performed
1.  **Basic CRUD:** Full lifecycle management of train records.
2.  **Point Queries:** Finding the nearest station to a specific GPS coordinate using `$near`.
3.  **Polygon Search:** Identifying all stations within the Tamil Nadu state boundary.
4.  **Regional Analysis:** Zooming into the Chennai City cluster.
5.  **Spatial Intersections:** Finding stations along the TN-Karnataka border ($geoIntersects).
6.  **Distance Modeling:** Geodetic distance between Chennai Central (MAS) and Coimbatore North (CBF).
7.  **Centroid Calculation:** Computing the geographic center of the railway network in Tamil Nadu.
8.  **Proximity Buffering:** 3km service radius analysis around PSG Tech, Coimbatore.
9.  **Geometric Union:** Merging Coimbatore and Tiruppur district polygons.
10. **Site Selection:** Using grid-density analysis to propose the best location for a supermarket.
11. **3D Proximity:** Calculating distance to Ooty stations considering altitude (Pythagorean 3D).
12. **Infrastructure Extrusion:** Modeling Chennai Central as a 3D extruded building block.
13. **Network Adjacency:** Building LineStrings for route corridors to find adjacent neighbors.

## 🚀 How to Run
1. Clone this repository.
2. Ensure you have a MongoDB Atlas URI with a `2dsphere` index on the `geometry` field.
3. Run the `.ipynb` notebook in Google Colab or Jupyter.

---
*Developed as part of the Big Data & Modern Databases curriculum.*