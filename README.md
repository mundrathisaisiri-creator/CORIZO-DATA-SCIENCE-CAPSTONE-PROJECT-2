# 🏭 Capstone Project 2: Semiconductor Manufacturing Yield Prediction

## 📌 Project Overview

This project focuses on predicting the **Pass/Fail yield of semiconductor manufacturing process entities** using machine learning.

Modern semiconductor manufacturing processes generate a large number of sensor and process measurement signals. However, many of these signals may contain irrelevant information or noise. Therefore, **feature selection and dimensionality reduction** are important for identifying the signals that contribute most significantly to manufacturing yield.

The objective of this project is to build and compare multiple supervised machine learning models and determine whether all available features are required for accurate yield prediction.

---

## 🎯 Project Objective

The main objectives are to:

- Explore the semiconductor manufacturing dataset.
- Clean and preprocess the data.
- Handle missing values and irrelevant attributes.
- Perform statistical analysis and data visualization.
- Analyze univariate, bivariate, and multivariate relationships.
- Separate predictor variables and the target variable.
- Check and handle target-class imbalance.
- Standardize the features where required.
- Apply feature selection/dimensionality reduction techniques.
- Train multiple machine learning classification models.
- Perform cross-validation.
- Optimize model hyperparameters using GridSearchCV.
- Compare model performance using train and test accuracy.
- Analyze classification reports.
- Select the best-performing model.
- Save the final trained model for future use.

These objectives follow the supplied Capstone Project 2 requirements.

---

## 📊 Dataset

The project uses the **Semiconductor Manufacturing Sensor Dataset**.

### Dataset Characteristics

| Property | Description |
|---|---|
| Domain | Semiconductor Manufacturing |
| Records | 1,567 |
| Features | 591 |
| Total columns | 592 |
| Target | Pass/Fail Yield |
| Data type | Sensor and process measurements |

Each row represents a single production entity with associated measured process features.

The target variable represents the yield outcome:

- **-1 → Pass**
- **1 → Fail**

The dataset also contains a timestamp corresponding to the specific test point.

---

## 🔄 Project Workflow

```text
Raw Sensor Data
       ↓
Data Exploration
       ↓
Data Cleaning
       ↓
Missing Value Treatment
       ↓
Statistical Analysis
       ↓
Data Visualization
       ↓
Feature & Target Separation
       ↓
Target Balance Analysis
       ↓
Feature Selection / Dimensionality Reduction
       ↓
Train-Test Split
       ↓
Feature Standardization
       ↓
Model Training
       ↓
Cross Validation
       ↓
GridSearch Hyperparameter Tuning
       ↓
Model Comparison
       ↓
Best Model Selection
       ↓
Model Saving
       ↓
Final Conclusion
```

---

# 🧹 1. Data Cleaning

The dataset is examined for:

- Missing values
- Irrelevant attributes
- Unnecessary columns
- Data inconsistencies
- Features requiring transformation

Missing values are treated using appropriate techniques based on the characteristics of the individual variables.

Functional and logical reasoning is used when deciding whether attributes should be retained or removed.

---

# 📈 2. Exploratory Data Analysis

Detailed exploratory analysis is performed to understand the structure and characteristics of the sensor data.

### Analysis Includes

- Univariate analysis
- Bivariate analysis
- Multivariate analysis
- Statistical summaries
- Distribution analysis
- Feature relationships
- Target-class distribution

Visualizations are used to identify patterns, outliers, correlations, and potential issues within the dataset.

The project requirements specifically call for detailed univariate, bivariate, and multivariate analysis with interpretations after each analysis.

---

# ⚙️ 3. Data Preprocessing

The following preprocessing steps are performed:

### Predictor and Target Separation

The dataset is divided into:

```text
X → Predictor Features
y → Target Variable
```

### Target Balance

The Pass/Fail distribution is analyzed to identify class imbalance.

If imbalance is present, appropriate balancing techniques such as **SMOTE** can be applied.

### Train-Test Split

The dataset is divided into training and testing subsets to evaluate how well the models generalize to unseen data.

### Standardization

Feature standardization is performed where required to bring variables to a comparable scale.

The project also requires checking whether the train and test datasets retain similar statistical characteristics compared with the original data.

---

# 🔍 4. Feature Selection

Since the dataset contains **591 features**, using every available feature may not be necessary.

Feature selection and/or dimensionality reduction techniques are investigated to identify the most relevant process signals.

The objective is to determine:

> **Are all 591 features necessary for predicting semiconductor manufacturing yield?**

Reducing irrelevant or noisy features can potentially:

- Improve model performance
- Reduce computational complexity
- Reduce overfitting
- Improve interpretability
- Identify important manufacturing signals

The project specification specifically highlights feature selection as a way to identify signals relevant to yield excursions.

---

# 🤖 5. Machine Learning Models

Multiple supervised classification algorithms are trained and evaluated.

Potential models include:

- Random Forest
- Support Vector Machine (SVM)
- Naive Bayes
- Other suitable classification algorithms

At least **three different machine learning models** are evaluated as required by the project specification.

---

# 🔧 6. Model Optimization

To improve model performance, the following techniques are applied:

### Cross-Validation

Cross-validation is used to obtain a more reliable estimate of model performance.

### GridSearchCV

GridSearchCV is used to search through different combinations of hyperparameters and identify the configuration that provides the best performance.

### Additional Optimization

Depending on the model and dataset characteristics, performance can be improved through:

- Feature selection
- Dimensionality reduction
- Standardization
- Normalization
- Target balancing
- Attribute removal

These optimization approaches are specifically suggested in the project requirements.

---

# 📊 7. Model Evaluation

The trained models are evaluated using:

- Training Accuracy
- Testing Accuracy
- Classification Report
- Precision
- Recall
- F1-Score
- Cross-validation performance

The classification report is analyzed to understand how effectively the models distinguish between:

```text
PASS (-1)
FAIL (1)
```

The performance of all developed models is compared before selecting the final model.

---

# 🏆 8. Best Model Selection

The final model is selected based on its overall performance on unseen test data and other relevant evaluation metrics.

The selection considers:

- Test accuracy
- Generalization capability
- Precision
- Recall
- F1-score
- Cross-validation performance
- Model complexity

The selected model is saved for future use as required by the project specification.

---

# 📌 Key Questions Addressed

This project aims to answer the following questions:

1. Can semiconductor manufacturing yield be accurately predicted using sensor data?
2. Are all 591 available features required?
3. Which features contribute most to yield prediction?
4. Does feature selection improve model performance?
5. Which machine learning algorithm performs best?
6. How does class imbalance affect prediction?
7. Can hyperparameter tuning improve the selected models?
8. Which model provides the best balance between performance and complexity?

---

# 📁 Project Structure

```text
Capstone-Project-2/
│
├── capstone2project.ipynb
├── signal-data.csv
├── README.md
└── saved_model/
    └── best_model.pkl
```

---

# 🛠️ Technologies Used

- **Python**
- **NumPy**
- **Pandas**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **Jupyter Notebook**
- **Imbalanced-learn / SMOTE**

---

# ▶️ How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the project

```bash
cd Capstone-Project-2
```

### 3. Install dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the notebook

```text
capstone2project.ipynb
```

Run the cells sequentially to reproduce the analysis and model-building process.

---

# 📋 Project Requirements Covered

| Task | Status |
|---|---|
| Import and explore data | ✅ |
| Missing value treatment | ✅ |
| Attribute removal | ✅ |
| Statistical analysis | ✅ |
| Univariate analysis | ✅ |
| Bivariate analysis | ✅ |
| Multivariate analysis | ✅ |
| Predictor-target separation | ✅ |
| Target balancing | ✅ |
| Train-test split | ✅ |
| Standardization | ✅ |
| Feature selection | ✅ |
| Multiple ML models | ✅ |
| Cross-validation | ✅ |
| GridSearch hyperparameter tuning | ✅ |
| Classification report | ✅ |
| Model comparison | ✅ |
| Best model selection | ✅ |
| Model saving | ✅ |
| Conclusion and improvement | ✅ |

---

# 💡 Conclusion

This project demonstrates the complete machine learning workflow for a **semiconductor manufacturing yield prediction problem**.

By combining data preprocessing, exploratory analysis, feature selection, class balancing, model training, cross-validation, and hyperparameter optimization, the project investigates how sensor/process signals can be used to predict manufacturing yield.

A major focus of the project is determining whether the complete set of **591 process features** is necessary or whether a smaller set of relevant features can provide comparable or improved predictive performance.

---

## 👨‍💻 Author

**Siri**

Data Science & Machine Learning Student

### Skills Demonstrated

`Python` `Machine Learning` `Data Analysis` `Feature Selection` `Classification` `EDA` `Scikit-learn` `Pandas` `NumPy` `Model Optimization`

---

### ⭐ Project Highlights

> **Machine learning-based semiconductor manufacturing yield prediction using sensor data, feature selection, class balancing, cross-validation, and hyperparameter optimization.**
