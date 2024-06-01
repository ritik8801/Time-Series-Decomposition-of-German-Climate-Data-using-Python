# Time Series Decomposition of German Climate Data using Python

The project decomposes daily and yearly climate data of Germany based on 1990-2021 data. 

## Table of contents
- [Rea & Transform Data](https://github.com/ritik8801/Time-Series-Forecasting-of-German-Climate-Data-using-Python/blob/main/Read%20%26%20Transform%20Data/read-and-transform-data.ipynb)
- [Clean & Select Data](https://github.com/ritik8801/Time-Series-Forecasting-of-German-Climate-Data-using-Python/blob/main/Clean%20%26%20Select%20Data/clean-and-select-data.ipynb)
- [Time Series Decomposition](https://github.com/ritik8801/Time-Series-Forecasting-of-German-Climate-Data-using-Python/blob/main/Time%20Series%20Forecasting/time-series-decomposition.ipynb)

## Dataset

The dataset provides official temperature data measured from 513 weather stations in Germany from 1990 to 2021.

The original data are provided by the German Meteorological Service (DWD, Deutscher Wetterdienst) via the OpenData area of the Climate Data Center (CDC). These data are provided in 1611 files, resulting in > 500 million rows of measurement information (or missing values), a format that is poorly suited for further analysis.

Therefore, the data are converted from "long format" to "wide format". The result is a time series with 10 minute frequency containing one column per weather station. The exact columns in the file are:

MESS_DATUM: the datetime values of the time series, representing the index of the time series
list of weather station ids: one column per weather station, represented by the weather station id
From the five numerical measurement values of the original data, only "air temperature at 2m height in °C" was kept.

In addition to the extracted temperature data, a notebook is provided which can be used to extract the other four types of measurements in the same format.

The following files are provided in this dataset:

german_temperature_data_1990_2021.csv, containing the extracted original data (download and transformation, see this [notebook](https://github.com/ritik8801/Time-Series-Forecasting-of-German-Climate-Data-using-Python/blob/main/Read%20%26%20Transform%20Data/read-and-transform-data.ipynb)).
german_temperature_data_1996_2021_from_selected_weather_stations.csv, containing a selection of the original data from 55 weather stations that have continuously provided a high amount of measurements from 1996-2021 (and thus no change in distribution over time). For the selection process, see this [notebook](https://github.com/ritik8801/Time-Series-Forecasting-of-German-Climate-Data-using-Python/blob/main/Clean%20%26%20Select%20Data/clean-and-select-data.ipynb).
[zehn_min_tu_Beschreibung_Stationen.txt](https://github.com/ritik8801/Time-Series-Forecasting-of-German-Climate-Data-using-Python/blob/main/zehn_min_tu_Beschreibung_Stationen.txt), additional information about the weather stations.
[DESCRIPTION_obsgermany_climate_10min_tu_historical_en.pdf](https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/10_minutes/air_temperature/DESCRIPTION_obsgermany_climate_10min_air_temperature_en.pdf), the official data set description.
The terms of use are described by https://opendata.dwd.de/climate_environment/CDC/Nutzungsbedingungen_German.pdf and https://gdz.bkg.bund.de.