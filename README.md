# Road Accident Fatality Prediction System

A machine learning-based system that analyzes road accident data and predicts accident fatality severity using historical accident records. The project focuses on identifying high-fatality accidents and evaluating models based on their ability to detect severe outcomes.

## Overview

This project uses the Fatality Analysis Reporting System (FARS) 2023 dataset, containing over 37,000 accident records, to build a classification system that distinguishes between low-fatality and high-fatality accidents.

The objective is to identify accident conditions associated with higher fatality risk and develop a predictive model that can effectively recognize severe accidents.

## Key Features

- Data preprocessing and exploratory data analysis.
- Feature engineering and selection.
- Classification of accidents into low-fatality and high-fatality categories.
- Comparison of multiple machine learning models.
- Model evaluation using precision, recall and ROC-AUC.
- Interactive prediction interface using Streamlit.

## Tech Stack

- **Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn, LightGBM, XGBoost
- **Deployment:** Streamlit

## Machine Learning Approach

The project follows a structured machine learning workflow:

1. Data collection and preprocessing.
2. Exploratory data analysis to understand accident patterns.
3. Feature engineering and preparation.
4. Model training and comparison.
5. Hyperparameter tuning and evaluation.
6. Integration of the selected model into a Streamlit application.

Multiple classification algorithms were explored, with LightGBM selected as the final model based on evaluation results.

## Model Performance

The final LightGBM model achieved:

| Metric | Result |
|---|---:|
| High-fatality Recall | 90% |
| ROC-AUC | 0.889 |

The model prioritizes identifying high-fatality cases, making recall an important evaluation metric.

## Project Structure

```text
Accident-Fatality-Prediction/
│
├── app.py
├── assets/
│
├── code/
│   └── eda and visualiztion/
│
├── model/
│   ├── encoders.pkl
│   ├── categorical_unique.pkl
│   ├── lgbm_model.pkl
│   ├── stack_features.pkl
│   └── train_features.pkl
│
├── .gitignore
└── README.md
```

Note: The large stacked model artifact and raw dataset are excluded from the repository. The application may require additional model files if the stacked model is used.

## Installation and Setup

1. Clone the repository:

```bash
git clone YOUR_REPOSITORY_URL
cd Accident-Fatality-Prediction
```

2. Install dependencies:

```bash
pip install pandas numpy scikit-learn lightgbm xgboost streamlit matplotlib seaborn
```

3. Run the Streamlit application:

```bash
streamlit run app.py
```

## Future Improvements

- Explore additional ensemble learning techniques.
- Improve model generalization through further validation.
- Incorporate more recent accident datasets.
- Enhance the prediction interface and visualization.
- Investigate explainable AI techniques for understanding model predictions.

## Author

**Your Name**

B.Tech Computer Science and Engineering  
Jaypee Institute of Information Technology, Noida
