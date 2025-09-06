---
title: "TreeDetectR"
description: Urban Tree Detection from LiDAR in R
image: ../images/treedetection.png
---
<a href="https://github.com/fyeqaa/TreeDetectR" target="_blank">
  <button style="background-color:#24292e; color:white; padding:8px 16px; border:none; border-radius:5px; cursor:pointer;">
    GitHub
  </button>
</a>


TreeDetectR is an R package I developed to detect and segment individual tree from urban LiDAR point cloud data. This project automates the processing steps, from raw LAS files to georeferenced tree locations.
The goal of this project was to detect and segment individual trees within the university campus using FIS-Broker data’s LiDAR point cloud data. 



What I Did

- Loaded and filtered raw LiDAR data
- Classified ground points using the Cloth Simulation Filter (CSF)
- Built a Digital Terrain Model (DTM) and Canopy Height Model (CHM)
- Detected individual tree tops using local maximum filtering (LMF)
- Segmented individual trees using the Dalponte2016 algorithm
- Exported georeferenced tree coordinates (X, Y, Z, Latitude, Longitude)

#### Visual Results

This CHM represents the height of vegetation above ground level. Brighter areas are taller tree canopies.

![CHM](/assets/TreeDetectR/Smoothed_CHM.png)

Red dots represent tree tops detected using Local Maximum Filtering (LMF).

![Tree Tops](/assets/TreeDetectR/treetops.png)


#### Georeferenced Tree Coordinates

Tree coordinates were extracted and exported as a CSV file, including height and WGS84 (Lat/Lon) positions.

**Sample of exported data:**

| Tree ID | Longitude | Latitude | Height (Z) |
|---------|-----------|----------|------------|
| 001     | 13.40123  | 52.52041 | 17.6       |
| 002     | 13.40128  | 52.52046 | 15.2       |
| 003     | 13.40131  | 52.52050 | 14.7       |

---

#### Summary

This project demonstrates how to automate urban tree detection using LiDAR data in R. With `TreeDetectR`, users can go from raw point cloud to segmented, geolocated individual trees in just a few steps.


