# Interview_data

## Context

An interview is carried out and the responses are saved in a CSV file.

Before publishing the data, a new metadata file is created which contains additional information about the data.

## Background

This is an example of interview data.

A short interview of 4 questions is undertaken for 1 person, asking questions about their thoughts on sustainable building design.

The approach here could be used for any interview data.

## Method

1. The CSV file is created based on the interview responses ('interview_data.csv')
2. A new [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) file is created ('interview_data.csv-metadata.json'). 
3. The final [CSVW dataset](https://www.stevenfirth.com/csv-on-the-web-an-introduction/) is the 'interview_data.csv' and 'interview_data.csv-metadata.json' files. These files can now be published as a CSVW dataset which would provide much more structured information than the CSV file alone.

## Files in this directory

- 'interview_data.csv' - the original data file containing the interview responses.
- 'interview_data.csv-metadata.json' - a [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) which is created to provide additional information for the CSV file.
- 'create_metadata.ipynb' - a Jupyter Notebook which is used to create the 'interview_data.csv-metadata.json' file. Alternatively the metadata file could be [created manually](https://www.stevenfirth.com/csv-on-the-web-creating-descriptive-metadata-files/).


