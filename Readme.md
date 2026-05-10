1. DATA SOURCES
2. DATA COLLECTION PIPELINE
3. MASTER DATASET CREATION

# COMPLETE DATA COLLECTION ARCHITECTURE

```
Web APIs / CSV / Government Data
                ↓
      Python Data Collection
                ↓
        Raw CSV Files
                ↓
      Cleaning & Alignment
                ↓
      Master Economic Dataset
                ↓
     Dashboard + ML Models
```

# FOLDER STRUCTURE

```
project/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── external/
│
├── notebooks/
├── scripts/
└── dashboard/

```


# STEP 1 — INSTALL REQUIRED LIBRARIES

```
pip install pandas yfinance requests beautifulsoup4
pip install matplotlib seaborn plotly
pip install textblob nltk

```

# WHAT YOU SHOULD CHECK IN EVERY DATASET

```

Check	              Why
----------          -------------
Missing values	    Avoid errors
Duplicate dates	    Merge issues
Wrong formats	    Parsing errors
Frequency mismatch	Daily vs monthly
Time zones       	Consistency
Nulls	            ML problems

```
# Rupee Instability Dashboard and Predictor
-------------------------------------------
## Inflation Data Preprocessing
-------------------------------
This module preprocesses CPI (Consumer Price Index) and inflation data for the Rupee Instability Dashboard and Predictor project.

The script reads raw CPI data from an Excel file, cleans and formats the dataset, handles missing values, and exports the processed data as a CSV file.

---

## Features

- Read CPI data from Excel
- Filter data for All India
- Clean and format columns
- Create proper date column
- Handle missing values
- Export processed dataset as CSV

---

## Technologies Used

- Python
- Pandas
- NumPy
- OpenPyXL

---

## Project Structure

```bash
Ruppee-Instability-Dashboard-and-pridictor/
│
├── data/
│   ├── raw/
│   │   └── cpi_1133.xlsx
│   │
│   └── processed/
│       └── inflation.csv
│
├── preprocess_inflation.py
├── requirements.txt
└── README.md


# Rupee Instability Dashboard and Predictor
-----------------------------------------
## FPI Data Preprocessing
---------------------------
This module preprocesses Foreign Portfolio Investment (FPI/FII) flow data collected from multiple yearly `.xls` files.

The script reads raw FPI files, cleans and merges the data, creates useful financial indicators, and exports the processed dataset as a CSV file.

---

## Features

- Read multiple yearly FPI files
- Merge datasets automatically
- Clean and format financial data
- Convert dates into datetime format
- Remove duplicate records
- Create flow-based indicators
- Export processed dataset as CSV

---

## Technologies Used

- Python
- Pandas
- Glob
- XLRD

---

## Project Structure

```bash
Ruppee-Instability-Dashboard-and-pridictor/
│
├── data/
│   ├── raw/
│   │   └── fpi/
│   │       ├── FPI 2015.xls
│   │       ├── FPI 2016.xls
│   │       └── ...
│   │
│   └── processed/
│       └── fpi_master.csv
│
├── preprocess_fpi.py
├── requirements.txt
└── README.md


# Rupee Instability Dashboard and Predictor
-------------------------------------------

## Foreign Exchange Reserves Data Preprocessing
-------------------------------------------------
This module preprocesses India's Foreign Exchange Reserves dataset collected from Excel files.

The script cleans reserve data, formats dates, converts numeric values, and exports a processed CSV file for analysis and dashboard visualization.

---

## Features

- Read reserve Excel data
- Clean and format reserve values
- Convert month names into dates
- Handle missing values
- Sort historical data
- Export processed dataset as CSV

---

## Technologies Used

- Python
- Pandas
- NumPy
- OpenPyXL

---

## Project Structure

```bash
Ruppee-Instability-Dashboard-and-pridictor/
│
├── data/
│   ├── raw/
│   │   └── Foreign Exchange Reserves.xlsx
│   │
│   └── processed/
│       └── forex_reserves.csv
│
├── preprocess_forex.py
├── requirements.txt
└── README.md


# Rupee Instability Dashboard and Predictor
------------------------------------------
## NIFTY 50 Market Data Preprocessing
-------------------------------------
This module downloads and preprocesses historical NIFTY 50 market data using the `yfinance` library.

The script fetches market data, cleans and formats it, calculates daily returns, and exports the processed dataset as a CSV file.

---

## Features

- Download historical NIFTY 50 data
- Clean and format market data
- Convert columns into numeric format
- Handle missing values
- Calculate daily market returns
- Export processed dataset as CSV

---

## Technologies Used

- Python
- Pandas
- NumPy
- yFinance

---

## Project Structure

```bash
Ruppee-Instability-Dashboard-and-pridictor/
│
├── data/
│   └── processed/
│       └── nifty_data.csv
│
├── preprocess_nifty.py
├── requirements.txt
└── README.md


# Rupee Instability Dashboard and Predictor
-------------------------------------------

## DXY (US Dollar Index) Data Preprocessing
---------------------------------------------
This module downloads and preprocesses historical DXY (US Dollar Index) data using the `yfinance` library.

The script fetches DXY market data, cleans and formats the dataset, calculates percentage changes, and exports the processed data as a CSV file.

---

## Features

- Download historical DXY data
- Clean and format financial data
- Convert columns into numeric format
- Handle missing values
- Calculate daily DXY percentage change
- Export processed dataset as CSV

---

## Technologies Used

- Python
- Pandas
- NumPy
- yFinance

---

## Project Structure

```bash
Ruppee-Instability-Dashboard-and-pridictor/
│
├── data/
│   └── processed/
│       └── dxy_data.csv
│
├── preprocess_dxy.py
├── requirements.txt
└── README.md


# Rupee Instability Dashboard and Predictor
-------------------------------------------
## Oil Price Dataset Preprocessing
-----------------------------------
This module preprocesses Brent crude oil price data for the Rupee Instability Dashboard and Predictor project.

The notebook loads oil price data from a local CSV file or downloads it using `yfinance`, cleans the dataset, creates financial indicators, and exports the processed data as a CSV file.

---

## Features

- Load oil price data from CSV or Yahoo Finance
- Download Brent crude oil data automatically
- Clean and format market data
- Remove duplicate and missing values
- Create moving averages and volatility indicators
- Calculate daily oil returns
- Export processed dataset as CSV

---

## Technologies Used

- Python
- Pandas
- NumPy
- yFinance
- Pathlib

---

## Project Structure

```bash
Ruppee-Instability-Dashboard-and-pridictor/
│
├── data/
│   ├── raw/
│   │   └── oil_prices.csv
│   │
│   └── processed/
│       └── oil_prices_preprocessed.csv
│
├── notebooks/
│   └── oil_price_preprocessing.ipynb
│
├── requirements.txt
└── README.md


# Rupee Instability Dashboard and Predictor
------------------------------------------
## USD/INR Dataset Preprocessing
----------------------------------
This notebook preprocesses historical USD/INR exchange rate data downloaded from Yahoo Finance.

The notebook cleans the dataset, creates time-series features, generates forecasting target variables, and exports a model-ready CSV file.

---

## Features

- Clean raw USD/INR data
- Handle missing and duplicate values
- Convert columns into numeric format
- Create time-series and volatility features
- Generate lag-based features
- Create forecasting target variables
- Export model-ready dataset

---

## Technologies Used

- Python
- Pandas
- NumPy
- Pathlib

---

## Project Structure

```bash
Ruppee-Instability-Dashboard-and-pridictor/
│
├── data/
│   ├── raw/
│   │   └── usd_inr.csv
│   │
│   └── processed/
│       └── usd_inr_preprocessed.csv
│
├── notebooks/
│   └── usd_inr_preprocessing.ipynb
│
├── requirements.txt
└── README.md


# Rupee Instability Dashboard and Predictor
-------------------------------------------
## Master Dataset Creation and Feature Engineering
-----------------------------------------------------
This module merges multiple processed financial and economic datasets into a single master dataset for the Rupee Instability Dashboard and Predictor project.

The final dataset combines exchange rate data, oil prices, DXY index, NIFTY index, forex reserves, inflation, and FPI flows into one unified dataset for analysis and forecasting.

---

## Datasets Used

| Dataset | Description |
|---|---|
| USD/INR | Exchange rate data |
| Oil Data | Crude oil prices |
| DXY Data | US Dollar Index |
| NIFTY Data | Indian stock market index |
| Forex Reserves | India's forex reserves |
| Inflation | CPI inflation data |
| FPI Data | Foreign investment flows |

---

## Features

- Merge multiple processed datasets
- Clean and align date-based records
- Handle missing values
- Create financial indicators
- Generate engineered features
- Export master dataset for analysis and prediction

---

## Technologies Used

- Python
- Pandas
- NumPy

---

## Project Structure

```bash
Ruppee-Instability-Dashboard-and-pridictor/
│
├── data/
│   ├── processed/
│   │   ├── usd_inr_preprocessed.csv
│   │   ├── oil_prices_preprocessed.csv
│   │   ├── dxy_data.csv
│   │   ├── nifty_data.csv
│   │   ├── forex_reserves.csv
│   │   ├── inflation.csv
│   │   └── fpi_master.csv
│   │
│   └── final/
│       └── master_dataset.csv
│
├── create_master_dataset.py
├── requirements.txt
└── README.md