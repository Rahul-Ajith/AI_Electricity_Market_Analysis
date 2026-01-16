# AI-Based Electricity Market Price Trend Analysis and Prediction

## Project Overview

This project implements AI-based models for predicting electricity market prices using historical data from Nord Pool, Europe's leading power market. The system analyzes historical price trends and forecasts future electricity prices using both statistical time-series methods (ARIMA) and machine learning approaches (Random Forest).

## Dataset

- **Source:** Nord Pool Market Data
- **Region:** Denmark (Price Areas DK1 and DK2)
- **Format:** CSV file with hourly electricity price data
- **Features:** 
  - Timestamps (HourUTC, HourDK)
  - Price areas (DK1, DK2)
  - Spot prices in EUR and DKK
  - Purchase and sale volumes

## Models Used

1. **ARIMA (AutoRegressive Integrated Moving Average)**
   - Classical time-series forecasting method
   - Captures temporal dependencies and trends
   - Baseline statistical approach

2. **Random Forest Regressor**
   - Ensemble machine learning method
   - Utilizes engineered features (lags, rolling statistics, time features)
   - Captures complex non-linear relationships

## Project Structure

```
ai_pricing_prediciton/
├── project_notebook.ipynb    # Main Jupyter notebook with complete analysis
├── NordpoolMarket.csv        # Dataset
├── requirements.txt          # Python dependencies
└── README.md                # This file
```

## Installation

1. Clone or download this repository

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Ensure the dataset `NordpoolMarket.csv` is in the project directory

## How to Run

1. Open the Jupyter notebook:
```bash
jupyter notebook project_notebook.ipynb
```

2. Run all cells sequentially (Cell → Run All) or execute cells one by one

3. The notebook includes:
   - Data loading and exploration
   - Data preprocessing and feature engineering
   - Model training (ARIMA and Random Forest)
   - Model evaluation and visualization
   - Results analysis

## Evaluation Metrics

The models are evaluated using three standard regression metrics:

- **MAE (Mean Absolute Error):** Average absolute difference between predicted and actual values
- **RMSE (Root Mean Squared Error):** Penalizes larger errors more heavily
- **MAPE (Mean Absolute Percentage Error):** Percentage-based error metric

## Results Summary

The notebook provides detailed performance comparison between ARIMA and Random Forest models, including:
- Prediction accuracy metrics
- Visualization of predicted vs actual prices
- Feature importance analysis
- Residual analysis

## Key Features

- **Comprehensive EDA:** Data exploration with visualizations
- **Feature Engineering:** Creation of temporal and lag features
- **Model Comparison:** Side-by-side evaluation of different approaches
- **Ethical Considerations:** Discussion of responsible AI usage in energy markets
- **Documentation:** Detailed explanations of methods and results

## Ethical Considerations

This project includes a dedicated section on ethical considerations, discussing:
- Dataset limitations and market volatility
- Bias in historical pricing patterns
- Risks of using AI predictions in real electricity trading
- Guidelines for responsible AI deployment

## Future Improvements

Potential enhancements include:
- LSTM/Transformer deep learning models
- Integration of external data (weather, demand forecasts)
- Real-time prediction APIs
- Multi-region modeling
- Uncertainty quantification

## Author

[Your Name]  
[Your University]  
[Date]

## License

This project is for educational and research purposes.

## Acknowledgments

- Nord Pool for providing market data
- Open-source Python libraries (pandas, scikit-learn, statsmodels, etc.)
