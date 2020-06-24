##### 1. What error metric would you use to evaluate how good a binary classifier is? What if the classes are imbalanced? What if there are more than 2 groups? (From 120 interview questions)

Accuracy:  Loss Function = $1/n*\sum_i^n[\hat y^i!=y^i]$

- Pros: Intuitive and easy to understand
- Cons: remove too many information, like dataset is imbalance, or with multiple groups

Log loss: Loss Function = $-1/n\sum_i^n[y^ilog(\hat y^i)+(1-y^i)log(1-\hat y^i)]$

* Pros: 