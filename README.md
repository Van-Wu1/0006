# CASA0006 Coursework – Predicting Road Traffic Accident Severity with Machine Learning

## Project Overview

This project investigates whether supervised machine learning models can accurately predict the severity of road traffic accidents in London. The study integrates spatial network indicators with traditional contextual features to enhance model performance and interpretability.

## Dataset

- **Primary source**: UK Department for Transport Road Safety Data (2015–2019)
- **Additional data**: Road network centrality metrics (betweenness, degree) computed from OpenStreetMap using `OSMnx`
- **Data processing**: Final modeling dataset contains 128,261 records and 87 numerical features after preprocessing

> ⚠️ Note: The raw file was removed from the Git history to comply with GitHub's 100MB file size limit. 

## Raw Data Requirement

To fully reproduce the notebook, you need to manually download the original raw dataset (approx. 1.3GB) from the UK Department for Transport:

**[Download Link (CSV)](https://data.dft.gov.uk/road-accidents-safety-data/dft-road-casualty-statistics-collision-1979-latest-published-year.csv)**

After downloading, please place the file in the following path relative to the project root:
```
../data/raw/
```

> Filename should be: `dft-road-casualty-statistics-collision-1979-latest-published-year.csv`



## Models Used

- Logistic Regression  
- Random Forest  
- XGBoost  

The models were evaluated using macro-F1 and per-class recall to address class imbalance.

## Key Findings

- **Random Forest** offered the best balance of performance and interpretability (macro-F1: 0.35)
- SHAP analysis identified key predictors such as:
  - `time_hour`, `day_of_week`, `second_road_class`
  - Network-based feature: `max_betweenness`

## File Structure
```
.
├── data/
│   ├── clean/
│   ├── final/                         
│   └── raw/                           
├── scr/
│   └── test/                          # Blocks files for test
├── YifanWu_0006_submission.ipynb      # Jupyter Notebook (main analysis)
├── YifanWu_0006_submission.pdf        # Exported report in PDF format
├── flowchart.png                      
└── README.md

```
## Author

Yifan Wu  
UCL CASA – Data Science for Spatial Systems  
April 2025