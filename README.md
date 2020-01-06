# DS-Interview-Questions-Flashcards
A flashcards-like collection of interviews questions for Data Science


## Machine Learning-related


#### Generate Questions



	<font size="3">Give me an example where MLE is equivalent to MAP</font>

 
 <details>
<summary>ANS</summary>
<div>
 When using uniform prior, we assign equal weights everywhere, on all possible values of the $\theta$. The implication is that the likelihood equivalently weighted by some constants. Being constant, we could be ignored from our MAP equation, as it will not contribute to the maximization.

  See details [here](https://wiseodd.github.io/techblog/2017/01/01/mle-vs-map/)
</div>
</details>

#### Linear Regression

- [x] What is **Bayesian Linear Regression**
 <details>
<summary>ANS</summary>
<div>
  The response variable generated from a normal (Gaussian) Distribution characterized by a mean and variance. The mean for linear regression is the transpose of the weight matrix multiplied by the predictor matrix. The variance is the square of the standard deviation σ (multiplied by the Identity matrix because this is a multi-dimensional formulation of the model).

 The aim of Bayesian Linear Regression is not to find the single “best” value of the model parameters, but rather to determine the posterior distribution for the model parameters. 
  See details [here](https://towardsdatascience.com/introduction-to-bayesian-linear-regression-e66e60791ea7)
</div>
</details>

#### Logistic Regression

 - [x] How to interpret the weights in Logistic Regression?
 <details>
<summary>ANS</summary>
<div>

   - For intercept $\beta_0$, it just denotes that when all numerical features and categorical features are zero, the estimated odds (probability of event divided by probablity of no event) are $\exp(\beta_0)$
   
   - For numercial features, If you increase the value of feature $x_j$  by one unit, the estimated odds change by a factor of  $\exp(\beta_j)$
   
   - For binary categorical features: one of the two values of the feature is the reference category. Changing the feature $x_j$ from the reference category to the other category changes the estimated odds by $\exp(\beta_j)$
   
   - Categorical feature with more than two categories: One solution to deal with multiple categories is one-hot-encoding, meaning that each category has its own column. You only need L-1 columns for a categorical feature with L categories, otherwise it is over-parameterized. The L-th category is then the reference category. You can use any other encoding that can be used in linear regression. The interpretation for each category then is equivalent to the interpretation of binary features.
   
   See details [here](https://christophm.github.io/interpretable-ml-book/logistic.html)
</div>
</details>


#### Random Forest

 - [x] How does random forest calcuate **Feature Importance**?
<details>
<summary>ANS</summary>
<div>
 By the decrease in node impurity weighted by the probability of reaching that node. The node probability can be calculated by the number of samples reaches that node divided by total number of samples.

  See details [here](https://towardsdatascience.com/the-mathematics-of-decision-trees-random-forest-and-feature-importance-in-scikit-learn-and-spark-f2861df67e3)
</div>
</details>
 

## Statistics-related


 - [x] What is **Simpson's Paradox**?
<details>
<summary>ANS</summary>
<div>
 Simpson's paradox occurs when groups of data show one particular trend, but this trend is reversed when the groups are combined together. Understanding and identifying this paradox is important for correctly interpreting data.

  See details [here](https://brilliant.org/wiki/simpsons-paradox/)
</div>
</details>

## Programming-related

## SQL-related

## Deep Learning-related 