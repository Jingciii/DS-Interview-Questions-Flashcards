# DS-Interview-Questions-Flashcards
A flashcards-like collection of interviews questions for Data Science


## Machine Learning-related

#### Logistic Regression

 * How to interpret the weights in Logistic Regression?
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

## Statistics-related


 * What is **Simpson's Paradox**?
<details>
<summary>ANS</summary>
<div>
Simpson's paradox occurs when groups of data show one particular trend, but this trend is reversed when the groups are combined together. Understanding and identifying this paradox is important for correctly interpreting data. See details [here](https://brilliant.org/wiki/simpsons-paradox/)
</div>
</details>

## Programming-related

## SQL-related

## Deep Learning-related 