# CSE 587 — Data-Intensive Computing (DIC)

> Course project for **CSE 587: Data-Intensive Computing** at the University at Buffalo. This is a shared repository used for the semester-long DIC project (group effort).

## Overview

This project performs **Earth Surface Temperature Analysis** — an exploratory data analysis (EDA) and visualization study of global land/surface temperature records. The work explores several related temperature datasets to identify the most useful one, characterizes the data, and produces a range of statistical summaries and geographic/temporal visualizations.

The notebooks were developed and run in **Google Colab** (each notebook includes an "Open in Colab" badge).

## What the project does

The main analysis (`CSE_587_ProjectPhase1.ipynb`) carries out exploratory data analysis on the temperature datasets, including:

- Inspecting data types, unique values, and counting null/missing values
- Computing descriptive statistics — mean, standard deviation, minimum and maximum temperatures
- Aggregating average temperature by **country**, by **month**, and by **latitude**
- Finding global minimum and maximum temperatures across the dataset
- Mapping the geographic locations of data points
- Plotting data binned by latitude on a map

The second notebook (`587_DIC.ipynb`) is exploratory ("just playing around with other datasets") and additionally uses time-series smoothing and interactive map/plot visualizations.

> Note: This is coursework. The notebooks contain the analysis and figures; no formal results or conclusions are claimed here beyond the EDA described above.

## Datasets

The project uses the **Climate Change: Earth Surface Temperature Data** collection (Berkeley Earth), commonly distributed via Kaggle. The following CSV files are referenced:

- `GlobalTemperatures.csv`
- `GlobalLandTemperaturesByCountry.csv`
- `GlobalLandTemperaturesByState.csv`
- `GlobalLandTemperaturesByMajorCity.csv`
- `GlobalLandTemperaturesByCity.csv`

The primary analysis focuses on the **Global Temperatures** dataset.

> The datasets are **not** included in this repository. In the notebooks they are loaded from Google Drive (e.g. `/content/drive/MyDrive/...`). To run the notebooks yourself, download the dataset and update the file paths accordingly (see below).

## Tech stack / tools

- **Language:** Python 3
- **Environment:** Jupyter Notebook / Google Colab
- **Data handling:** pandas, numpy
- **Visualization:** matplotlib, seaborn, plotly (express & graph objects), folium
- **Signal processing:** scipy (`savgol_filter`)

## How to run

### Option A — Google Colab (recommended)

1. Open either notebook via the "Open in Colab" badge at the top of the notebook.
2. Download the dataset (see [Datasets](#datasets)) and place the CSV files in your Google Drive.
3. Mount your Drive when prompted and update the dataset paths to match your Drive layout.
4. Run the cells top to bottom.

### Option B — Local Jupyter

1. Clone this repository:
   ```bash
   git clone https://github.com/JayeshSuryavanshi/Data-Intensive-Computing.git
   cd Data-Intensive-Computing
   ```
2. Install the dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly folium scipy jupyter
   ```
3. Download the dataset CSVs and update the `read_csv(...)` paths in the notebooks to point to your local files (the notebooks currently reference Google Drive paths).
4. Launch Jupyter and open a notebook:
   ```bash
   jupyter notebook
   ```

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- plotly
- folium
- scipy
- jupyter (to run the notebooks locally)

## Repository structure

```
.
├── CSE_587_ProjectPhase1.ipynb   # Main EDA: Earth Surface Temperature Analysis
├── 587_DIC.ipynb                 # Additional exploration / extra datasets
├── .gitignore
└── README.md
```

## License / attribution

This is an academic course project. The temperature datasets are sourced from the Berkeley Earth "Climate Change: Earth Surface Temperature Data" collection and are subject to their respective licenses.
