# A Detailed Analysis of Raw Sensor Distance Readings
## Overview

For now focused primarily on Gowanus area sensors, namely the "Hoyt & 5th" sensor, this repo contains all Python code and data analysis on how variations of sensor distance measurements interacts with [local weather data](##-Weather-Data) in both Gowanus and Jamaica Bay.

This analysis is performed on five deployed sensor with at least six months of measurement data captured: "Hoyt & 5th", "Carroll & 4th", "Smith & 9th", "Davenport Court" and "Russell Street".

**Our goal is to better understand what internal and external factors influence variations in the baseline sensor reading of our deployed sensor in order to provide a more reliable and consistent readings.**
<br/>

## Sensor Data

Sensor data is queried from InfluxDB using the InfluxDBClient object in Python. The data is resampled at 10-minute intervals in order to merge timestamps with weather data, which is also resampled at the same 10-day interval.

## Weather Data

The Weather Data is retrieved from SUNY Micronet weather stations via a dedicated API endpoint. Weather data is retrieved both from individual locations and as an aggregated mean across stations. Part of this research aims to assess the relative importance of hyperlocality in weather data. 

<!---![Screen Shot 2021-08-12 at 4 15 30 PM](https://user-images.githubusercontent.com/17898669/129263486-9c334168-4a04-4425-b8e5-39272e1d074c.png)--->
![Screen Shot 2022-05-13 at 4 40 14 PM](https://user-images.githubusercontent.com/17898669/168394505-d2aec01c-2136-4363-8d36-18012d9af18c.png)
