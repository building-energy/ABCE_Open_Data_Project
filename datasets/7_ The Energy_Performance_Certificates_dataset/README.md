# ABCE_Open_Data_Project - EPC Dataset

---UNDER DEVELOPMENT---

## Dataset introduction

[The energy performance certificate (EPC) dataset](https://epc.opendatacommunities.org/) is a freely accessible dataset where the ABCE Open Data team have applied the [FAIR principles](https://www.go-fair.org/fair-principles/) to make the dataset open and accessible for more users.

To access an EPC dataset you must first create an account at the provided web address, where you can log-in each time you wish to download or use the data. 
Once you have created an account you will then be able to access the data under a copyright [license](https://epc.opendatacommunities.org/docs/copyright). The data is arranged such that you can select differnt filters (or search by postcode) to acquire the EPC data for the property/properties you desire. 

When downloaded, you get a file named 'epc-certificate' or 'epc-certificates' if you downloaded multiple EPCs. Within that file you are then provided with three files:
 - LICENCE.txt: this is a text file containing the license agreement under which the EPC data can be used.
 - certificates.csv: this is a csv file that contains the recorded information for each property selected when downloading the dataset. Each property's data is captured on a seperate row.
 - recommendations.csv: this csv file contains the recommendation information for each property selected. Each row of this csv corresponds to a different recommendation, whereby multiple property's recommendations can be found using a unique identifier.


## What we are exploring
CSV data files are one of the most commonly used file formats for data science. In order to make the data more open (following the FAIR principles) the ABCE open-data group have identified EPC datasets as a format that woudl benefit from teh CSVW format.
CSV files can be loaded easily by Python or Matlab. However, the metadata is stored seperately from dataset if users download the dataset from the [origin website](https://epc.opendatacommunities.org/). 
Our task is to create a generic metadata file to contain the necessary information that fully describes the CSVW format of the EPC data, and to provide a demonstration of how data analysis can be peformed for the EPC data using the cSVW format. 

### First stage

- [ ] write metadata.json (all .txt/.csv in one .json)
      - Select EPC data file from [origin website](https://epc.opendatacommunities.org/)
      - Unzip file and move to root analysis folder location
      - co-locate the metadate.json files within the root folder (one .json for each of the certificates and recommendations CSV files)
- [ ] code to reuse metadata
      - reuse metadata.json with dataset
      - csv validating