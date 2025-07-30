# 🏥 Clustering Analysis of Healthcare Facilities in the Special Region of Yogyakarta (DIY)

This repository presents a spatial clustering analysis of healthcare facilities in the Special Region of Yogyakarta (DIY), Indonesia. Using OpenStreetMap data (via OSMnx) and KMeans clustering, the study explores healthcare distribution patterns in relation to administrative boundaries.

---

## 📌 Overview

The analysis covers:
- Extraction of healthcare facility data (`clinic`, `doctors`, `hospital`) from OSM
- Retrieval of administrative boundary data for Sleman, Bantul, Gunung Kidul, Kulon Progo, and Yogyakarta City
- Determination of the optimal number of clusters (K = 5) via Elbow and Silhouette methods
- Visualization of clustering outputs overlaid on maps
- Assessment of healthcare coverage by cluster and by city/regency

---

## 📈 Methodology Highlights

### 🔹 Data Collection
- Healthcare facilities were retrieved via OSMnx using amenity tags: `clinic`, `doctors`, and `hospital`.
- Administrative boundaries were collected with `admin_level=6`.

### 🔹 Clustering Process
- Facility coordinates were projected and clustered using **KMeans**.
- The optimal K value (**K = 5**) was determined via:
  - Elbow Method
  - Silhouette Score

### 🔹 Spatial Join
- Facilities were spatially joined to city/regency polygons using `sjoin` from GeoPandas.

### 🔹 Coverage Analysis
- Number and type of facilities were analyzed per cluster and per city.

---
## 🔧 How to Run the Notebook

1. **Install Dependencies**:
    ```bash
    pip install osmnx geopandas scikit-learn matplotlib
    ```

2. **Run the Notebook**:
   - Execute all cells sequentially in `Clustering_Analysis_of_Healthcare_Facilities.ipynb`.

3. **Outputs**:
   - Clustered facility maps
   - Optimal K plots
   - Cluster composition summaries

---
