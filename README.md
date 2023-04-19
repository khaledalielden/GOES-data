# GOES-data
This code is for downloading and plotting GOES X-ray Flux from Space Weather Prediction Center - NOAA. This is an alternative code rather than using sunpy package.

# To sun the code

```
import goes

start_time = '2023-01-10 00:00'
end_time = '2023-01-12 00:30'
```
**select the time limits and goes satellite number**
```
X=goes.goes_xray(start_time, end_time,SatelliteNumber = 17)       
```

**get the data**
```
picked_time, fluxA, fluxb = X.get_data()                         
```
**plot_xray( time , fluxA , fluxb )**
```
X.plot_xray(picked_time, fluxA, fluxb)                            
```
**xray_peaks(  wavelength  , x-ray class  )**
```
pt, pv = X.xray_peaks(fluxA,'C')                                
```

# Result

<img src="Xray.jpeg" width="600"/>
