# ABCE Open Data Project - IAQ Sensor dataset example

## Dataset introduction

This is the iaq sensor data of an office building in livingston scotland. The IAQ sensor is placed in the open office space. It records past 6 months minutely data of temperature, carbon dioxide and relative humidity. The ABCE Open Data team explore under [FAIR principles](https://www.go-fair.org/fair-principles/).


The files in this folder are:

1. This README.md file.

2. a Jupyter Notebook named 'eoffice_iaq_plot_code.ipynb' which contains examples, written in Python, of how to analyse the dataset. This notebook can be viewed directly in GitHub or on NBViewer here: https://nbviewer.org/github/building-energy/ABCE_Open_Data_Project/blob/main/external_datasets/office_iaq_sensor_data/office_iaq_plot_code.ipynb
3. a file named 'office_iaq_plot_code.png' which is an example plot created by the analysis in the Jupyter Notebook.



## What we are exploring
The CSV on the Web (CSVW) is a standard to add metadata to describe the contents and structure of comma-separated values (CSV) data files.The UK Government Digital Service recommends to use CSVW. CSV files are the most flexible one since they can be loaded easily by Python or Matlab. However, the metadata is only on webpage, seperately stored from dataset if users download the dataset. This may result in inconvenience when reusing.

What we want to do is to create a metadata file to contain the necessary information from webpage and to provide a demonstration about reusage of metadata we create. 

## How did we create the metadata file?


### First stage



## Plots
**Indoor Air Temperature vs Carbon dioxide Concentration**

![office_iaq_plot](https://user-images.githubusercontent.com/62925977/179420765-280e1e0a-6ded-4230-b66c-6f402cc7b225.png)
