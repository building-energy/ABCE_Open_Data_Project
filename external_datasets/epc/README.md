# ABCE_Open_Data_Project - EPC Dataset

## Dataset introduction

[The energy performance certificate (EPC) dataset](https://epc.opendatacommunities.org/) is a freely accessible dataset where the ABCE Open Data team have applied the [FAIR principles](https://www.go-fair.org/fair-principles/) to make the dataset open and accessible for more users.

To access an EPC dataset you must first create an account at the provided web address, where you can log-in each time you wish to download or use the data. 
Once you have created an account you will then be able to access the data under a copyright [license](https://epc.opendatacommunities.org/docs/copyright). The data is arranged such that you can select differnt filters (or search by postcode) to acquire the EPC data for the property/properties you desire. 

When downloaded, you get a file named 'epc-certificate' or 'epc-certificates' if you downloaded multiple EPCs. Within that file you are then provided with three files:
 - LICENCE.txt: this is a text file containing the license agreement under which the EPC data can be used.
 - certificates.csv: this is a csv file that contains the recorded information for each property selected when downloading the dataset. Each property's data is captured on a seperate row.
 - recommendations.csv: this csv file contains the recommendation information for each property selected. Each row of this csv corresponds to a different recommendation, whereby multiple property's recommendations can be found using a unique identifier.



**Plots**
The plots are available inside a ZIP file for a quick inspection.

## What we are exploring

In their dataset, text files are the most flexible one since they can be loaded easily by Python or Matlab. However, the metadata is only on webpage, seperately stored from dataset if users download the dataset. This may result in inconvenience when reusing.

What we want to do is to create a metadata file to contain the necessary information from webpage and to provide a demonstration about reusage of metadata we create. 

## License

## Reference

## Tasks


### First stage

- [ ] write metadata.json (all .txt/.csv in one .json)
      - convert txt to csv?
      - write json
- [ ] code to reuse metadata
      - reuse metadata.json with dataset
      - csv validating
- [ ] upload zipfile of dataset sample. if we can use python to read zip from url, this step can be skiped.
      - consider about the data file format
      - notes: python library zipfile


### Second stage (optional)

If time and resourses are allowed, the second stage could be restructing the dataset using ['sensor observation model'](https://www.w3.org/TR/vocab-ssn/#Observations-overview).