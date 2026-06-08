# Forest Fires Prevention Lab

## Project Overview

This project investigates the factors that influence forest fire severity using the Forest Fires dataset from the UCI Machine Learning Repository. The objective is to apply exploratory data analysis (EDA), regression modeling, and model diagnostics to understand how weather conditions and fire-related indices affect the burned area of forest fires.

The project was completed as part of a Data Science laboratory assessment focused on regression analysis and model evaluation.

---

## Dataset

Source: UCI Machine Learning Repository

Dataset: Forest Fires Dataset

Repository ID: 162

The dataset contains meteorological and fire-weather measurements collected from a forest region in Portugal.

### Key Variables

| Variable | Description             |
| -------- | ----------------------- |
| FFMC     | Fine Fuel Moisture Code |
| DMC      | Duff Moisture Code      |
| DC       | Drought Code            |
| ISI      | Initial Spread Index    |
| temp     | Temperature (°C)        |
| RH       | Relative Humidity (%)   |
| wind     | Wind Speed              |
| rain     | Rainfall                |
| area     | Burned Area (hectares)  |

---

## Objectives

* Load and inspect the Forest Fires dataset.
* Perform exploratory data analysis.
* Examine relationships between predictors and fire area.
* Build multiple linear regression models.
* Introduce nonlinear transformations.
* Create interaction effects between variables.
* Apply logarithmic transformations to address skewness.
* Evaluate and compare competing regression models.
* Conduct residual and influence diagnostics.

---

## Exploratory Data Analysis

The following analyses were performed:

* Dataset structure inspection
* Summary statistics
* Missing value assessment
* Correlation analysis
* Correlation heatmap visualization
* Distribution analysis of burned area
* Scatter plots between predictors and target
* Residual analysis

### Visualizations

* Correlation Heatmap
* Area Distribution Histogram
* Temperature vs Burned Area
* Relative Humidity vs Burned Area
* Residual Plot

---

## Regression Models

### Model 1: Baseline Linear Regression

Predictors:

* Temperature
* Relative Humidity
* Wind
* FFMC
* DMC
* DC
* ISI

Target:

* log(area + 1)

---

### Model 2: Nonlinear Regression

Additional features:

* Temperature²
* DMC²

Purpose:

* Capture nonlinear relationships between environmental conditions and fire size.

---

### Model 3: Interaction Regression

Interaction terms:

* Temperature × DMC
* Temperature × Relative Humidity
* Temperature × Wind
* DMC × ISI

Purpose:

* Examine combined effects of multiple environmental variables.

---

### Log Transformation

Because the burned area variable is highly skewed, a logarithmic transformation was applied:

log(area + 1)

This transformation improves model stability and reduces the influence of extreme observations.

---

## Model Evaluation

Models were compared using:

* R²
* Adjusted R²
* AIC
* BIC

Diagnostic analyses included:

* Residual plots
* Q-Q plots
* Cook's Distance

These diagnostics help evaluate model assumptions and identify influential observations.

---

## Key Findings

* Burned area exhibits strong positive skewness.
* Log transformation improves model performance.
* Interaction and nonlinear terms provide modest improvements over the baseline model.
* Environmental variables such as temperature, humidity, and drought indices contribute to explaining fire behavior, although the overall predictive power remains limited.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Seaborn
* Matplotlib
* Statsmodels
* UCI ML Repository API
* Jupyter Notebook

---

## Installation

Clone the repository:

```bash
git clone https://github.com/machariajoseph986-lgtm/Fire-Prevention-Lab-1.git
cd Fire-Prevention-Lab-1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

---

## Repository Structure

```text
Fire-Prevention-Lab-1/
│
├── forestfires.csv
├── Forest_Fires_Prevention.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Future Improvements

* Feature selection techniques
* Regularized regression (Ridge/Lasso)
* Random Forest Regression
* Gradient Boosting Models
* Cross-validation
* Hyperparameter optimization

---

## Author

Joseph Macharia

Data Science Student

GitHub:
https://github.com/machariajoseph986-lgtm
