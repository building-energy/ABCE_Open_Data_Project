# Questionnaire_data

## Context

A questionnaire is carried out and the responses are saved in a CSV file.

Before publishing the data, a new metadata file is created which contains additional information about the data.

## Background

This is an example of questionnaire data.

A short questionnaire is undertaken for 5 people, asking questions about their name, age, gender and occupation.

The approach here could be used for any questionnaire data.

## Method

1. The CSV file is created based on the questionnaire responses ('questionnaire_data.csv')
2. A new [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) file is created ('questionnaire_data.csv-metadata.json'). 
3. The final [CSVW dataset](https://www.stevenfirth.com/csv-on-the-web-an-introduction/) is the 'questionnaire_data.csv' and 'questionnaire_data.csv-metadata.json' files. These files can now be published as a CSVW dataset which would provide much more structured information than the CSV file alone.

## Files in this directory

- 'questionnaire_data.csv' - the original data file containing the questionnaire responses.
- 'questionnaire_data.csv-metadata.json' - a [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) which is created to provide additional information for the CSV file.
- 'analysis_example.ipynb' - a Jupyter Notebook which provides an example of analysing this dataset.
- 'create_metadata.ipynb' - a Jupyter Notebook which is used to create the 'questionnaire_data.csv-metadata.json' file. Alternatively the metadata file could be [created manually](https://www.stevenfirth.com/csv-on-the-web-creating-descriptive-metadata-files/).


