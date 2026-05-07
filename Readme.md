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



