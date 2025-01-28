# Jupyter notebook metadata schema
This repository provides details on the metadata convention used in Jupyter notebooks for training developed for ECMWF. Please see the [Jupyter notebook template](https://github.com/ecmwf-training/jupyter-template/blob/develop/jupyter-notebook-template.ipynb) as an example of how this metadata is applied. 

Please apply this metadata schema to all notebooks used for training at ECMWF. If any metadata fields are irrelevant to the topic of the notebook, leave them blank.

For instructions on how to add metadata to Jupyter notebooks, both at the notebook level, and for individuals cells within notebooks, please refer to https://jupyterbook.org/en/stable/content/metadata.html.

## Metadata at notebook level
For notebook level metadata, the following table lists the metadata keys and their descriptions that shall be included in each notebook.

**For Copernicus notebooks, additional metadata applied to Jupyter notebooks for the [WEkEO platform](https://www.wekeo.eu/) shall also be applied, with the exception of tags:orbit, tags:satellite, tags:sensor, tags:service. The WEkEO Jupyter notebook metadata schema is described here: https://gitlab.eumetsat.int/eumetlab/cross-cutting-tools/jn-metadata-schema.**

| Metadata key | Description | Type | Default | Limits | Notes |
|---|---|---|---|---|---|
| tags:category | The overarching topic and programme under which the notebook falls | string | | | Choose one or more of the following, in quotes, separated by commas: 'meteorology', 'computing', 'machine-learning', 'destine', 'research-project' (*note that this refers to research projects, such as Horizon Europe projects, not notebooks developed in ECMWF research department*), 'c3s', 'cams', 'cems'. |
| tags:data_type | The high level data type | string | | | Choose one or more of the following, in quotes, separated by commas: 'observation', 'forecast', 'forecast-s2s', 'forecast-seasonal', 'reanalysis', 'projection' |
| tags:data_product | The precise name of data products used in notebook | string or list of strings | | | For copernicus, use CDS/ADS API convention for product names. For core/DestinE... |

## Metadata at notebook cell level
Copernicus notebooks shall include metadata tags for certain cells. These include the following tags:
{
    "tags": ["logo", "run", "objectives", "install", "api", "import", "request", "key-messages"]
}
| Metadata cell tag | Which cells to include tag |
|---|---|
| logo | Any cells including logos in the notebook, such as the logolines for C3S/CAMS at the top of each notebook |
| run | Any cells including links or information about running the notebooks on platforms such as WEkEO, Binder, Colab, Kaggle, Deepnote, etc. |
| objectives | Any cells discussing learning objectives. |
| install | Any cells describing installation instructions of packages, such as cdsapi. |
| api | Any cells describing the CDS API or API key. |
| import | Any cells describing the import of libraries/packages. |
| request | Any cells containing API requests, or describing API requests. |
| key-messages | The cells at the end of the notebook summarising key take-home messages. |
