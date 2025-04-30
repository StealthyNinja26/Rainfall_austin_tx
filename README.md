# 🌧️ Rainfall Data Cleaning and Analysis

This notebook processes and analyzes rainfall and weather data for Austin, Texas. It involves data cleaning, transformation, and basic statistical analysis to prepare the dataset for further modeling or exploratory tasks.

## 📌 Objective

- Clean and preprocess the Austin weather dataset.
- Handle missing values and special characters ('T', '-') appropriately.
- Convert all features to numerical types.
- Generate basic statistics like mean, trimmed mean, median, and confidence intervals for all features.

## 📁 Dataset Description

Original Dataset: `austin_weather.csv`

Key Features:
- Temperature metrics (High, Average, Low)
- Dew point readings
- Humidity levels
- Sea level pressure
- Visibility measures
- Wind speed measurements
- Total daily precipitation

## 🧰 Libraries Used

- `pandas` – for data manipulation
- `numpy` – for numerical computations
- `scipy.stats` – for statistical analysis

## 🧹 Data Cleaning Steps

- Dropped irrelevant columns: `Events`, `Date`, `SeaLevelPressureHighInches`, `SeaLevelPressureLowInches`
- Replaced:
  - `'T'` (trace precipitation) with `0.0`
  - `'-'` (missing data) with `0.0`
- Converted all columns to numerical datatypes (`int64` or `float64`).
- Verified that there were no missing or duplicated entries.

## 📊 Basic Statistical Analysis

For each feature, the notebook computed:

- **Mean**
- **Trimmed Mean** (after removing top and bottom 10% of the data)
- **Median**
- **95% Confidence Interval** of the mean

These steps help understand the central tendency and variability of weather-related parameters.

## ▶️ How to Run the Notebook

1. Ensure you have `austin_weather.csv` in the same directory.
2. Install necessary libraries:
   ```bash
   pip install pandas numpy scipy
3. Launch Jupyter Notebook and open `Rainfall.ipynb`:
   ```bash
   jupyter notebook
4. Execute all cells sequentially.
