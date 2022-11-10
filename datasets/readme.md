# datasets

## What's in this folder?

This folder contains the example datasets which are the outcomes of the ABCE Open Data Project.

For each dataset:

- The data itself is stored in a Comma-Separated Values (CSV) file. This is a standard data format which most users can recognise. CSV files can be opened in a text editor and can be analysed in Excel or through programming (i.e Python).
- An additional file is also provided which is a metadata file, as defined in the [CSV on the Web (CSVW) standards](https://www.w3.org/TR/tabular-data-primer/). This is the key finding of this project, that using these metadata files for CSV data is a suitable approach for providing structured, machine-readable information about the dataset described by the CSV data. It is also shown that it is possible to use this appraoach to develop datasets which meet the [FAIR data principles](https://www.go-fair.org/fair-principles/).
- Examples of simple analysis of the datasets - such as plotting a graph or creating a table - are also given for each dataset. These are done here using Python in [Jupyter Notebooks](https://jupyter.org/) but many other apporaches (e.g. Excel) would also be possible.

For more information on CSVW please see:
- https://www.stevenfirth.com/csv-on-the-web-an-introduction/
- https://csvw.org/
- https://www.w3.org/TR/tabular-data-primer/

## Where should I start?

The first example '[01_Hobo_U12_sensor_data_v1](https://github.com/building-energy/ABCE_Open_Data_Project/tree/main/datasets/01_Hobo_U12_sensor_data_v1)' shows how to create a CSVW metadata file for a sensor data file. This is good starting point if you have some CSV data of your own and wish to create a simple metadata file for it.

The second example '[02_Hobo_U12_sensor_data_v2](https://github.com/building-energy/ABCE_Open_Data_Project/tree/main/datasets/02_Hobo_U12_sensor_data_v2)' develops this further and demonstrates how the data could published to meet the FAIR data guidelines. 

The third example '[03_EnergyPlus_simulation_data](https://github.com/building-energy/ABCE_Open_Data_Project/tree/main/datasets/03_EnergyPlus_simulation_data)' shows how to develop a CSVW dataset for simulation data and how this data can be published on a data repository (Figshare in this case).



