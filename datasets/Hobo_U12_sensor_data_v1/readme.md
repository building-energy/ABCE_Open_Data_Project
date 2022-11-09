# Hobo_U12_sensor_data_v1

This is an example of sensor data.

A Hobo U12 sensor recorded time series measurements of the internal conditions of a room in a building. In this case the sensor records the air temperature, the air humidity and the light levels.

The approach here could be used for any sensor which records time series measurements.

The files in this directory are:

- 'ABCE_atrium_U12.csv' - the original data file as downloaded from the sensor.
- 'ABCE_atrium_U12_UTF8.csv' - a revised version of the original data file, saved with a new encoding of UTF-8 (the original file was encoded as ANSI). This is needed to be able to work with the file in the Jupyter Notebooks.
- 'ABCE_atrium_U12_UTF8.csv-metadata.json' - a CSVW metadata object which provides the metadata for the CSV file.
- 'analysis_example.ipynb' - a Jupyter Notebook which provides an example of analysing this dataset.
- 'create_metadata.ipynb' - a Jupyter Notebook which is used to create the 'ABCE_atrium_U12_UTF8.csv-metadata.json' file.
