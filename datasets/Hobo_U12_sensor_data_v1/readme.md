# Hobo_U12_sensor_data_v1

## Context

A data file is downloaded from a sensor. 

Before publishing the data, a new metadata file is created which contains additional information about the data.

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

No. 

The new CSVW dataset here is an example of well structured data. CSVW can be [converted to RDF](https://www.w3.org/TR/tabular-data-primer/#transformation) which would satisfy [Principle I1](https://www.go-fair.org/fair-principles/i1-metadata-use-formal-accessible-shared-broadly-applicable-language-knowledge-representation/) of the FAIR guidelines. 

However this dataset contains much information in the form of text only, such as the type of sensor used and the location where the sensor was placed. This means that the dataset would not meeting [Principle F1](https://www.go-fair.org/fair-principles/f1-meta-data-assigned-globally-unique-persistent-identifiers/) which asks for *"Globally unique and persistent identifiers remove ambiguity in the meaning of your published data by assigning a unique identifier to every element of metadata and every concept/measurement in your dataset."* 

The dataset also could use a dedicated common vocabulary for describing sensor measurements (such as the SOSA ontology) which would help to meet [Principle I2](https://www.go-fair.org/fair-principles/i2-metadata-use-vocabularies-follow-fair-principles/) of the FAIR guidelines.

An example of this same dataset as FAIR data is given here: https://github.com/building-energy/ABCE_Open_Data_Project/tree/main/datasets/Hobo_U12_sensor_data_v2


