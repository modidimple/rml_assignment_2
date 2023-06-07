## Q2 Calculate and Plot Local Feature Importance.

## Local Explainability

#### LIME and SHAP

* **LIME: Explains creating a surrogate (smaller, simpler)  model. Then approximates predictions**
   * The "effect" in LIME refers to the impact of each feature on the predicted outcome for the selected instance. Positive coefficients indicate that the feature has a positive effect on the prediction, while negative coefficients indicate a negative effect.
   * The "weight" in LIME refers to the importance of each feature in the overall explanation.
* **SHAP:** 
   * F(x) refers to the prediction of the machine learning model for a given data point x, while E[F(x)] refers to the expected prediction of the model over a background dataset. 
   * If F(x) and E[F(x)] are close to each other, it suggests that the model is making predictions that are consistent with the overall behavior of the dataset. 
   * If there is a large difference between F(x) and E[F(x)], it suggests that the model makes predictions that are significantly different from the overall behavior of the dataset, which may indicate bias or overfitting.
   * Positive values indicate that the feature contributes positively to the prediction, while negative values indicate that the feature contributes negatively. The size of the SHAP value indicates the magnitude of the feature's influence.
   
#### EBM
#### sample 30

* (pic of line shap 30 sample) 
* E[f(X)]= 0.082 represents the average predicted output over the background data .
* F(X) = 0.125 that predicts sample index for 30 .

* Shap: lone _to _value _ratio_std  has a SHAP value of 0.05 and contributes the most positive affect , followed by income         std , which has a SHAP value of -0.01 its means negative affect on mortgage high price .
* lime: lone _to _value _ratio_std  has a SHAP value of contributes the most positive affect , followed by property_value_std ,   which has a SHAP value of -0.12 its means negative affect on mortgage high price .
 
* (pic of local inpretaion )
 
* The title indicates that the predicted value for this sample is 0.1268, which differs slightly from the actual response of       1.0000.The main effect of lone _to _value _ratio_std makes the largest contribution to the final prediction, with a positive     effect (approximately0.95). Second number property_value contribution to the final prediction, with a positive effect           (approximately0.20) on mortgage high price

#### sample 8000

* (pic of lime and shap)

* E[f(X)]= 0.082 represents the average predicted output over the background data .
* F(X) = 0.005  that predicts sample index for 8000.

* shap:  lone _to _value _ratio_std  has a SHAP value of - 0.04 and contributes the most negative effect , followed by term 360   ,which has a SHAP value of -0.02 this  effect also negative  effect high-priced mortgage
* lime:  one _to _value _ratio_std  has a SHAP value of - 0.04 and contributes the most postive effect high-priced mortgage.

 
 * pic of local inpretaion)
 * The title indicates that the predicted value for this sample is 0.0052, which differs slightly from the actual response of       0.0000.The main effect of lone _to _value _ratio_std makes the largest contribution to the final prediction, with a Negative     effect (approximately – 0.05).  Second numberterm_360 contribution to the final prediction, with a negative  effect             (approximately- 1.2) on mortgage high price.
 
 #### sample 16000
 
 * (pic of lime and shap)
 * shap: lone _to _value _ratio_std  has a SHAP value of - 0.04 and contributes the most negative effect , followed by              Property_value_std ,which has a SHAP value of -0.02 this  effect also negative  effect on high-priced mortgage.
 * lime : debt_to_income_ratio_std has a SHAP value of - contributes the most postive  effect high-priced mortgage.
 
* (pic of local inpretaion)

* The title indicates that the predicted value for this sample is 0.0073, which differs slightly from the actual response of       0.0000.The main effect of lone _to _value _ratio_std makes the largest contribution to the final prediction, with a Negative     effect (approximately – 0.05).  Second number property_ value  contribution to the final prediction, with a negative  effect     (approximately-0.5) high-priced mortgage.

#### Reul DNN
#### sample 30


* (pic of line shap 30 sample) 
* SHAP: Loan to value ratio, property value, and loan amount are the most important features in predicting High Priced. They all   have a positive relationship with the target variable.
* LIME: Agrees with SHAP for Loan to value ratio, property value, and loan amount to be the most important features in             predicting High Priced.

* (pic of local inpretaion)
* Local Interpretability: Agrees with LIME that property value is the most important feature in predicting the target variable.

#### sample 8000
* (pic of line shap 8000 sample) 
* SHAP: Loan to value ratio, property value, and term 360 are the most important features in predicting High Priced. They all     have a negative relationship with the target variable.
  LIME: Agrees with SHAP for Loan to value ratio, property value, and term360 to be the most important features in predicting     High Priced. But has term360 as the most important.
  
* (pic of local inpretaion)
* Local Interpretability: Agrees with LIME that term360 is the most important feature in predicting the target variable.


#### sample 16000
* (pic of line shap 16000 sample) 
* SHAP: Loan to value ratio, property value, and loan amount are the most important features in predicting High Priced. Loan to   value ratio and property value have a positive relationship with the target variable. While loan amount has a negative           relationship with the High Priced.
* LIME: Agrees with SHAP for property value to be the most important feature in predicting High Priced, but followed by debt to   income ratio

* (pic of local inpretaion)
* Local Interpretability: ‘no intro rate period’ feature is the most important feature, followed by debt to income ratio.

#### XGB2
#### sample 30
* (pic of line shap 30 sample)
* LIME and SHAP agrees on the most influential feature to be  loan_to_value_ratio_std with a positive effect on                   high_priced_mortgage for sample point 30.

* (pic of local inpretaion)
* As shown in the model above ‘loan_to_value_ratio_std’ feature represent the standardized ‘loan-to value-ratio’, which is a       measure of the loan amount relative to the appraised value of the property.A higher loan-to-value ratio indicates a higher       risk for lenders,potentially leading to higher interest rates and hence the value of 0.5525 suggest that the loan to value       ratio for this particular application is relatively high.

#### sample 8000
* (pic of line shap 8000 sample)
* LIME and SHAP disagree on the most influential feature on ‘high_priced_mortgage’ for Sample point 8000. LIME suggests that       ‘loan_to_value_ratio_std’ is the most influential feature with a positive  effect on ‘high_priced_mortgage’, while SHAP          suggests that ‘property_value_std’ is the most influential with a negative effect on ‘high_priced_mortgage’.
* (pic of local inpretaion)
* Property value, loan-to-value ratio, and term_360, are directed towards the left side, indicating that decreasing or lower       values of these features for a specific instance have a relatively stronger influence on the prediction of a high-priced         mortgage.

#### sample 16000
* LIME and SHAP agree that ‘loan_to_value_ratio_std’  has the strongest influence on ‘high_priced_mortgage’ for sample point       16000. ‘Loan_to_value_ratio_std’has a negative effect on‘high_priced_mortgage’ as the value is -0.04 . LIME and SHAP disagree   on the rankings and effects of the other features on Status.
* (pic of local inpretaion)
* Property value, loan-to-value ratio, play pivotal role in predicting ‘high_priced_mortgage’ and are directed towards the left   side, indicating that decreasing or lower values of these features for a specific instance have a relatively stronger           influence on the prediction of a high-priced mortgage.

 








  
  
 













*










   


