
# 🚗 Car Price Prediction

A Machine Learning project focused on predicting the selling prices of used cars using Python and regression algorithms.

The project follows a complete Machine Learning workflow, including data exploration, preprocessing, feature engineering, model training, hyperparameter tuning, and model evaluation.

## 🎯 Problem

Estimating the selling price of a used car can be challenging because several factors influence its market value, including manufacturing year, current market price, mileage, fuel type, seller type, and transmission.

The goal of this project is to develop and compare regression models that can predict used car selling prices based on these features.

## 📊 Dataset Description

The project uses a dataset named `cardata.csv`, containing 301 records and 9 initial features.

### Dataset Features

| Feature | Description |
|---|---|
| Car_Name | Name of the car model |
| Year | Year of manufacture |
| Selling_Price | Target variable (selling price) |
| Present_Price | Current ex-showroom price |
| Kms_Driven | Total kilometers driven |
| Fuel_Type | Type of fuel (Petrol, Diesel, CNG) |
| Seller_Type | Dealer or Individual |
| Transmission | Manual or Automatic |
| Owner | Number of previous owners |

## ✨ Project Features

- **Data Loading & Exploration:** Load the dataset and examine its structure and statistical properties.
- **Data Cleaning:** Identify missing values and remove duplicate records.
- **Outlier Detection:** Use the Interquartile Range (IQR) method to identify and filter outliers.
- **Feature Engineering:** Create a new feature called `Age` based on the manufacturing year.
- **Exploratory Data Analysis (EDA):** Analyze feature distributions and relationships using statistical visualizations.
- **Categorical Encoding:** Apply One-Hot Encoding to categorical variables.
- **Feature Scaling:** Apply MinMaxScaler and StandardScaler in the regression pipelines.
- **Model Training:** Train multiple regression models.
- **Hyperparameter Tuning:** Optimize Ridge Regression using GridSearchCV.
- **Cross-Validation:** Evaluate models using 5-fold and 10-fold cross-validation.
- **Model Comparison:** Compare model performance using regression evaluation metrics.

## 🛠️ Technologies & Libraries

- **Python:** Main programming language.
- **Pandas:** Data manipulation and analysis.
- **NumPy:** Numerical computations.
- **Matplotlib:** Data visualization.
- **Seaborn:** Statistical data visualization.
- **Scikit-learn:** Machine Learning models, preprocessing, cross-validation, and evaluation.
- **Jupyter Notebook:** Interactive development environment.
- **Git & GitHub:** Version control and project management.

## 🤖 Machine Learning Models

Three regression approaches were implemented and compared.

### 1. Linear Regression

A baseline Ordinary Least Squares (OLS) regression model was implemented using:

- MinMaxScaler
- LinearRegression
- 10-Fold Cross-Validation

### 2. Ridge Regression

Ridge Regression was implemented using L2 regularization to improve model generalization.

Hyperparameter tuning was performed using GridSearchCV with:

- Alpha values ranging from 0 to 0.95.
- Different solver options.
- 5-Fold Cross-Validation.

The best parameters obtained were:

- **Alpha:** 0.95
- **Solver:** auto

The selected model was further evaluated using 10-Fold Cross-Validation.

### 3. Polynomial Regression

Polynomial Regression was implemented to capture nonlinear relationships between features and car prices.

The following polynomial degrees were evaluated:

- Degree 1
- Degree 2
- Degree 3

Ridge Regression was used as the final estimator.

The best-performing configuration was Polynomial Regression with Degree 2.

## 📈 Model Evaluation

The models were evaluated using the following metrics:

- **MSE (Mean Squared Error):** Measures the average squared prediction error.
- **RMSE (Root Mean Squared Error):** Measures the prediction error in the same unit as the target variable.
- **R² Score:** Measures how well the model explains the variance in the target variable.

### Test Set Results

| Model | MSE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 1.3903 | 1.1791 | 0.8828 |
| Ridge Regression | 1.4040 | 1.1849 | 0.8817 |
| Polynomial Regression (Degree 2) | 0.4567 | 0.6758 | 0.9615 |

### Cross-Validation Results

| Model | Cross-Validation R² |
|---|---:|
| Linear Regression | 0.8494 |
| Ridge Regression | 0.8503 |
| Polynomial Regression (Degree 2) | 0.9389 |

### Best Model

Polynomial Regression with Degree 2 achieved the best performance among the evaluated models, with:

- **R² Score:** 0.9615
- **RMSE:** 0.6758
- **MSE:** 0.4567

These results indicate that the polynomial model captured nonlinear relationships in the dataset more effectively than the other evaluated models.

*Note: Results are based on the current notebook implementation and should be re-evaluated after improving the preprocessing workflow.*

## 📸 Visualizations

The project includes several visualizations to better understand the dataset and evaluate model performance.

### 1. Exploratory Data Analysis

- Categorical feature distributions.
- Correlation heatmap.
- Relationships between numerical features and selling prices.
- Boxplots for outlier detection.

### 2. Model Prediction Comparison

Actual vs. predicted selling prices are visualized for:

- Linear Regression
- Ridge Regression
- Polynomial Regression

<!-- Add your screenshots and visualization images here -->

## ⚙️ Installation & Usage

### 1. Clone the Repository

```bash
git clone [YOUR_REPOSITORY_URL]
```

### 2. Navigate to the Project Directory

```bash
cd [PROJECT_DIRECTORY]
```

### 3. Install Dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### 4. Run Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the Notebook

Open `CarPrice (3).ipynb` in Jupyter Notebook.

Make sure `cardata.csv` is located in the same directory as the notebook.

Run the notebook cells sequentially to reproduce the analysis and model results.

## 📖 What I Learned

Through developing this project, I gained practical experience in:

- Working with real-world datasets using Pandas and NumPy.
- Performing Exploratory Data Analysis (EDA).
- Identifying and handling duplicate records and outliers.
- Applying Feature Engineering techniques.
- Encoding categorical variables.
- Understanding the importance of feature scaling.
- Implementing Linear Regression and Ridge Regression.
- Applying Polynomial Features to capture nonlinear relationships.
- Performing hyperparameter tuning with GridSearchCV.
- Evaluating models using MSE, RMSE, and R².
- Applying cross-validation to assess model performance.
- Comparing multiple regression algorithms.
- Visualizing actual and predicted values.

## 🚀 Future Improvements

- Building a preprocessing pipeline using ColumnTransformer and Pipeline.
- Improving data preprocessing to prevent data leakage.
- Comparing additional regression algorithms such as Random Forest and Gradient Boosting.
- Performing more extensive hyperparameter optimization.
- Applying more robust cross-validation strategies.
- Developing an interactive web application for car price prediction.
- Improving model interpretability using feature importance and explainability techniques.

## 👩‍💻 Author

**Pardis Aghamohammadrafi**

---
