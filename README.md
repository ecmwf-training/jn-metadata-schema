# jn-metadata-schema
This repository provides details on the metadata convention used in Jupyter notebooks for training developed for ECMWF. Please see the [Jupyter notebook template](https://github.com/ecmwf-training/jupyter-template/blob/main/jupyter-notebook-template.ipynb) as an example of how this metadata is applied. If any metadata fields are irrelevant to the topic of the notebook, leave them blank.

## Metadata at notebook level
For notebook level metadata, the following table lists the metadata keys and their descriptions that shall be included in each notebook.

For Copernicus notebooks, additional metadata applied to Jupyter notebooks for the [WEkEO platform](https://www.wekeo.eu/) shall also be applied, with the exception of tags:orbit, tags:satellite, tags:sensor, tags:service. The WEkEO Jupyter notebook metadata schema is described here: https://gitlab.eumetsat.int/eumetlab/cross-cutting-tools/jn-metadata-schema.

| Metadata key | Description | Type | Default | Limits | Notes |
|---|---|---|---|---|---|
| tags:category | The overarching topic and programme under which the notebook falls | string | | | Choose one or more of the following, in quotes, separated by commas: 'meteorology', 'computing', 'machine-learning', 'destine', 'research-project' (*note that this refers to research projects, such as Horizon Europe projects, not notebooks developed in ECMWF research department*), 'c3s', 'cams', 'cems'. |
| tags:data_type | The high level data type | string | | | Choose one or more of the following, in quotes, separated by commas: 'observation', 'forecast', 'forecast-s2s', 'forecast-seasonal', 'reanalysis', 'projection' |
| tags:data_product | The precise name of data products used in notebook | string or list of strings | | | For copernicus, use CDS/ADS API convention for product names. For core/DestinE... |

## Metadata at notebook cell level
