# flight-delay-prediction-model-analysis
Flight Delay Prediction: Model Comparison Study

**Note:** The notebook uses a subset of the full flight delay dataset (sample_flights.csv) for demonstration purposes.  
R² values and other metrics will differ from the full dataset, but the workflow, feature engineering, and model evaluation logic remain accurate.

Project Overview

This project analyzes U.S. flight delay data to evaluate whether daily average flight delays can be accurately predicted, and whether a complex time-series model (Facebook Prophet) outperforms a simpler Linear Regression approach.

The focus is on selecting models based on data structure and assumptions, rather than defaulting to sophisticated techniques, highlighting analytical judgment that is essential for real-world data analysis.


Dataset

Source: U.S. Department of Transportation (via Kaggle)

Dataset: Airline Delay and Cancellation Data

Scope: Historical flight performance data aggregated to daily average delays

Note: Due to file size, the raw dataset is not included.

Link: https://www.kaggle.com/datasets/usdot/flight-delays


Methodology

Data Preparation

Aggregated raw flight-level data to daily averages

Cleaned and formatted time-based features

Converted dates into numerical format for regression modeling


Models Evaluated

Linear Regression – captures long-term trend behavior without assuming seasonality

Facebook Prophet – time-series forecasting model assuming recurring seasonal patterns


Train/Test Strategy

Chronological train-test split

Final portion of the dataset held out to simulate real-world forecasting conditions


Model Evaluation Metrics

R² (Coefficient of Determination)

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)


Results
Model	R² Score
Linear Regression	0.9276
Facebook Prophet	-0.7872


Key Observations

Linear Regression explained over 92% of variance in daily flight delays

Prophet underperformed, producing a negative R²

Visualization confirmed Linear Regression closely tracked actual delays, while Prophet failed to capture the data structure


Key Insights

Model complexity does not guarantee better performance

Daily aggregation removed seasonal signals needed for Prophet

Trend-based behavior better explains daily flight delays

Proper evaluation prevents overconfidence in complex models


Limitations

Daily aggregation removes intra-day and flight-level seasonality

External variables such as weather, holidays, and airport congestion were not included

Findings apply specifically to daily-level delay prediction


Impact & Applications

Accurate prediction of flight delays can support:

Airline scheduling and operational planning

Staffing decisions

Customer communication and service improvements

More importantly, this project demonstrates analytical reasoning—choosing the right model based on data behavior rather than popularity.


Tools & Technologies

Python, Pandas, NumPy

Scikit-learn

Facebook Prophet

Matplotlib

Repository Structure
├── project3.ipynb
├── README.md

Key Takeaway

Choosing the right model is about understanding data structure and limitations, not model complexity. This mindset is crucial for delivering actionable insights in real-world analytics projects.
