# Dividend Stock Predictions

## Project Overview

This project explores stock price movements around dividend payout dates using machine learning techniques. The main objectives are to:

1. Analyze patterns of dividend-paying stocks
2. Understand stock price behavior around ex-dividend dates
3. Evaluate the viability of shorting stocks before dividend payouts
4. Assess the effectiveness of the dividend capture method

## Dataset

The dataset contains historical stock market data from Yahoo Finance for the 500 largest companies by market capitalization, spanning a five-year period. It includes daily records of:

- Stock prices (Open, High, Low, Close)
- Trading volume
- Dividends
- Stock splits
- Adjusted closing prices

## Methodology

1. **Data Preprocessing**: 
   - Handling missing values
   - Treating outliers
   - Feature engineering (e.g., creating date-related features)
   - Scaling numeric features
   - One-hot encoding for categorical variables

2. **Exploratory Data Analysis (EDA)**:
   - Visualizing dividend trends over time
   - Analyzing average dividend yields
   - Identifying top dividend-paying companies

3. **Model Implementation**:
   Three models were implemented and compared:
   - Logistic Regression (baseline)
   - Decision Tree
   - Random Forest

4. **Model Evaluation**:
   - Time series cross-validation
   - Metrics: Precision, Recall, F1-score, AUC-ROC
   - Confusion matrices
   - Feature importance analysis (for Random Forest)

## Key Findings

- The Random Forest model performed best, with an F1-score of 0.97 on the test set.
- Feature importance analysis from the Random Forest model identified key factors predicting stock price movements after dividend payouts.
- The models can be used to assess the likelihood of price drops and help time short positions.
- For the dividend capture strategy, the models can predict potential price rebounds after the ex-dividend date.

## Future Work

- Explore advanced ensemble methods like XGBoost or LightGBM
- Implement time-series specific models (e.g., LSTMs) to capture temporal dependencies
- Incorporate additional features such as company financials or market sentiment

## Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- imbalanced-learn (for SMOTE)

## Usage

1. Clone the repository
2. Install required packages: `pip install -r requirements.txt`
3. Run the Jupyter notebook: `jupyter notebook Dividend-Stock-Predictions.ipynb`

## License

This project is open source and available under the [MIT License](LICENSE).
