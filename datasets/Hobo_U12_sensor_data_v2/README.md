# Hobo_U12_sensor_data_v2

## Context

A data file is downloaded from a sensor. 

Before publishing the data, the data is processed to a series of new files and a new metadata file is created which contains additional information about the data.

The data is now published as [FAIR data](https://www.go-fair.org/fair-principles/).

## Background

This is an example of sensor data.

A [Hobo U12](https://www.onsetcomp.com/products/data-loggers/u12-011/) sensor recorded time series measurements of the internal conditions of a room in a building. In this case the sensor records the air temperature, the air humidity and the light levels.

The approach here could be used for any sensor which records time series measurements.

## Method

1. The data file is downloaded from the sensor ('ABCE_atrium_U12.csv')




2. A new [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) file is created ('ABCE_atrium_U12.csv-metadata.json'). 
3. The final [CSVW dataset](https://www.stevenfirth.com/csv-on-the-web-an-introduction/) is the 'ABCE_atrium_U12.csv' and 'ABCE_atrium_U12.csv-metadata.json' files. These files can now be published as a [CSVW dataset](https://www.stevenfirth.com/csv-on-the-web-an-introduction/) which would provide much more structured information than the CSV file alone.

## Files in this directory

- 'ABCE_atrium_U12.csv' - the original data file as downloaded from the sensor.
- 'ABCE_atrium_U12.csv-metadata.json' - a [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) which is created to provide additional information for the CSV file.
- 'analysis_example.ipynb' - a Jupyter Notebook which provides an example of analysing this dataset.
- 'create_metadata.ipynb' - a Jupyter Notebook which is used to create the 'ABCE_atrium_U12_UTF8.csv-metadata.json' file. Alternatively the metadata file could be [created manually](https://www.stevenfirth.com/csv-on-the-web-creating-descriptive-metadata-files/).



## Is this [FAIR data](https://www.go-fair.org/fair-principles/)?

