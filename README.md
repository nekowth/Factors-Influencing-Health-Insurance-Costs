# Factors-Influencing-Health-Insurance-Costs
Factors Influencing Health Insurance Costs – R-based Statistical Modeling
Project Summary
This project analyzes a real-world health insurance dataset to understand how demographic and lifestyle factors (such as age, BMI, sex, region, and smoking status) influence individual medical expenses. Using R for data cleaning, visualization, and inferential statistics, we applied multiple linear regression models and statistical tests (ANOVA, t-tests, Shapiro-Wilk) to identify significant predictors and validate model assumptions. We also introduced interaction terms to capture compounded effects (e.g., smoker × BMI) and improved model accuracy to R² = 0.8678.

Research Question
How do age, sex, BMI, number of children, smoking status, and region affect individual medical charges?

Hypotheses
H₀: None of the variables significantly affect medical costs.

H₁: At least one variable significantly influences healthcare costs.

Dataset Summary
Source: Kaggle Medical Cost Personal Datasets

Size: 1,338 records × 7 features

Key Features:

age, sex, bmi, children, smoker, region, charges

Tools Used
Language: R

Libraries: dplyr, ggplot2, stats, car, multcomp, MASS, shapiro.test, lm, anova, TukeyHSD

Visualization: Boxplots, scatter plots, heatmaps, correlation matrices

Methodology
🔹 Data Cleaning & Exploration
Checked for missing values and outliers

Converted categorical variables into numeric (e.g., smoker, region)

Identified key trends via univariate and bivariate visualizations

🔹 Statistical Testing
Shapiro-Wilk Normality Test: To assess residual normality

T-Tests: Compared charges by smoker/non-smoker and gender

ANOVA + Tukey HSD: Compared regional differences in charges for smokers

🔹 Modeling
Multiple Linear Regression:

Identified significant predictors: age, BMI, smoking status

Adjusted for multicollinearity using VIF

Improved Model:

Included interaction terms (e.g., smoker * BMI)

Achieved adjusted R² = 0.8678

Key Findings
Factor	Impact on Charges
Smoking	Most significant; adds ~$23,000 to charges
BMI	Charges increase linearly when BMI > 30 (obese)
Age	Positive correlation (~$263 per year increase)
Region	Significant only for smokers (Southeast > Northeast)
Children	Minor but significant contributor
Gender	Males slightly higher charges than females (p = 0.029)

Smokers with BMI > 30 had the highest medical costs.

Interaction terms revealed compounded effects that linear terms alone missed.

Model residuals satisfied assumptions of normality and homoscedasticity.

Folder Structure
kotlin
Copy
Edit
Health_Insurance_Cost_Modeling/
├── data/
│   └── insurance.csv
├── scripts/
│   └── final.Rmd
├── report/
│   ├── Project Report.docx
│   ├── Applied Stats Presentation.pptx
│   └── README.md
└── outputs/
    ├── interaction_model_summary.png
    ├── residual_plots.png
    └── correlation_matrix.png
Conclusion
This project confirms that smoking, obesity (BMI > 30), and age are critical drivers of increased medical costs. The improved model, using interaction terms, strengthens our understanding of how these factors jointly influence expenses—offering insights valuable to insurance providers and public health strategists.

Team
Name	Contribution
Neha Kowtharapu	Residual diagnostics, presentation
Nilaya Ramireddy	Exploratory analysis, regression model
Rupasri Pamulapati	ANOVA + post-hoc testing, R coding
Sapna Vibhaker	Data cleaning, interaction term modeling
Srija Dammannagari	T-tests, normality checks, documentation

References
Dieleman, J. L., et al. (2017). Factors associated with increases in US health care spending, 1996-2013. JAMA, 318(17), 1668. https://doi.org/10.1001/jama.2017.15927

Kaggle. Medical Cost Personal Datasets. https://www.kaggle.com/datasets/mirichoi0218/insurance

Contact
For questions or suggestions, contact:
Neha Kowtharapu - nehakowtharapu@gmail.com
