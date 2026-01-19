# GDP-Forecasting-Pipeline-using-ARIMA
This project builds an end-to-end forecasting pipeline to predict GDP per capita (USD) for multiple countries using the ARIMA time-series model.
The pipeline automates:
- Data preprocessing and cleaning
- Model training and forecasting (1–5 years ahead)
- Evaluation using Mean Absolute Error (MAE)
- Consolidated results table with forecasts and error metrics
# Motivation
Forecasting GDP is crucial for economic planning, policy-making, and business strategy.
ARIMA was chosen for its interpretability and effectiveness in modeling time-series data with trends and seasonality.
# Dataset
- Source: World Bank Economic Indicators (Excel file)
- Key variables: GDP per capita, Birth Rate, Death Rate, Electric Power Consumption, Infant Mortality Rate, Unemployment Rate, Population Density, Life Expectancy, Internet Usage Rate
- Preprocessing:
- Renamed columns for readability
- Sorted by country and year
- Dropped missing values
- Filtered countries with at least 10 years of GDP data
⚙️ Methodology
1. Data Preparation
- Converted Year column to datetime index
- Split into train (all but last 5 years) and test (last 5 years)
2. Modeling
- Applied ARIMA(1,1,1) model for each country
- Forecasted GDP per capita for 5 years ahead
3. Evaluation
- Compared forecasts with actual test data
- Computed Mean Absolute Error (MAE)
4.  Results Consolidation
- Created a results table with:
- Country name
- Forecasts for Year 1–5
- MAE
