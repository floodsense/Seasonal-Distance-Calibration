# A Detailed Analysis of Raw Sensor Distance Readings
## Overview

For now focused primarily on the "Hoyt & 5th" sensor, this repo contains all Python code and data analysis on how variations of sensor distance measurements interacting with [local weather data](##-Weather-Data).

**Our goal is to better understand what internal and external factors influence variations in the baseline sensor reading of our deployed sensor in order to provide a more reliable and consistent readings.**
<br/>

## Sensor Data

Sensor data is queried from InfluxDB using the InfluxDBClient object in Python. The data is resampled at 10-minute intervals in order to merge timestamps with weather data, which is also resampled at the same 10-day interval.

## Weather Data

The Weather Data is pulled from "the_weather_scraper" Repo forked from it's original location and contains readings from 4 personal weather stations in the Gowanus area.

![Screen Shot 2021-08-12 at 4 15 30 PM](https://user-images.githubusercontent.com/17898669/129263486-9c334168-4a04-4425-b8e5-39272e1d074c.png)
