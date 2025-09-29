# 💨 Air Quality Time Series Analysis and Interactive Visualization

## Project Overview
This repository contains a Jupyter Notebook that performs **time series analysis and interactive visualization** of air quality data. The main goal of this project is to clean a challenging, raw dataset, prepare it for analysis, and create dynamic, interactive plots using Plotly to explore trends in air pollutant concentrations over time.

## 📊 Data Source
The analysis uses the **Air Quality Data Set**.

* **Original File:** `AirQuality.csv`
* **Key Features Analyzed:** Time series data for various air pollutants and meteorological parameters, including:
    * `CO(GT)` (True hourly averaged concentration of CO)
    * `NOx(GT)` (True hourly averaged overall NOx concentration)
    * `NO2(GT)` (True hourly averaged concentration of NO2)
    * `T` (Temperature)
    * `RH` (Relative Humidity)
    * `AH` (Absolute Humidity)

## ✨ Analysis & Cleaning Pipeline

The notebook `AirQuality_Analysis.ipynb` follows a clear, structured approach for data wrangling and visualization:

### 1. Data Cleaning and Preparation
The raw CSV file presented several challenges, which were addressed:
* **Custom Parsing:** The data was reloaded using the correct delimiter (semicolon `;`) and decimal separator (comma `,`) to correctly parse the European format.
* **Missing Value Handling:** Missing values, encoded as `-200` in the dataset, were converted to standard NumPy `NaN`.
* **Time Series Indexing:** Separate `Date` and `Time` columns were combined and converted into a single, comprehensive `DateTime` index for effective time series analysis.
* **Outlier/Missing Column Removal:** An empty column (`Unnamed: 15`) and a column with excessive missing data (`NMHC(GT)`) were dropped.
* **Row Removal:** All remaining rows with missing values were dropped to ensure a clean dataset for plotting.

### 2. Interactive Visualization
The cleaned dataset was used to generate interactive visualizations, allowing users to zoom, pan, and hover over the data points for detailed inspection of the time series trends.

* **Tool Used:** **Plotly**
* **Output:** An interactive line plot visualizing the various pollutant and meteorological features over the time period of the dataset (March 2004 to April 2005).

## 💻 Dependencies

To run this notebook locally, you need a Python environment with the following libraries:

```bash
pandas
plotly

You can install the necessary dependencies using pip:

pip install pandas plotly
🚀 How to Run the Notebook
Clone the repository:

Bash

git clone [your-repository-url]
cd [your-repository-name]
Ensure data is present: Make sure the AirQuality.csv file (or equivalent air quality dataset) is in the project directory, or update the file path in the notebook if necessary.

Launch Jupyter:

Bash

jupyter notebook AirQuality_Analysis.ipynb
Execute Cells: Run all cells in the notebook to perform the data cleaning, preparation, and generate the interactive Plotly visualization.
