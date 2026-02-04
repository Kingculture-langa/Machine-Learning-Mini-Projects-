#### Case Study :
A recent 10-year study conducted by a research team at the Great Falls Medical School was conducted to assess how age, systolic blood pressure, and smoking relate to the risk of emphysema. Assume that the data in the file emphysema are from a portion of this study.
Risk is interpreted as the probability (times 100) that the patient will develop emphysema over the next 10-year period. 


# Emphysema Risk Prediction Using Multiple Linear Regression
# Overview
This project analyzes data from a 10-year medical study conducted by Great Falls Medical School to examine how age, systolic blood pressure, and smoking status relate to the risk of developing emphysema.
Risk is defined as the probability in percentagethat an individual will develop emphysema over the next 10 years.
A multiple linear regression model is developed to estimate emphysema risk and is then used to predict the risk for a specific individual.
________________________________________
# Tools & Methods
## Tools
- Libraries, Python: pandas, numpy, scikit-learn, Matplotlib
- Version Control: GitHub
## Methods
# Data inspection, Preparation and Visualization
mported and inspected the emphysema dataset for completeness and consistency
Encoded smoking status as a dummy variable (1 = smoker, 0 = nonsmoker)
Visualized relationship between all variables
# Modeling Approach:
Applied multiple linear regression to model 10-year emphysema risk as a function of age, systolic blood pressure, and smoking status
Estimated regression coefficients using the least squares method
  # Prediction:
Used the estimated regression equation to predict emphysema risk for a specific individual (Art Speen)
Interpreted results within the context of model accuracy and uncertainty
Model Evaluation:
Assessed model fit using R-squared and Adjusted R-squared
Evaluated predictive accuracy using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE)
# Data Description
The dataset (emphysema) represents a subset of patients from the study and includes the following variables:
## Variable	Description
- Risk:	Probability in percengate of developing emphysema over 10 years
- Age:	Age of the patient (years)
- Blood pressure : blood pressure
- Smoker: Smoking status (1 = smoker, 0 = nonsmoker)
________________________________________
# Model Specification
A multiple linear regression model is used:
"Risk"=β_0+β_1 ("Age")+β_2 ("Boold presuure")+β_3 ("Smoker")+ε

Where:
	β_0is the intercept
	β_1,β_2,β_3are regression coefficients
	εis the error term
Smoking status is represented using a dummy variable, where:
	1 = Smoker
	0 = Nonsmoker
________________________________________
# Research Question
What is the probability of developing emphysema over the next 10 years for:
Art Speen, a 68-year-old smoker with a systolic blood pressure of 175 mmHg?
________________________________________
# Prediction Method
Once the regression coefficients are estimated, Art Speen’s risk is calculated by substituting his values into the regression equation:
"Predicted Risk"=β_0+β_1 (68)+β_2 (175)+β_3 (1)

This result represents the predicted probability in percentage that Art Speen will develop emphysema within the next 10 years is 53.81%
________________________________________
# Files in This Repository
LinearRegressionModel.ipynb -Regression analysis and prediction code
Risk of emphysema.csv – Dataset used for analysis
riskOfemphysema.Cleand.csv-  file after data cleaning 
README.md – Project documentation
________________________________________

# Results
Age, blood pressure, and smoking status are important predictors of emphysema risk.
Smoking status is incorporated using a binary (dummy) variable.
The regression model allows individualized risk prediction over a 


# Interpretation of Model Evaluation Metrics
The multiple linear regression model demonstrates strong explanatory power and reasonable predictive accuracy, as indicated by the evaluation metrics.

The R-squared value of 0.8035 indicates that approximately 80.35% of the variability in the 10-year emphysema risk is explained by the predictors included in the model: age, systolic blood pressure, and smoking status. This suggests that the model fits the data well and that these variables are important determinants of emphysema risk.
The Adjusted R-squared value of 0.7906 is only slightly lower than the R-squared value, indicating that the model does not include unnecessary predictors. This confirms that each variable contributes meaningful explanatory power and that the model is not overfitted.
The Mean Absolute Error (MAE) of 5.53 indicates that, on average, the model’s predicted risk differs from the actual risk by about 5.5 percentage points. This suggests that most predictions are reasonably close to the observed values and that large prediction errors are uncommon.
The Root Mean Squared Error (RMSE) of 6.53 represents the typical prediction error while placing greater weight on larger errors. The fact that RMSE is moderately higher than MAE suggests the presence of some larger prediction errors, but not to an extreme degree. Overall, this level of error is acceptable for a medical risk prediction model based on a limited number of predictors.
Overall Assessment
Taken together, these results indicate that the regression model provides a strong fit to the data and reliable risk estimates. While individual predictions may deviate by several percentage points, the model effectively captures the major factors influencing emphysema risk and is suitable for predicting 10-year risk at the population and individual level.



