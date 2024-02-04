# Analysis of travel itinerary of Premysl Otarak II

A repository with the code and datasets supplementing the paper **Metrics for the identification of primary centers of government from historical itineraries: Přemysl Otakar II: A Case Study**. The primary goal of this study is to test various metrics to represent the importance of the localities in the administration of the medieval kingdom. A case study is performed on the travel itinerary of Přemysl Otakar II.

## Develop

- create conda environment from .yml file `conda env create -f environment.yml --name po2`
- activate the environment `conda activate po2`
- in case the dependencies have been changes, export them into the environment .yml file `conda env export --no-builds | grep -v "prefix" > environment.yml`

## Code structure

### Processing

`/src/processing` consists of all scripts needed to download, clean, and preparse data to prepare them for the analysis, run the codes in this order:

- `01_download-data.ipynb` download all necessary files (including SRTM and geographical data)
- `02_filter-data.ipynb` clean and filter the input datasets used in further analysis
- `03_create-paths.ipynb` calculate optimal travel paths between all destination in the itinerary
- `04_create-itinerary.ipynb` create day-to-day and hour-to-hour itinerary based on the optimal travel paths

### Metrics

`/src/metrics` list four notebooks calculating the localities metrics of importance:

- `01_stays.ipynb`
- `02_travel.ipynb`
- `01_network.ipynb`
- `01_influence.ipynb`

### Use-cases

`/src/use-cases` scripts in this folder analyze the calculated metrics and produce graphical outputs.

### Data

`/data` folder stores all raw, intermediate, and output datasets

- `/data/01_raw`
- `/data/02_processed`
- `/data/03_paths`
- `/data/04_itinerary`
- `/data/05_metrics`
- `/data/06_outputs`
