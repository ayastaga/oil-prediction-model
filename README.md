# Oil Price Prediction Model  
*An exploratory machine‑learning project using linear regression to forecast oil prices.*

## Table of Contents  
1. [Project Overview](#project‐overview)  
2. [Motivation](#motivation)  
3. [Dataset](#dataset)  
4. [Model & Methodology](#model‐&‐methodology)  
5. [Usage](#usage)  
6. [Results & Interpretation](#results‐&‐interpretation)  
7. [Limitations & Future Work](#limitations‐&‐future‐work)  
8. [Directory Structure](#directory‐structure)  
9. [Dependencies](#dependencies)  
10. [License](#license)  
11. [Contact](#contact)  

---

## Project Overview  
This repository contains an older project that applies linear regression techniques to historical oil‑price data (specifically the WTI spot price) in order to predict future price movements. The goal is to showcase the end‑to‑end process: data ingestion, cleaning, model training, evaluation, and interpretation.  

## Motivation  
Forecasting commodity prices such as oil is a challenging but interesting problem because of the many influencing factors (geopolitics, supply/demand, macroeconomics). While this model utilises a simple approach (linear regression), it provides a baseline against which more complex algorithms might later be compared.

## Dataset  
The dataset used is:  
- **Cushing, OK WTI Spot Price FOB** (.csv) — historic spot price data for WTI crude oil.  
  - Source: included in the repository (`Cushing_OK_WTI_Spot_Price_FOB.csv`)  
  - Time‑span, format, any preprocessing steps are documented inside the notebook.  
  
Ensure when you re‑run or extend this model you are aware of:
- All missing values, date parsing and indexing by time‑series.  
- Feature generation or any transformations applied.

## Model & Methodology  
The modelling approach followed these steps:
- Exploratory data analysis (visualising trends, seasonality, stationarity, etc).  
- Feature engineering (e.g., lag features, moving averages).  
- Split into training and test sets (time‑series aware).  
- Train a linear regression model to predict oil price at a future time point given past values.  
- Evaluate using appropriate metrics (e.g., RMSE, MAE) and visualise actual vs predicted.  
- Interpret the results and discuss how well the simple linear model performs.

The main work is contained in:
- `Machine_Learning__Oil_Prices_Prediction_[Linear_Regression].ipynb`  
- `[OLD_MODEL]_Machine_Learning__Oil_Price_Prediction.ipynb` (an earlier version)

## Usage  
To run this project locally:
1. Clone this repository:
   ```bash
   git clone https://github.com/ayastaga/oil-prediction-model.git
   cd oil-prediction-model```
2. Set up a Python environment (e.g., with venv or conda) and install dependencies
   ```bash
   pip install -r requirements.txt```
3. Launch the notebook:
   ```bash
   jupyter notebook```
4. Open `Machine_Learning__Oil_Prices_Prediction_[Linear_Regression].ipynb` and run the cells. Modify or extend the model as desired (e.g., try other regression algorithms or add features)

## Results & Interpretation
- The model provides a baseline forecast of future oil prices.
- Performance metrics (RMSE/MAE) and plots show prediction accuracy over time.
- Interpretations of feature importance, lag effects, and residuals are discussed in the notebook.

## Limitations & Future Work

### Limitations:
- Linear regression may not capture non-linear relationships or market shifts.
- Exogenous factors like geopolitics or supply shocks are not modeled.
- Stationarity, autocorrelation, and heteroskedasticity may affect reliability.

### Future Work:
- Explore advanced models: ARIMA, LSTM, or gradient boosting.
- Include external features: inventory levels, geopolitical indices, macroeconomic indicators.
- Use rolling forecasts or walk-forward validation.
- Deploy as a web app or schedule periodic retraining.

## Directory Structure
```
/oil-prediction-model  
├── Cushing_OK_WTI_Spot_Price_FOB.csv  
├── Machine_Learning__Oil_Prices_Prediction_[Linear_Regression].ipynb  
├── [OLD_MODEL]_Machine_Learning__Oil_Price_Prediction.ipynb  
├── LICENSE  
└── README.md
```

## Dependencies
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## License
This project is licensed under the MIT License.

## Contact
For questions or collaboration, please reach out to the author. 
