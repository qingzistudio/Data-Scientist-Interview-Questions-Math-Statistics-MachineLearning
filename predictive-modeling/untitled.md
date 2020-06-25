# Predictive Modeling

**1. What error metric would you use to evaluate how good a binary classifier is? What if the classes are imbalanced? What if there are more than 2 groups? \(From 120 interview questions\)**

Accuracy: Loss Function = ​ $$1/N\cdot\sum_i^N[\hat y^i!=y^i]$$ 

* Pros: Intuitive and easy to understand
* Cons: remove too many information, like datasets are imbalance, or with multiple groups

Log loss: Binary classification Loss Function = ​  $$-1/N\cdot\sum_i^N[y^ilog(\hat y^i)+(1-y^i)log(1-\hat y^i)]$$ , where $$y^i\in[0,1]$$ 

Multi-class classification Loss Function = $$-1/N\cdot\sum_i^N\sum_j^My_{ij}log(\hat y_{ij})$$ 

* Pros: No. 1 metric used in classification case. It can used as the objective function in ML models, also as a performance metric to punish misclassifications; in multi-class, log loss is the same as cross entropy.
* Cons: model get punished too heavily when we are certain about something that wrong

ROC Curve &  AUC Score: ROC Curve has y axis TPR= $$\frac{TurePositiveSamples}{PositiveSamples}$$, and x axis TNR= $$\frac{FalsePositiveSamples}{FalseSamples}$$, the most top-left side are better.  ROC AUC score is the area under ROC = $$1/2\cdot\sum_i^{m-1}(x_{i+1}-x_i)\cdot(y_{i+1}+y_i)$$ 

* Pros: Can be used in imbalanced datasets; Should use when you only care about comparing and ranking a set of predictors
* Cons: Only can be used in binary classifiers; it does not give information about the spatial distribution of model errors

Cohen Kappa: $$\kappa=(p_0-p_e)/(1-p_e)$$ , where $$p_0$$ is accuracy, and $$p_e$$is accuracy of the random classifier

* Pros: used heavily in the context of classification; work well for imbalanced problems
* Cons: no standardized way to interpret its values

_Read More_

{% embed url="https://www.quora.com/What-is-an-intuitive-explanation-for-the-log-loss-function" %}

{% embed url="https://neptune.ai/blog/evaluation-metrics-binary-classification?utm\_source=quora&utm\_medium=answer&utm\_campaign=blog-evaluation-metrics-binary-classification&utm\_content=blog" %}

{% embed url="https://towardsdatascience.com/choosing-the-right-metric-is-a-huge-issue-99ccbe73de61" %}

**2. What is regularization and where might it be helpful? What is an example of using regularization in a model?**











