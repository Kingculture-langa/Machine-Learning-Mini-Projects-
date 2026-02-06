
## Project : Emphysema Risk Prediction Using Multiple Linear Regression
#### Case Study :
A recent 10-year study conducted by a research team at the Great Falls Medical School was conducted to assess how age, systolic blood pressure, and smoking relate to the risk of emphysema. Assume that the data in the file emphysema are from a portion of this study.
Risk is interpreted as the probability (times 100) that the patient will develop emphysema over the next 10-year period. 
Research Question:
What is the probability of developing emphysema over the next 10 years for: Art Speen, a 68-year-old smoker with a systolic blood pressure of 175 mmHg?


#### Overview
This project analyzes data from a 10-year medical study conducted by Great Falls Medical School to examine how age, systolic blood pressure, and smoking status relate to the risk of developing emphysema.
Risk is defined as the probability in percentagethat an individual will develop emphysema over the next 10 years.
A multiple linear regression model is developed to estimate emphysema risk and is then used to predict the risk for a specific individual.

Steps followed 
1. Install and load necessary packages
2. Load your data
3. Explore and Understand the data
4. Model selection 
5. Get a model summary
6. Make predictions
7. Plot and visualize your model
8. conclusion 

________________________________________
#  1.Install and load necessary packages
- Libraries, Python: pandas, numpy, scikit-learn, Matplotlib
- Version Control: GitHub
# 2.Load Data

# 3. Explore and Understand the data

- imported and inspected the emphysema dataset for completeness and consistency
- Encoded smoking status as a dummy variable (1 = smoker, 0 = nonsmoker)
- Visualized relationship between all variables
 Data Description
The dataset (emphysema) represents a subset of patients from the study and includes the following variables:
Variable	Description
- Risk:	Probability in percengate of developing emphysema over 10 years
- Age:	Age of the patient (years)
- Blood pressure : blood pressure
- Smoker: Smoking status (1 = smoker, 0 = nonsmoker)
  
# 4.Model Selection:
Supervide machine learning algorithm: A multiple linear regression model is used:
Risk = β_0+β_1 (Age)+β_2 (Boold presuure)+β_3 (Smoker)

- Where:
	- β_0is the intercept
	- β_1,β_2,β_3are regression coefficients
- Smoking status is represented using a dummy variable, where:
	- 1 = Smoker
	- 0 = Nonsmoker


# 5. Model summuary 
coefficients:
- B0 -77.2518 	Intercept
- B1 1.1623 	Coeffictent for Age
- B2 0.2546 	Coeffictent for Blood pressure
- B3 7.4650 	Coeffictent for For smoker

Model Evaluation:
- R-squared:					 	0.8035
- Adjusted R-squared:	 			0.7906
- Mean Absolute Error (MAE):		5.5295
- Root Mean Squared Error (RMSE): 6.5272

# 6.Prediction:
Once the regression coefficients are estimated, Art Speen’s risk is calculated by substituting his values into the regression equation:
"Predicted Risk"=β_0+β_1 (68)+β_2 (175)+β_3 (1)

# 7. Plot and visualize your model

<img width="944" height="966" alt="image" src="https://github.com/user-attachments/assets/759abf6f-d4a9-4731-90ec-fe82ad725bef" />


# 8 Conclution 
Interpretation of Model Evaluation Metrics
The multiple linear regression model demonstrates strong explanatory power and reasonable predictive accuracy, as indicated by the evaluation metrics.

- The R-squared value of 0.8035 indicates that approximately 80.35% of the variability in the 10-year emphysema risk is explained by the predictors included in the model: age, blood pressure, and smoking status. This suggests that the model fits the data well and that these variables are important determinants of emphysema risk.

- The Adjusted R-squared value of 0.7906 is only slightly lower than the R-squared value, indicating that the model does not include unnecessary predictors. This confirms that each variable contributes meaningful explanatory power and that the model is not overfitted.
  
- The Mean Absolute Error (MAE) of 5.53 indicates that, on average, the model’s predicted risk differs from the actual risk by about 5.5 percentage points. This suggests that most predictions are reasonably close to the observed values and that large prediction errors are uncommon.
  
- The Root Mean Squared Error (RMSE) of 6.53 represents the typical prediction error while placing greater weight on larger errors. The fact that RMSE is moderately higher than MAE suggests the presence of some larger prediction errors, but not to an extreme degree. Overall, this level of error is acceptable for a medical risk prediction model based on a limited number of predictors.

- ________________________________________
# Files in This Repository
- LinearRegressionModel.ipynb -Regression analysis and prediction code
- Risk of emphysema.csv – Dataset used for analysis
- riskOfemphysema.Cleand.csv-  file after data cleaning 
- README.md – Project documentation
________________________________________





