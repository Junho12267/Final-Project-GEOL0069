# Interpolating Sea Surface Height Anomaly

### Purpose of the project
The purpose of this project is to interpolate Sea Surface Height Anomaly ( SSHA )  in the Southern Ocean using the eddies observed in Sentinel 3 altimetry( Pegliasco et al.,2022). The along-track data of Sentinel-3 can help track how eddies in the Southern Ocean move over time. Sentinel-3 is very useful as it works as both active and passive satellite and does a good job in tracking ocean features like eddies as shown in the infographic below. 

![Alt text](https://github.com/Junho12267/Final-Project-GEOL0069/blob/main/How%20does%20sentinel%203%20work(1080%20x%201920%20px)%20(1).png)


However, since Sentinel-3 has narrow tracks and its revisit time is only around once a day (Even with Sentinel-3A and 3B combined). Hence, interpolating eddies using GPSAT helps to fill in the missing gaps in the Sentinel-3 satellite track and create a whole picture of SSHA in the Southern Ocean. 


This data is useful as SSHA is a good indicator of how sea level changes with recent anthropogenic global warming. 
Based on Sallee J.B.,2018, the Southern Ocean has been warming at 0.1 to 0.2 degrees Celsius per decade from the surface to 1000m in depth due to anthropogenic emissions. Additionally, SSHA can also help to understand how the increase in temperature in the Southern Ocean leads to the decrease in the Antarctic ice sheet. ( Holland et.al,2020).

### Methodology
**Part 1**
1. Eddy data around the world ocean is acquired using **Mesoscale Trajectory Eddy Atlas** ( Has Eddy data around the world from 1993 to 2022)
2. The eddy from Western Antarctica is selected as it has relatively little ice sheet
3. A 500 km buffer zone is selected from the eddy to filter out along-track data that doesn't pass through near the eddy. 
4. Altimetry data from Sentinel 3 is acquired from the Copernicus data space system, and it is plotted to make sure that it passes through the buffer zone
5. Altimetry data is downloaded to use in Part 2.
   
**Part 2**

6. Sea Surface Height Anomaly (SSHA)  is determined by subtracting the instantaneous Sea Surface Height (SSH) from the long-term mean sea surface (MSS).
   
**SSHA= SSH-MSS**

Sea surface Height is calculated using the following equation

**SSH = H - R - C**

Where

H = Satellite altitude ( Around 814.5km  ( Source: European Space Agency, 2024))

R = Ku band retracted range to water ( The radar measured distance and corrected distance to the water surface based on Ku band signal. Sentinel 3 has Ku band around 20 GHz (Source: Fu, L.L. and Cazenave, A. eds., 2000, and European Space Agency )

C = Geophysical Corrections, which include: Ionospheric correction, dry tropospheric correction, wet tropospheric corrections, sea state bias correction, tidal corrections, inverted barometer correction, high-frequency sea surface fluctuation correction

7. Altimetry data has been filtered to a latitude near the Southern Ocean, and any SSHA above 1m has been filtered out, as this is considered erroneous.
8. Select a buffer zone for a region to interpret SSHA and create a square grid to create an expert location.
9. Use GPSAT to interpolate SSHA.

## **Link to notebook**
[Final Project eddies](https://colab.research.google.com/drive/1vlX_AHtxUGKYow2XjmVzCoL5NvGAkqnV#scrollTo=yXp-nUCcKPlr)

## **Link to video**
(https://ucl.zoom.us/rec/share/bAjxy5ocnSv_Quj1SIp5utSnOZXO68RJtTH2q5WMvHdpb4JEyQKXo25pq7hTrgc_.D_a_DDY0QmySYGx7?startTime=1748694771000 Passcode: 7Gi$V*^N)

**Note: In 5:46 of the video, what I meant is SSHA is 0.1 to 0.2m higher than normal in general ( Not 0.2 to 0.4m).**

## References 

EdenSeven (2025) Britain’s Electricity Generation – Annual Review. Available at: https://www.edenseven.co.uk/national-grid-eso-analysis-annual-review-24 (Accessed: 29 May 2025).EdenSeven+5EdenSeven+5EdenSeven+5 

European Space Agency (ESA), 2024. Satellite constellation. Available at: https://www.esa.int/Applications/Observing_the_Earth/Copernicus/Sentinel-3/Satellite_constellation?utm_source=chatgpt.com [Accessed 29 May 2025]. 

Fu, L.L. and Cazenave, A. eds., 2000. Satellite altimetry and earth sciences: a handbook of techniques and applications (Vol. 69). Elsevier. Holland, D.M., Nicholls, K.W. and Basinski, A., 2020. The Southern Ocean and its interaction with the Antarctic ice sheet. Science, 367(6484), pp.1326-1330. 

GEOL0069, Artificial Intelligence for Earth Observation, Week 8, Eddies from altimetry part 1 and 2

Pegliasco, C., Delepoulle, A., Mason, E., Morrow, R., Faugère, Y. and Dibarboure, G., 2022. META3. 1exp: A new global mesoscale eddy trajectory atlas derived from altimetry. Earth System Science Data, 14(3), pp.1087-1107. 

Sallée, J.B., 2018. Southern Ocean warming. Oceanography, 31(2), pp.52-62. 

Whitehouse, P.L., 2018. Glacial isostatic adjustment modelling: historical perspectives, recent advances, and future directions. Earth surface dynamics, 6(2), pp.401-429. 

 




