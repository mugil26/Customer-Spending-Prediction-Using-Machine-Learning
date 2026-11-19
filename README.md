# Customer Spending Prediction Using Machine Learning

## Project Overview

This project focuses on predicting customer spending amounts using machine learning algorithms based on customer demographics, income, website activity, purchasing history, membership type, and shopping preferences.

The project uses Python, Pandas, and Scikit-learn to perform data cleaning, exploratory data analysis, preprocessing, model training, and performance evaluation. Multiple regression algorithms are compared to identify the best-performing model.

A Streamlit web application is developed to allow users to enter customer details and predict their expected spending amount interactively.

## Key Features

- Loading and inspecting customer shopping datasets
- Exploratory Data Analysis (EDA)
- Identifying and handling missing values
- Checking duplicate records
- Generating descriptive statistical summaries
- Separating numerical and categorical features
- Handling missing numerical and categorical values
- Encoding categorical variables using One-Hot Encoding
- Scaling numerical features using StandardScaler
- Splitting data into training and testing sets
- Building machine learning pipelines
- Training and comparing multiple regression models
- Evaluating models using R² Score, Mean Squared Error (MSE), and Mean Absolute Error (MAE)
- Selecting the best-performing regression model
- Saving the trained model using Pickle
- Developing an interactive Streamlit application
- Predicting customer spending based on user-provided inputs

## Dataset Overview

The project uses the `ShopSmart_data.csv` dataset.

The dataset includes customer-related information used to predict spending behavior.

| Column | Description |
|---|---|
| Age | Customer's age |
| Annual_Income | Customer's annual income |
| Website_Visits | Number of website visits |
| Previous_Purchases | Number of previous purchases |
| Membership_Type | Customer membership category |
| Preferred_Category | Customer's preferred shopping category |
| City_Tier | Customer's city classification |
| Discount_Used | Indicates whether a discount was used |
| Amount_Spent | Target variable representing customer spending |

## Data Cleaning and Preprocessing

The project performs the following preprocessing operations:

- Checks dataset structure and data types.
- Identifies missing values in the dataset.
- Fills missing annual income values using the mean.
- Fills missing website visits using the mean.
- Fills missing membership types using the mode.
- Fills missing preferred categories using the mode.
- Checks duplicate records.
- Generates descriptive statistical summaries.

## Machine Learning Models

The project trains and compares six regression algorithms using Scikit-learn pipelines.

| Algorithm | Description |
|---|---|
| Linear Regression | Predicts spending using a linear relationship between input features and target values. |
| Ridge Regression | Applies L2 regularization to reduce overfitting. |
| Lasso Regression | Applies L1 regularization for feature selection and model simplification. |
| K-Nearest Neighbors (KNN) | Predicts spending based on nearby data points. |
| Decision Tree Regressor | Uses decision rules to predict customer spending. |
| Random Forest Regressor | Combines multiple decision trees to improve prediction performance. |

## Model Evaluation

The models are evaluated using three regression performance metrics:

- **R² Score:** Measures how well the model explains variations in customer spending.
- **Mean Squared Error (MSE):** Measures the average squared difference between actual and predicted values.
- **Mean Absolute Error (MAE):** Measures the average absolute prediction error.

The best-performing model is selected based on the highest R² score.

The selected model pipeline is saved as `best_model_pipeline.pkl` for future predictions.

## Streamlit Web Application

An interactive web application is developed using Streamlit.

Users can enter the following customer details:

- Age
- Annual Income
- Website Visits
- Previous Purchases
- Membership Type
- Preferred Category
- City Tier
- Discount Used

After entering the details and clicking the **Predict Spend** button, the application displays the predicted customer spending amount in Indian Rupees (₹).

## Technologies Used

- Python – Programming language used for data analysis and machine learning.
- Jupyter Notebook – Environment for experimentation and model development.
- Streamlit – Framework used to develop the interactive prediction application.
- Scikit-learn – Machine learning algorithms, preprocessing, pipelines, and evaluation.

## Libraries Used

| Library | Purpose |
|---|---|
| Pandas | Data loading, cleaning, manipulation, and analysis. |
| Seaborn | Exploratory data analysis and data visualization. |
| Scikit-learn | Model training, preprocessing, pipelines, and performance evaluation. |
| Pickle | Saving and loading the trained machine learning pipeline. |
| Streamlit | Building the interactive web application. |

## Project Files

- `expriment.ipynb` – Jupyter Notebook containing data preprocessing, model training, and evaluation.
- `app(1).py` – Streamlit application for predicting customer spending.
- `best_model_pipeline.pkl` – Saved best-performing machine learning pipeline.
- `ShopSmart_data.csv` – Original customer shopping dataset used for model development.
- `cleaned_data.csv` – Cleaned dataset used by the Streamlit application.
- `logo.png` – Logo displayed in the Streamlit application's sidebar.

## How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

### 2. Install Required Libraries

```bash
pip install pandas numpy seaborn scikit-learn streamlit
```

### 3. Run the Jupyter Notebook

```bash
jupyter notebook
```

Open `expriment.ipynb` and execute the cells in order to perform data preprocessing, model training, evaluation, and model saving.

### 4. Run the Streamlit Application

Make sure the following files are available in the project directory:

- `app(1).py`
- `best_model_pipeline.pkl`
- `cleaned_data.csv`
- `logo.png`

Run the application:

```bash
streamlit run "app(1).py"
```

### 5. Make Predictions

1. Open the Streamlit application in your browser.
2. Enter the customer's demographic and shopping details.
3. Select the membership type, preferred category, city tier, and discount usage.
4. Click the **Predict Spend** button.
5. View the predicted customer spending amount.

## Future Improvements

- Improve prediction accuracy through hyperparameter tuning.
- Add more customer behavioral features.
- Include additional data visualizations and insights.
- Deploy the Streamlit application online.
- Implement feature importance analysis to understand spending behavior.
