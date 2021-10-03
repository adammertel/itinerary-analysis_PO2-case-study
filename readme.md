# Analysis of travel itinerary of Premysl Otarak II

## Develop

- create conda environment from .yml file `conda env create -f environment.yml --name po2`
- activate the environment `conda activate po2`

### in case it is needed:

- export the environment to the .yml file `conda env export --no-builds | grep -v "prefix" > environment.yml`

## Code structure

### Processing
`/src/processing` consists of all scripts needed to download, clean and preparse data to prepare them for the analysis:

- `01_download-data.ipynb` download necessary files
- `02_filter-data.ipynb` cleans and filters the input datasets used in further analysis
- `03_create-paths.ipynb` calculates optimal travel paths between all destination in the itinerary
- `04_create-itinerary.ipynb` creates day-to-day and hour-to hour itinerary based on the optimal travel paths

### Metrics
`/src/metrics` list four notebooks that calculates the metrics of the localities importance:

- `01_stays.ipynb`
- `02_travel.ipynb`
- `01_network.ipynb`
- `01_influence.ipynb`

### Use-cases
`/src/use-cases` scripts in this folder analyse the calculated metrics and produce graphical outputs.

### Data
`/data` folder store all raw, intermediate and output datasets

- `/data/01_raw`
- `/data/02_processed`
- `/data/03_paths`
- `/data/04_itinerary`
- `/data/05_metrics`
- `/data/06_outputs`
