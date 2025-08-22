# Indian Airfare ML Prediction

A machine learning project that predicts Indian domestic airline ticket prices using various regression models.

## Project Overview

This project analyzes Indian domestic flight data to build predictive models for airline ticket prices. The analysis includes data cleaning, exploratory data analysis, and comparison of multiple machine learning algorithms including Ridge Regression, K-Nearest Neighbors, Random Forest, and Boosted Trees.

## Features

- **Data Cleaning**: Comprehensive preprocessing of flight data including date/time parsing, categorical encoding, and missing value handling
- **Exploratory Data Analysis**: Visual analysis of price distributions, correlations, and categorical variable relationships
- **Multiple ML Models**: Implementation and comparison of four different regression models
- **Cross-Validation**: 10-fold stratified cross-validation for robust model evaluation
- **Model Selection**: Automated hyperparameter tuning and model selection based on RMSE

## Dataset

The dataset contains 10,683 observations of Indian domestic flights with the following features:
- **Flight Details**: Airline, source, destination, total stops, duration
- **Temporal Features**: Journey date, departure time
- **Target Variable**: Price (in Indian Rupees)

## Models Evaluated

1. **Ridge Regression**: Linear model with L2 regularization
2. **K-Nearest Neighbors**: Non-parametric regression
3. **Random Forest**: Ensemble tree-based model
4. **Boosted Trees**: Gradient boosting with XGBoost

## Results

The **Boosted Trees model** performed best with an RMSE of 1,874.88 on the test set, representing approximately 2.4% error relative to the price range.

## Key Findings

- Flight duration has the strongest correlation with price (0.74)
- Number of stops moderately correlates with price (0.51)
- Premium/Business class tickets significantly impact pricing
- Jet Airways and IndiGo are among the most expensive airlines

## Project Structure

```
indian-airfare-ml-prediction/
├── README.md                           # Project documentation
├── PredictingIndianAirfares.Rmd        # Main analysis notebook
├── PredictingIndianAirfares.pdf        # Compiled report
├── data/                               # Data files
│   ├── IndianAirfareData.xlsx          # Original dataset
│   └── PredictingIndianAirfareCodebook.pdf  # Data documentation
├── models/                             # Trained models
│   ├── bt_final_fit_train.rda          # Best boosted trees model
│   ├── bt_tune.rda                     # Boosted trees tuning results
│   ├── knn_tune.rda                    # KNN tuning results
│   ├── rf_tune.rda                     # Random forest tuning results
│   └── ridge_tune.rda                  # Ridge regression tuning results
├── results/                            # Model outputs
│   └── airplane_tibble.rda             # Test set predictions
└── images/                             # Project images
    ├── Airplane1.jpg
    ├── Airplane2.jpg
    └── airline_jet_flying_out_of_laptop.jpg
```

## Technologies Used

- **R**: Primary programming language
- **Tidyverse**: Data manipulation and visualization
- **Tidymodels**: Machine learning framework
- **XGBoost**: Gradient boosting implementation
- **Ranger**: Random forest implementation

## Author

Nazhah Mir

## License

This project is for educational purposes. Please refer to the original dataset source for licensing information. 