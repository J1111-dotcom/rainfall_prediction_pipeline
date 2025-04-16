# Will It Rain Tomorrow? Predicting Rainfall with Machine Learning

This project explores the use of machine learning to predict whether it will rain tomorrow in Australia using historical weather data. The dataset includes daily observations such as temperature, humidity, pressure, wind speed, and more.

The goal was to build an end-to-end binary classification pipeline with thoughtful preprocessing, feature engineering, model training, and evaluation — all while extracting insights into what weather patterns most influence rainfall.


## Project Highlights

- Built an end-to-end ML pipeline using `scikit-learn`, `pandas`, and `matplotlib`
- Applied imputation strategies for missing data (median, mode)
- Engineered a seasonal feature from the date field
- Tuned a `RandomForestClassifier` using `GridSearchCV` with stratified k-fold cross-validation
- Compared performance with a `LogisticRegression` baseline
- Visualized feature importances to identify key drivers of rainfall


## Key Insights

- The final Random Forest model achieved **85.8% test accuracy** with strong performance on non-rainy days and modest recall on rainy days.
- **Humidity and pressure at 3pm**, along with recent rainfall and wind speed, were the most influential features.
- Logistic Regression served as a lighter, interpretable baseline with similar recall but slightly lower precision.


## Repository Structure

rainfall-prediction-pipeline/ ├── data/ # Contains Rainfall_Australia.csv (not committed) ├── notebooks/ │ └── rainfall_prediction_pipeline.ipynb ├── images/ # Visuals (e.g., feature importance, confusion matrix) ├── README.md # This file └── requirements.txt # (Optional) for environment setup


## Dataset

The dataset was sourced from the [Australian Bureau of Meteorology via Kaggle](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package).  
A local copy (`Rainfall_Australia.csv`) is stored in the `/data/` folder for stability and reproducibility.


## Future Enhancements

- Optimize recall for rainy days using F1-score or class-weight tuning
- Explore temporal modeling or lagged features
- Test tree boosting models (e.g., XGBoost, LightGBM)
- Deploy as a basic weather alert tool or REST API


## Portfolio Context

This project is part of a broader portfolio showcasing practical applications of data science across analytics, visualization, and machine learning.  
For more projects, visit [My GitHub Portfolio](https://github.com/J1111-dotcom).
