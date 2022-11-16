# Image_data

## Context

A set of image files (photos) have been taken and need to be uploaded to a data repository. 

Before publishing the photos, a metadata files are created which contains additional information about the photos.

## Background

This is an example of inage data.

A series of photos were taken using an iPhone.

The approach here could be used for any series of images.

## Method

1. The image files are downloaded from the sensor (the .JPEG files in this folder).
2. A CSV file ('dataset.csv') is created which contains supporting information for the image files (such as the location and when the photo was taken).
2. A new [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) file is created ('dataset.csv-metadata.json'). This describes the structure of the CSV file.
3. The final [CSVW dataset](https://www.stevenfirth.com/csv-on-the-web-an-introduction/) is the 'dataset.csv' and 'dataset.csv-metadata.json' files. These files can now be published, along with the original image files, as a CSVW dataset which would provide much more structured information than the image files or CSV file alone.

## Files in this directory

- '*.JPEG' - the origian image files.
- 'dataset.csv' - a CSV file, created manually in Excel, which gives further data about each image. It is possible that this kind of information coud also be downloaded from the camera.
- 'dataset.csv-metadata.json' - a [CSVW metadata object](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) which is created to provide additional information for the CSV file. The metadata file was [created manually](https://www.stevenfirth.com/csv-on-the-web-creating-descriptive-metadata-files/).
- 'analysis_example.ipynb' - a Jupyter Notebook which provides an example of analysing this dataset.
