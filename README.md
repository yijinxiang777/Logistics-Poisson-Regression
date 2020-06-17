# Logistics-Poisson-Regression
## Logiistics Regression   
### Likelihood Ratio Test(LRT) : follows a chi-sqaure distribution (df = number of parameters different between two models)  
### Wald Test: foloows a chi-sqaure distribution (df = 1, only one parameter tested at a time)    

## Conditional Logistic Regression
### Mantal-Haenszel Methods: Can only control the matched factors  
### Mathmatical Modeling: (add # of pair -1 terms to represent the matched situation, use strata xxx to create dummy variables for the pair id)  

## Polytomous Logistic Regression 
(category - 1) models
proc logistic /link=glogit;

## Ordinal Logistic Regression  
### Score Test: Evaluate the proportional odds    
      1. Null hypothesis is that all ORs are equal (want a large p value)
      2. Follows a chi-sqaure distribution with a df = s * (k-2)   s- # of pedictor variables in the model; k - # of ordinal categories of the outcome 
      3. Need to consider the intercept (k-1), the ln(odds) of D>=g when all the independent variables = 0
      
## Log Binomial Regession
### Drawbacks: 
      1. Confidence interval may be narrower than they should be   
      2. Modeels may not always coverge  
## Colinearity  
### How to Tackle it:
      1. Observe: choose variables with narrow condifnece interval
      2. Condition Indices (CIs) >30
      3. Variance Decomposition Proportions (VDPs) 2 or more >0.5  
## Goodness of Fit


## Poisson Regression  
Approximates the bionomial distribution when N is big and p is small
calculate the ln_n first, ln_n = log(n)
proc genmod /link = log dist = poisson offseet = ln_n

