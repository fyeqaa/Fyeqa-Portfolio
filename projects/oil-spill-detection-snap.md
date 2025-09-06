#### Study Area

- **Location:** Trinidad and Tobago
- **Event:** Oil Spill on 7th February 2024



#### Data

- **Source:** Sentinel-1 SAR imagery downloaded from [Copernicus Open Access Hub](https://colhub.copernicus.eu/userguide/)
- **Focus:** Region of interest around Trinidad and Tobago



### Methodology

This project was executed entirely using the **ESA SNAP Toolbox** with Sentinel-1 SAR imagery. All processing steps were performed through SNAP's graphical interface (no custom code).

##### 1. Data Download
- Downloaded Sentinel-1 GRD data from Copernicus Open Access Hub
- Selected scenes around Trinidad and Tobago covering the date of the 7th February 2024 oil spill

##### 2. Subsetting
- Used SNAP’s Subset Tool to spatially limit the imagery to the affected offshore area
- This improved processing speed and focused the analysis on the region of interest

##### 3. Polarization Selection
- Processed both VH and VV polarizations
- Found that VV polarization provided clearer contrast for oil slick detection
- Used polarization comparison as part of result interpretation

##### 4. Preprocessing Steps

Following the standard Sentinel-1 GRD preprocessing chain in SNAP:


- Radiometric Calibration
  - Converted pixel values to backscatter coefficient (sigma naught)
- Speckle Filtering
  - Applied Lee Sigma filteR with the following configuration:
    - Filter size: 7x7
    - Sigma: 0.9
    - Target window size: 3x3
  - This reduced granular SAR noise while preserving detail critical for oil slick detection


##### 5. Oil Spill Detection
- Used SNAP’s built-in Oil Spill Detection Tool:
  - Detected dark regions with reduced backscatter (common oil slick signature)
  - Applied custom thresholding parameters within the tool
- Masked land areas to remove false positives and enhance accuracy

##### 6. Export and Visualization
- Exported the final classified output as a GeoTIFF

#### Results

- Successfully identified oil spill areas in Sentinel-1 imagery
- Demonstrated the effectiveness of radar remote sensing in monitoring maritime disasters

![Satelite Sar image](/assets/oil-spill-detection-snap/raw_image.png)

![Subset and Filtered sar image](/assets/oil-spill-detection-snap/Filtered_sar.png)

![Detected Oil Spill](/assets/oil-spill-detection-snap/oil_spill_detection.png)


#### Tools & Software

- SNAP Toolbox (Sentinel Application Platform, ESA)
- Sentinel-1 SAR Data

##### Project Presentation

[Oil Spill Detection - Presentation (PDF)](/assets/oil-spill-detection-snap/Presentation.pdf)


