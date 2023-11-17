# R-Program
 Research Methods:
A multiple regression model


Objective: Predict the stress rating based on physiological measurements.


Dataset Description:

The study uses numerical variables to measure various aspects of human health, including stress ratings, respiratory rates, temperature, locomotor movements, blood oxygenation levels, rapid eye movement, stress hormone levels, and heart rates.
These variables represent measurements for each of the 630 observations, with values within each variable representing measurements for each of these variables. 


The Shapiro-Wilk normality test was employed to assess whether the residuals followed a normal distribution.

Shapiro-Wilk normality test

data:  resid(transformed_model)
W = 0.98085, p-value = 2.444e-07


The Shapiro-Wilk test results demonstrate a divergence from normalcy in residuals, indicating that the assumption of normality has been violated. 
This implies that the residuals do not have a completely normal distribution. However, violations may not necessarily invalidate the results of a multiple regression analysis, particularly with higher sample sizes, because the apparent non-normality may be impacted by the nature of the data or sample characteristics.





Multiple Regression Analysis of Stress Levels
To assess the variables affecting stress levels, we performed a multivariate regression analysis using physiological data as predictors. 
The dependent variable, the natural logarithm of stress ratings (log(sr)), was employed to address non-normality in the distribution of stress ratings.

With an adjusted R2 of 0.9698, the regression model demonstrated a high degree of statistical significance, meaning that the predictor variables together explained a noteworthy percentage of the variance in stress levels or 96.98% of the variability in transformed stress ratings.

Stress levels were found to be significantly influenced by both rapid eye movement (rem) and stress hormone levels (sh). 
Reduction in sh and increase in rem were correlated with higher stress ratings. The residuals' symmetric distribution and standard error of 0.0482 suggested that there was not much variability that the model could not have captured.  
The research emphasizes the significance of these indicators in predicting stress levels.




Exploring Interaction Effects on Stress Levels


To analyze factors influencing stress levels, the researchers used an interaction term in a multiple regression model.
The dependent variable, the natural logarithm of stress ratings, was employed to address non-normality in the distribution of stress ratings.
The regression model with the interaction term was highly significant, showing that predictors had strong explanatory power.
The updated R2 value of 0.9729 considerably improved the model fit.

Interaction Effect:
The study established the term (rem_sh_interaction) to describe the interaction between rapid eye movement (rem) and stress hormone levels (sh). Because of the combined influence, the negative coefficient suggests a drop in stress ratings.
The model was found to be well-fitted, as evidenced by the symmetric distribution of the residuals. The residual standard error of 0.04568 suggested that the variability in stress ratings was not too great.

According to the study's findings, stress levels are accurately predicted by physiological markers. Although the normalcy assumptions were violated, a thorough analysis supported the findings. 
It was discovered that fast eye movement and stress hormone levels were significant markers. Multiple regression models successfully captured the relationships between physiological indicators and stress assessments. 
The study underscores the importance of taking interactions and transformations into account in order to increase forecast accuracy.  
For a more sophisticated knowledge of stress prediction, future studies should investigate other variables or develop modeling methodologies.


A logistic regression model

Objective: Predict the 'Outcome' variable, indicating the presence or absence of diabetes, using logistic regression on the 'diabetes' dataset.

The study uses ratio scales to measure various factors such as pregnancies, glucose, blood pressure, skin thickness, insulin, BMI, diabetes pedigree function, and age. 
The outcome is a binary variable indicating the presence or absence of diabetes, with the number of pregnancies being the most significant independent variable.

onfusion Matrix and Statistics
          Reference
Prediction   0   1
         0 130  33
         1  20  47
                                          
               Accuracy : 0.7696          
                 95% CI : (0.7097, 0.8224)
    No Information Rate : 0.6522          
    P-Value [Acc > NIR] : 7.748e-05       
                                          
                  Kappa : 0.4721          
                                          
 Mcnemar's Test P-Value : 0.09929         
                                          
            Sensitivity : 0.8667          
            Specificity : 0.5875          
         Pos Pred Value : 0.7975          
         Neg Pred Value : 0.7015          
             Prevalence : 0.6522          
         Detection Rate : 0.5652          
   Detection Prevalence : 0.7087          
      Balanced Accuracy : 0.7271          
 The logistic regression model predicts diabetes presence or absence using a dataset, with the confusion matrix revealing the following breakdown.                                         
             
                                      	            Reference
Prediction 	  0   	 1
        	 0	 130 	 33
        	 1  	  20  	 47

The model accurately predicted diabetes outcomes in 77% of cases, with a 95% confidence interval of 71% to 82%. The model's no information rate, which represents accuracy by always predicting the majority class, is 65%, highlighting its performance beyond a baseline prediction strategy. The 95% confidence interval for accuracy is 0.7097 to 0.8224.
At 0.4556, the Kappa value, which measures agreement above and beyond chance, suggests moderate agreement between the model's predictions and random chance.

The accuracy of the model is remarkable at 76.96% with a small 95% confidence interval, showing strong prediction ability. Its high sensitivity (90%) and modest specificity (52.5%) indicate that there is still room for improvement in detecting real negatives.
Exploration of false positive and negative characteristics, refinement of the model through parameter optimization or alternative techniques, and external validation on an independent dataset to assess generalizability




References:

Stults-Kolehmainen MA, Sinha R. The effects of stress on physical activity and exercise. Sports Med. 2014 Jan;44(1):81-121. doi: 10.1007/s40279-013-0090-5. PMID: 24030837; PMCID: PMC3894304.
Joshi RD, Dhakal CK. Predicting Type 2 Diabetes Using Logistic Regression and Machine Learning Approaches. Int J Environ Res Public Health. 2021 Jul 9;18(14):7346. doi: 10.3390/ijerph18147346. PMID: 34299797; PMCID: PMC8306487.
 Bays H.E., Chapman R., Grandy S., Group S.I. The relationship of body mass index to diabetes mellitus, hypertension and dyslipidaemia: Comparison of data from two national surveys. Int. J. Clin. Pract. 2007;61:737–747. doi: 10.1111/j.1742-1241.2007.01336.x. 
Jackson EM. Stress relief: the role of exercise in stress management. ACSMS Health Fit J. 2013;17(3):14–9.



