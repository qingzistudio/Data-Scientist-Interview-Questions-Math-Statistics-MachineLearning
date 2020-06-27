# Statistics

1.**What is  R-squared? What are some other metrics that could be better than  R-squared and why?**

 **R-squared** is usually used to evaluate the quality of fit of a model on data. The formula is R-squared =  \(Variation explained by model\)/\(Total variation\)  
**Adjusted R-squared**, which increases only if the new term improves the model more than would be expected by chance. The formula is $$R_{adj}^2 = 1-[(1-R^2)(n-1)/(n-k-1)]$$ , N is the number of data points, and K is the number of independent regressors.  
**One main difference between R-squared and adjusted R-squared**  is R-squared assumes that every single variable explains the variation, the adjusted R-squared tells the percentage of variation explained by only the variables that actually affect the dependent variable. 



