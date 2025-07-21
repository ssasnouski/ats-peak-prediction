# Peak ATS Load Forecasting for Energy Trading

## Project Overview
Energy supply companies need to predict peak electricity consumption hours (ATS) 1-2 days in advance for trading calculations. This project builds a model to:
- Forecast peak hours within regulatory windows (9:00-12:00 and 15:00-21:00)
- Handle unique data challenges (missing weekends/holidays data)
- Incorporate exogenous predictors (SO system operator data and planned UES values)

## Key Features
- **Data Pipeline**: Merges ATS, SO, and UES data with calendar features
- **Feature Engineering**:
  - Lag features (1h, 2h, 24h, 48h)
  - Rolling statistics
  - Holiday/weekend indicators
  - Weather integration
- **Modeling**: Probability forecasting for 24-hour peaks using XGBoost
- **Evaluation**: Custom metrics for peak hour accuracy

## Usage
1. Install dependencies:
```bash
pip install -r requirements.txt
