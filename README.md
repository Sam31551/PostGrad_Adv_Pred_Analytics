# PostGrad_Adv_Pred_Analytics

This project demonstrates the use of various statistical models and techniques to analyze complex datasets, addressing issues like overdispersion, model comparison, and the handling of hierarchical data structures. 

Data Description
A dataset investigating the impact of education level and level of anxious attachment on unwanted pursuit behaviors in the context of couple separation.

Variables:

**1. UPB**
number of unwanted pursuit behavior perpetrations.

**2. EDUCATION**
1 if at least bachelor's degree; 0 otherwise.

**3. ANXIETY**
continuous measure of anxious attachment.

Each section is meticulously designed to teach the application of these methods, with the code providing practical examples of their implementation in R.


**Question 1**
Section A: A Poisson Generalized Linear Model is fit to analyze the relationship between UPB (response variable) and predictors EDUCATION and ANXIETY.
  -> Results: Both variables were found to be significant. Education to a sig. level of 0.01 and Anxiety to a sig. level of 0.001. 
              Coefficient Estimates show that those with a bachelor’s degree are less likely to have high UPB.
              Those with Anxiety are more likely to have high UPB.

Section B: Overdispersion test. The data is checked for overdispersion test as this violates the Poisson model's assumptions.
  -> Results: Data was found to be overdispersed. Due to overdispersion, a Zero-Inflated Poisson (ZIP) model or a Negative Binomial model would be more appropriate.

Section C: The negative binomial regression model is fit in a bid to tackle data overdispersion.
  -> Results: ANXIETY remains significant, but EDUCATION becomes non-significant.

Section D: To compare the predictive performance of Poisson and Negative Binomial models using Cross Validation and Mean Squared Error (MSPE).
  -> Results: Both models have similar performance, but the Poisson model shows a slightly lower average MSPE across iterations, making it the preferred model.

  **Question 2**
  To analyze the effect of school on math scores using both a normal linear regression and a mixed-effects model.

  -> Results: When using a normal linear regression model, school is not a significant covariate when it comes to predicting math scores.
              A fixed effects model to isolate the impact of school explain the variance in math scores. School becomes a significant variable. 
              0.18 is total variance in outcome that can be attributed to differences between schools (found using Intraclass coefficients). 

  **Question 3**
  To model a non-linear relationship using kernel smoothing and smoothing splines. 
 
  Data is generated for analysis. Kernel Smoothing splines are fit using different bandwith values (One found using CV, one large and one small).
  The 3 bandwiths are graphed with the one found using cross validation shown to be the optimum fit to the data.

  **Question 4**
  Regression splines with differing degrees of data are fit to the data. 

  The optimum splines are found to be the smoothing spline and the Cross-Validated bandwith.

  
