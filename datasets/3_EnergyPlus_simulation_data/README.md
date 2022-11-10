# EnergyPlus_Simulation)data

## Context

A data file is created by a simulation programme. 

Before publishing the data, a new metadata file is created which contains additional information about the data.

## Background

This is an example of simulation or modelling data.

An [EnergyPlus](https://energyplus.net/) simulation of a building is created, run and a CSV file of the model outputs is saved. The data includes hour-by-hour predictions of energy consumption and internal conditions (e.g. air temperature) of the modelled building.

The approach here could be used for any simulation data which makes time series predictions.

## Method

1. The data file is downloaded from the sensor ('eplusout.csv')
2. A new [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) file is created ('eplusout.csv-metadata.json'). 
3. The final [CSVW dataset](https://www.stevenfirth.com/csv-on-the-web-an-introduction/) is the 'eplusout.csv' and 'eplusout.csv-metadata.json' files. These files can now be published as a CSVW dataset which would provide much more structured information than the CSV file alone.

## Files in this directory

- 'eplusout.csv' - the original data file as created by the simulation package.
- 'eplusout.csv-metadata.json' - a [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) which is created to provide additional information for the CSV file.
- 'analysis_example.ipynb' - a Jupyter Notebook which provides an example of analysing this dataset.
- 'create_metadata.ipynb' - a Jupyter Notebook which is used to create the 'eplusout.csv-metadata.json' file. Alternatively the metadata file could be [created manually](https://www.stevenfirth.com/csv-on-the-web-creating-descriptive-metadata-files/).


## Is this FAIR data?

No, this dataset does not fully meet the [FAIR data guidelines](https://www.go-fair.org/fair-principles/).

The new CSVW dataset here is an example of well structured data. CSVW can be [converted to RDF](https://www.w3.org/TR/tabular-data-primer/#transformation) which would satisfy [Principle I1](https://www.go-fair.org/fair-principles/i1-metadata-use-formal-accessible-shared-broadly-applicable-language-knowledge-representation/) of the FAIR guidelines. 

However this dataset contains much information in the form of text only, such as the type of sensor used and the location where the sensor was placed. This means that the dataset would not meeting [Principle F1](https://www.go-fair.org/fair-principles/f1-meta-data-assigned-globally-unique-persistent-identifiers/) which asks for *"Globally unique and persistent identifiers remove ambiguity in the meaning of your published data by assigning a unique identifier to every element of metadata and every concept/measurement in your dataset."* 

The dataset also could use a dedicated common vocabulary for describing sensor measurements (such as the [SOSA ontology](https://www.w3.org/TR/vocab-ssn/)) which would help to meet [Principle I2](https://www.go-fair.org/fair-principles/i2-metadata-use-vocabularies-follow-fair-principles/) of the FAIR guidelines.

An example of this same dataset as FAIR data is given here: https://github.com/building-energy/ABCE_Open_Data_Project/tree/main/datasets/Hobo_U12_sensor_data_v2




This folder contains an example of how to analyse the 'Simulation data example' dataset.

The dataset itself can be viewed here: https://figshare.com/s/464885898d0041bfa8fd

The files in this folder are:
- this README.md file.
- a Jupyter Notebook named 'examples_of_data_analysis.ipynb' which contains examples, written in Python, of how to analyse the dataset. This notebook can be viewed directly in GitHub or on NBViewer here: https://nbviewer.org/github/building-energy/ABCE_Open_Data_Project/blob/main/internal_test_datasets/simulation/examples_of_data_analysis.ipynb
- a file named 'time_series_plot.png' which is an example plot created by the analysis in the Jupyter Notebook. 

