# Flooding Assessment in Akosombo and its Environs
Using remote sensing (SAR) and GIS for evaluating the flooding extents for the 2023 inundation event in Akosombo, Ghana (West Africa). The application also incorprated SAR Image despeckling using refined the Lee Filter (Yommy et al., 2015) for efficient speckle noise
removal and the improvement of image quality . The method is based on the well-known Lee filter. In this method the K-Nearest Neighbour (KNN) algorithm is employed to adjust the number of neighbour pixels used within the sliding window.

## Using Sentinel-1 ground range detection satellites in Google Earth Engine (GEE)

### Overview on the SAR sensor

The SAR (Synthetic Aperture Radar) sensor is mounted satellite and points sideways instead of straight down (nadir). It is an active sensor that sends electromagnetic waves to the earth's surface and receives the reflected signal.
The electromagnetic wave received by the sensor is called the measured backscatter. A SAR image is a 2D rendering of the measured backscatter.

![image](https://github.com/user-attachments/assets/ed3c546d-ab9d-49d7-a0f7-94a802d6cf25)
An optical sensor (left) only works with clear, sunny skies. A SAR sensor (right) can work both day and night, and even when clouds are present.
Source: pro.arcgis.com

COMPOSITION
Platform:
Sentinel-1A and Sentinel-1B satellites
Sensor: C-band Synthetic Aperture Radar (SAR).

Band Used:
VH: Vertical transmit, horizontal receive polarization.

Resolution: Approximately 10 meters.

Spatial Coverage: Global.

Temporal Coverage: From October 3, 2014, to present.

Revisit Time: Typically, 6-12 days, depending on the latitude and sensor mode.

### Polorization Type
![image](https://github.com/user-attachments/assets/e2654815-a43e-4a41-a62b-dfe4de5bf43e)
Four main SAR Polarization types.
Source: pro.arcgis.com

Based on the assessment required, the VH Polarization was selected. Illustrated below are some pros and cons of this polarization type

Advantages:
Enhanced Vegetation Detection: VH polarization is sensitive to volume scattering, making it effective for detecting changes in vegetation and flooded areas under vegetation.
Improved Discrimination of Surface Types: It can help distinguish between different surface types due to its sensitivity to structural differences.

Disadvantages:
Higher Noise Levels: VH polarization typically has higher noise levels compared to VV, which can affect the clarity and accuracy of the flood maps.
Lower Signal-to-Noise Ratio: It generally has a lower signal-to-noise ratio, which can impact the quality of the data for detecting water surfaces

### Benefits/advantages of using SAR data
a. An active sensor, used by SAR systems, functions as both the source and the receiver
b. Unlike an optical sensor, a SAR sensor can operate during the day or night, independent of the sun, since it transmits its own signal.
c. Active sensing also allows you to control the polarization of the transmitted electromagnetic waves.
d. SAR can penetrate through clouds, smoke, and even vegetation, making it particularly useful during extreme weather events when optical sensors may be ineffective

### Results (Illustration of the User-Interface acquired from GEE).  
![Akosombo_Flooding_SAR_extract](https://github.com/user-attachments/assets/63b76806-e0ce-430e-a4e4-fa03eae5959e)

### Link to the Webpage
https://ee-geohazardrisk-mapping.projects.earthengine.app/view/akosombofloodingsar

### Github link for Refined Lee Speckle filter
Applying a Refined Lee Speckle filter as coded in the SNAP 3.0 S1TBX:

https://github.com/senbox-org/s1tbx/blob/master/s1tbx-op-sar-processing/src/main/java/org/esa/s1tbx/sar/gpf/filtering/SpeckleFilters/RefinedLee.java
Adapted by Guido Lemoine

### Reference
Yommy, A. S., Liu, R., & Wu, S. (2015, August). SAR image despeckling using refined Lee filter. In 2015 7th International Conference on Intelligent Human-Machine Systems and Cybernetics (Vol. 2, pp. 260-265). IEEE.

### License
This project is licensed under the MIT License - see the LICENSE file for details.
