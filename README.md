# Interpolating Sea level anomalies based on eddies in the Southern ocean

### Purpose of the project
The purpose of this project is to interpolate sea level anomaly in the Southern Ocean using the eddies observed in Sentinel 3 altimetry( Pegliasco et al.,2022). Based on Sallee J.B.,2018, the Southern Ocean has been warming at 0.1 to 0.2 degrees Celsius per decade from the surface to 1000m in depth due to anthropogenic emissions. This helps to understand how the increase in temperature in Southern Ocean leads to the decrease in Antartica ice sheet. ( Holland et.al,2020).

### Methodology
**Part 1**
1. Eddy data around the world ocean is acquired using **Mesoscale Trajectory Eddy Atlas** ( Has Eddy data around the world from 1993 to 2022)
2. The eddy from Western Antartica is selected as it has relatively little ice sheet
3. 500Km buffer zone is selected from the eddy to filter out along track data that doesn't pass through near the eddy. 
4. Altimetry data from Sentinel 3 is acquired from the Copernicus data space system and it is plotted to make sure that it passes through the buffer zone
5. Altimetry data is downloaded to use in Part 2.
   
**Part 2**

6. Sea Surface Height Anomaly (SSHA)  is determined from substracting instantaneous Sea Surface Height (SSH) with long term mean sea surface.
   
**SSHA= SSH-MSS**

Sea surface Height is calculated using following equation

**SSH = H - R - C**

Where

H = Satelite altitude ( Around 814.5km  ( Source:European Space Agency))

R = Ku band retracted range to water ( The radar measured distance and corrected distance to the water surface based on Ku band signal. Sentinel 3 has Ku band around 20 GHz (Source: Fu, L.L. and Cazenave, A. eds., 2000. and European Space Agency )

C = Geophysical Corrections, which include: Ionospheric correction, dry tropospheric correction, wet tropospheric corrections, sea state bias correction, tidal corrections, inverted barometer correction high-frequency sea surface fluctuation correction

7. 


