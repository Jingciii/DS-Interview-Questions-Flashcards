# DS-Interview-Questions-Flashcards
A flashcards-like collection of interviews questions for Data Science


## Machine Learning-related


#### Generate Questions



	Give me an example where MLE is equivalent to MAP

 
 <details>
<summary>ANS</summary>
<div>
 When using uniform prior, we assign equal weights everywhere, on all possible values of the $\theta$. The implication is that the likelihood equivalently weighted by some constants. Being constant, we could be ignored from our MAP equation, as it will not contribute to the maximization.

  See details [here](https://wiseodd.github.io/techblog/2017/01/01/mle-vs-map/)
</div>
</details>

#### Linear Regression

	What is Bayesian Linear Regression?
 <details>
<summary>ANS</summary>
<div>
  The response variable generated from a normal (Gaussian) Distribution characterized by a mean and variance. The mean for linear regression is the transpose of the weight matrix multiplied by the predictor matrix. The variance is the square of the standard deviation σ (multiplied by the Identity matrix because this is a multi-dimensional formulation of the model).

 The aim of Bayesian Linear Regression is not to find the single “best” value of the model parameters, but rather to determine the posterior distribution for the model parameters. 
 
  See details [here](https://blog.minitab.com/blog/adventures-in-statistics-2/how-to-interpret-regression-analysis-results-p-values-and-coefficients)
</div>
</details>

	 How to interpret the Regression Coefficients for Cuvilinear Relationships and Interactive Terms?
 <details>
<summary>ANS</summary>
<div>
  Interaction terms indicate that the effect of one predictor depends on the value of another predictor. 
 
  See details [here](https://towardsdatascience.com/introduction-to-bayesian-linear-regression-e66e60791ea7)
</div>
</details>

	What are the assumptions required for linear regression?
 <details>
<summary>ANS</summary>
<div>

 1. There is a linear relationship between the dependent variables and the regressors, meaning the model you are creating actually fits the data
 
 2. The errors or residuals of the data are normally distributed and independent from each other
 
 3. There is minimal multicollinearity between explanatory variables
 
 4. Homoscedasticity. This means the variance around the regression line is the same for all values of the predictor variable.
 
  See details [here](https://www.springboard.com/blog/data-science-interview-questions/)
</div>
</details>
	
#### Logistic Regression

	How to interpret the weights in Logistic Regression?
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

	How does random forest calcuate Feature Importance?
<details>
<summary>ANS</summary>
<div>
 By the decrease in node impurity weighted by the probability of reaching that node. The node probability can be calculated by the number of samples reaches that node divided by total number of samples.

  See details [here](https://towardsdatascience.com/the-mathematics-of-decision-trees-random-forest-and-feature-importance-in-scikit-learn-and-spark-f2861df67e3)
</div>
</details>
 

## Statistics-related


	What is Simpson's Paradox?
<details>
<summary>ANS</summary>
<div>
 Simpson's paradox occurs when groups of data show one particular trend, but this trend is reversed when the groups are combined together. Understanding and identifying this paradox is important for correctly interpreting data.

  See details [here](https://brilliant.org/wiki/simpsons-paradox/)
</div>
</details>

	What is the Central Limit Theorem and why is it important?
<details>
<summary>ANS</summary>
<div>
 Suppose that we are interested in estimating the average height among all people. Collecting data for every person in the world is impossible. While we can’t obtain a height measurement from everyone in the population, we can still sample some people. The question now becomes, what can we say about the average height of the entire population given a single sample. The Central Limit Theorem addresses this question exactly.
 
 Formally, it states that if we sample from a population using a sufficiently large sample size, the mean of the samples (also known as the sample population) will be normally distributed (assuming true random sampling). What’s especially important is that this will be true regardless of the distribution of the original population.

  See details [here](https://spin.atomicobject.com/2015/02/12/central-limit-theorem-intro/)
</div>
</details>	

	What is sampling? How many sampling methods do you know?
<details>
<summary>ANS</summary>
<div>
 Sampling is a statistical analysis technique used to select, manipulate and analyze a *representative* subset of points to identify trends and patterns in the larger data set being examined.
 
 * Sampling based on *Probability*:
 	* Simple random sampling: Software is used to randomly select subjects from the whole population
 	
 	* Stratified sampling: Subsets of the data sets or population are created based on a common factor, and samples are randomly collected from each subgroup
 	
 	* Cluster sampling: The larger data set is divided into subsets (clusters) based on a defined factor, then a random sampling of clusters is analyzed
 	
 	* Multistage sampling: A more complicated form of cluster sampling, this method also involves dividing the larger population into a number of clusters. Second-stage clusters are then broken out based on a secondary factor, and those clusters are then sampled and analyzed. This staging could continue as multiple subsets are identified, clustered and analyzed
 	
 	* Systematic sampling: A sample is created by setting an interval at which to extract data from the larger population -- for example, selecting every 10th row in a spreadsheet of 200 items to create a sample size of 20 rows to analyze
 	
 * Sampling based *Non-Probablity*:
 	
 	* Convenience sampling: Data is collected from an easily accessible and available group
 	
 	* Consecutive sampling: Data is collected from every subject that meets the criteria until the predetermined sample size is met

 	* Purposive or judgmental sampling: The researcher selects the data to sample based on predefined criteria

 	* Quota sampling: The researcher ensures equal representation within the sample for all subgroups in the data set or population

  See details [here](https://searchbusinessanalytics.techtarget.com/definition/data-sampling)
</div>
</details>	

	What is the difference between type I vs type II error?
<details>
<summary>ANS</summary>
<div>
 A type I error (FP) occurs when the null hypothesis is true, but is rejected. Let me say it again, a type I error occurs when the null hypothesis is actually true, but was rejected as false by the testing. 
 
 A type II (FN) error occurs when the null hypothesis is false, but erroneously fails to be rejected. Let me say this again, a type II error occurs when the null hypothesis is actually false, but was accepted as true by the testing.

  See details [here](https://www.datasciencecentral.com/profiles/blogs/understanding-type-i-and-type-ii-errors)
</div>
</details>

	How to interpret P-values in Linear Regression Analysis
<details>
<summary>ANS</summary>
<div>
 The p-value for each term tests the null hypothesis that the coefficient is equal to zero (no effect). A low p-value (< 0.05) indicates that you can reject the null hypothesis. In other words, a predictor that has a low p-value is likely to be a meaningful addition to your model because changes in the predictor's value are related to changes in the response variable. Conversely, a larger (insignificant) p-value suggests that changes in the predictor are not associated with changes in the response.

  See details [here](https://blog.minitab.com/blog/adventures-in-statistics-2/how-to-interpret-regression-analysis-results-p-values-and-coefficients)
</div>
</details>

## Programming-related

## SQL-related

## Deep Learning-related 