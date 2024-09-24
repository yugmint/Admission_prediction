---

# Graduate Admission Prediction

## Project Overview
This repository contains an analysis aimed at predicting the likelihood of graduate admission to Ivy League colleges for Indian students. By examining key factors that influence admission decisions, we aim to provide insights that enhance Jamboree's new feature that estimates a student's chances of admission.

## Business Problem
Jamboree has launched a feature that allows students to check their probability of gaining admission to top colleges abroad. Understanding the factors that impact graduate admissions is crucial for refining this feature and offering tailored guidance to prospective students.

## Dataset
**Dataset Link:** [jamboree_admission.csv](jamboree_admission.csv)

### Column Profiling:
- **Serial No.**: Unique row ID
- **GRE Scores**: Score out of 340
- **TOEFL Scores**: Score out of 120
- **University Rating**: Rating out of 5
- **SOP & LOR Strength**: Strength rating out of 5
- **Undergraduate GPA**: GPA out of 10
- **Research Experience**: Binary (0 or 1)
- **Chance of Admit**: Probability ranging from 0 to 1

## Analysis Steps

### 1. Data Import and Exploration
- Import the dataset and explore its structure and characteristics.
- Identify and drop any unique identifiers to prevent bias in the model.
- Conduct both graphical and non-graphical analyses to examine the distribution of variables and relationships.

### 2. Data Preprocessing
- Check for and treat duplicate values, missing values, and outliers.
- Engineer relevant features for improved modeling.

### 3. Model Development
- Build a Linear Regression model using the `Statsmodel` library.
- Test assumptions of linear regression including:
  - Multicollinearity (using VIF score)
  - Mean of residuals
  - Linearity of variables
  - Homoscedasticity
  - Normality of residuals

### 4. Performance Evaluation
- Evaluate model performance using metrics such as MAE, RMSE, R², and Adjusted R².
- Experiment with Ridge and Lasso regression to explore improvements.

### 5. Insights and Recommendations
- Identify key predictors influencing the chance of admission and provide actionable recommendations for enhancing predictive accuracy.

## Key Findings
- The target variable (chance of admit) is left-skewed, indicating that most students have lower probabilities of admission.
- Strong positive correlations exist among exam scores (GRE, TOEFL, GPA) and with the chance of admit.
- Categorical variables such as university ranking, research experience, and the quality of SOP and LOR also contribute positively to admission chances.
- Both Linear and Ridge Regression models explain up to **82%** of the variance in the target variable.
- Metrics for model evaluation include:
  - **Mean Absolute Error (MAE)**: [insert value]
  - **Root Mean Squared Error (RMSE)**: [insert value]
  - **R² Score**: [insert value]
  - **Adjusted R² Score**: [insert value]
- High multicollinearity among predictors limits improvement potential.

## Recommendations
- To enhance prediction accuracy, consider incorporating additional features such as work experience, internships, mock interview performance, extracurricular activities, and diversity factors.
- Regularly update the model with new data to adapt to changing trends in admissions criteria.

## How to Use This Repository
### Clone the Repository
```bash
git clone https://github.com/yourusername/jamboree-admission-prediction.git
```

### Install Required Libraries
Ensure you have Python and the necessary libraries installed. Use the following command to install required packages:
```bash
pip install -r requirements.txt
```

### Run the Analysis
Open the Jupyter notebooks provided in the repository to explore the data and perform the analysis step-by-step.

## Contributions
Contributions to this project are welcome. Feel free to fork the repository, make improvements, and submit pull requests. For major changes, please open an issue first to discuss your proposals.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

Feel free to fill in the specific metric values once you have them!
