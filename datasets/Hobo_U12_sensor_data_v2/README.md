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
2. This data is processed, restructured and saved as a new CSV file ('observation.csv'). The structure of this CSV file aligns with the [Observation class in the SOSA ontology](https://www.w3.org/TR/vocab-ssn/#Observations-overview).
3. A new [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) file is created ('observation.csv-metadata.json'). This metadata file describes the 'observation.csv' file and provides sufficient information to convert the data in the 'observation.csv' file into RDF data using the vocabulary of the SOSA ontology.
4. The final [CSVW dataset](https://www.stevenfirth.com/csv-on-the-web-an-introduction/) is the 'observation.csv' and 'observation.csv-metadata.json' files. These files can now be published as FAIR data which would provide much more structured information than the CSV file alone.

## Files in this directory

- 'ABCE_atrium_U12.csv' - the original data file as downloaded from the sensor.
- 'analysis_example.ipynb' - a Jupyter Notebook which provides an example of analysing this dataset.
- 'create_metadata.ipynb' - a Jupyter Notebook which is used to create the 'observation.csv-metadata.json' file. Alternatively the metadata file could be [created manually](https://www.stevenfirth.com/csv-on-the-web-creating-descriptive-metadata-files/).
- 'create_observations.ipynb' - a Jupyter Notebook which is used to create the 'observation.csv' file. 
- 'observation.csv' - a CSV file which holds the same data as the 'ABCE_atrium_U12.csv' file but in a different format.
- 'observation.csv-metadata.json' - a [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) which is created to provide additional information for the CSV file.

## Is this FAIR data?

Yes, this dataset does represent an example of [FAIR data](https://www.go-fair.org/fair-principles/).

The CSVW dataset here (the 'observation.csv' and 'observation.csv-metadata.json' files) can be converted to RDF data using the process described in the W3C CSVW Standards, specifically [Generating RDF from Tabular Data on the Web](https://www.w3.org/TR/2015/REC-csv2rdf-20151217/). The premise of this work is that if the equivalent RDF data meets the FAIR data guidelines, then the CSVW data also meets the FAIR data guidelines.

It is not particularly intended that the CSVW data would be converted to RDF data for analysis, many users would prefer to work directly with the data in CSV format. But the fact that it can be converted to RDF if needed allows for this dataset to be described as meeting the FAIR data guidelines. Examples of how the RDF data looks for this dataset can be seen towards the end of the 'create_metadata.ipynb' Jupyter Notebook in the 'Testing' section.

As this dataset can be converted to RDF, it satifies [Principle I1](https://www.go-fair.org/fair-principles/i1-metadata-use-formal-accessible-shared-broadly-applicable-language-knowledge-representation/) of the FAIR guidelines, namely *"(Meta)data use a formal, accessible, shared, and broadly applicable language for knowledge representation"*.

As the dataset is based on the [SOSA ontology](https://www.w3.org/TR/vocab-ssn/), a common vocabulary for describing sensor measurements, it meets [Principle I2](https://www.go-fair.org/fair-principles/i2-metadata-use-vocabularies-follow-fair-principles/) *"(Meta)data use vocabularies that follow the FAIR principles"*.

The requirement of [Principle F1](https://www.go-fair.org/fair-principles/f1-meta-data-assigned-globally-unique-persistent-identifiers/) *"Globally unique and persistent identifiers remove ambiguity in the meaning of your published data by assigning a unique identifier to every element of metadata and every concept/measurement in your dataset"* is also satisfied by this dataset. This is because the values of concepts and measurements, when converted to RDF, are converted to [URIs](https://www.w3.org/TR/rdf11-primer/#section-IRI) (Uniform Resource Identifiers) which are globally unique and persistent. 

For example, in the CSV file the sensor used for the measurements is referred to as the string 'Sensor1_Hobo_U12'. This string alone is not a globaly unique and persistent identifier. However once converted to RDF an URI is used to represent the sensor with the value '[https://github.com/building-energy/ABCE_Open_Data_Project/tree/main/datasets/Hobo_U12_sensor_data_v2#Sensor1_Hobo_U12](https://github.com/building-energy/ABCE_Open_Data_Project/tree/main/datasets/Hobo_U12_sensor_data_v2#Sensor1_Hobo_U12)'. This is now a globally unique and persistent identifier. Following the web address given in this URI will resolve back to the GitHub repository where the entire dataset is stored. 

*(Note: the URI used for the sensor here could be improved by using a different URI for the sensor which resolves to additional information about the sensor itself - such as the sensor serial number, make and model etc. This could also be done for the other concepts in the dataset, such as the observation location (FeatureOfInterest) and the property being observed (ObservationProperty). This would improve the dataset further and uses the principles described in [5 Star Open Data](https://github.com/building-energy/ABCE_Open_Data_Project/tree/main/datasets/Hobo_U12_sensor_data_v2#Sensor1_Hobo_U12).)*






