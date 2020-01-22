# DS-Interview-Questions-Flashcards
A flashcards-like collection of interviews questions for Data Science


## Machine Learning-related


#### General Questions



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

	 How to interpret the Regression Coefficients for Curvilinear Relationships and Interactive Terms?
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

	What are limitations in Linear Regression models?
 <details>
<summary>ANS</summary>
<div>

 1. Linear regression models are sensitive to outliers
 
 2. Overfitting - It is easy to overfit your model such that your regression begins to model the random error (noise) in the data, rather than just the relationship between the variables. This most commonly arises when you have too many parameters compared to the number of samples
 
 3. Linear regressions are meant to describe linear relationships between variables. So, if there is a nonlinear relationship, then you will have a bad model. However, you can sometimes compensate for this by transforming some of the parameters with a log, square root, etc. transformation.
 
 4. The data may not fit the model due to violation of assumptions. The other answers deal with this and there is lots of material in textbooks and online about this, so, I won’t say more about it.
 
  See details [here](https://www.quora.com/What-are-the-limitations-of-linear-regression-modeling-in-data-analysis)
</div>
</details>
	
#### Logistic Regression

	How to interpret the weights in Logistic Regression?
 <details>
<summary>ANS</summary>
<div>

   - For intercept $\beta_0$, it just denotes that when all numerical features and categorical features are zero, the estimated odds (probability of event divided by probability of no event) are $\exp(\beta_0)$
   
   - For numerical features, If you increase the value of feature $x_j$  by one unit, the estimated odds change by a factor of  $\exp(\beta_j)$
   
   - For binary categorical features: one of the two values of the feature is the reference category. Changing the feature $x_j$ from the reference category to the other category changes the estimated odds by $\exp(\beta_j)$
   
   - Categorical feature with more than two categories: One solution to deal with multiple categories is one-hot-encoding, meaning that each category has its own column. You only need L-1 columns for a categorical feature with L categories, otherwise it is over-parameterized. The L-th category is then the reference category. You can use any other encoding that can be used in linear regression. The interpretation for each category then is equivalent to the interpretation of binary features.
   
   See details [here](https://christophm.github.io/interpretable-ml-book/logistic.html)
</div>
</details>

#### Navie Bayes

	What is navie about Navie Bayes?

<details>
<summary>ANS</summary>
<div>
 Its core assumption of conditional independence (i.e. all input features are independent from one another) rarely holds true in the real world

  See details [here](https://elitedatascience.com/machine-learning-algorithms)
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

#### Clustering

	How is k-NN different from k-means clustering?
<details>
<summary>ANS</summary>
<div>
 k-NN, or k-nearest neighbors is a classification algorithm, where the k is an integer describing the number of neighboring data points that influence the classification of a given observation. K-means is a clustering algorithm, where the k is an integer describing the number of clusters to be created from the given data.

  See details [here](https://www.springboard.com/blog/data-science-interview-questions/)
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
 	
 * Sampling based *Non-Probability*:
 	
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

	What is a statistical interaction?
	
<details>
<summary>ANS</summary>
<div>
 Basically, an interaction is when the effect of one factor (input variable) on the dependent variable (output variable) differs among levels of another  factor.

  See details [here](http://icbseverywhere.com/blog/mini-lessons-tutorials-and-support-pages/statistical-interactions/)
</div>
</details>

	What is selection bias?
<details>
<summary>ANS</summary>
<div>
 Selection (or “sampling”) bias occurs in an “active,” sense when the sample data that is gathered and prepared for modeling has characteristics that are not representative of the true, future population of cases the model will see. That is, active selection bias occurs when a subset of the data are systematically (i.e., non-randomly) excluded from analysis.

  See details [here](https://www.elderresearch.com/blog/selection-bias-in-analytics)
</div>
</details>

	What is an example of a data set with a non-Gaussian distribution?
<details>
<summary>ANS</summary>
<div>
 The Gaussian distribution is part of the Exponential family of distributions, but there are a lot more of them, with the same sort of ease of use, in many cases, and if the person doing the machine learning has a solid grounding in statistics, they can be utilized where appropriate. 
 
 In a Poisson or Bernoulli process, the statistic that gives the time to the next event is not normal, but the data collected in such processes is the number of events per time unit, and for large 𝑛, that's approximately normal.

  See details [here](https://www.quora.com/Most-machine-learning-datasets-are-in-Gaussian-distribution-Where-can-we-find-the-dataset-which-follows-Bernoulli-Poisson-gamma-beta-etc-distribution)
</div>
</details>

	What is F-test?
<details>
<summary>ANS</summary>
<div>
 The F-test can be used in regression analysis to determine whether a complex model is better than a simpler version of the same model in explaining the variance in the dependent variable.
 
 The test statistic of the F-test is a random variable whose Probability Density Function is the F-distribution under the assumption that the null hypothesis is true.
 
 The testing procedure for the F-test for regression is identical in its structure to that of other parametric tests of significance such as the t-test.

  See details [here](https://towardsdatascience.com/fisher-test-for-regression-analysis-1e1687867259)
</div>
</details>

	What is the Standard Deviation?

 
 <details>
<summary>ANS</summary>
<div>
  The standard deviation is a statistic that measures the dispersion of a dataset relative to its mean and is calculated as the square root of the variance. It is calculated as the square root of variance by determining the variation between each data point relative to the mean. If the data points are further from the mean, there is a higher deviation within the data set; thus, the more spread out the data, the higher the standard deviation.

  See details [here](https://www.investopedia.com/terms/s/standarddeviation.asp)
</div>
</details>

	What is the Standard Error?

 
 <details>
<summary>ANS</summary>
<div>
  The standard error (SE) of a statistic is the approximate standard deviation of a statistical sample population. The standard error is a statistical term that measures the accuracy with which a sample distribution represents a population by using standard deviation. In statistics, a sample mean deviates from the actual mean of a population—this deviation is the standard error of the mean.

  See details [here](https://www.investopedia.com/terms/s/standard-error.asp)
</div>
</details>


	Describe the procedure of Hypothesis Testing.
	
 <details>
<summary>ANS</summary>
<div>

  1. Determine the null hypothesis and alternative hypothesis
  2. Verifiy data condition
  3. Assume that the null hypothesis is true, calculate the p-value
  4. Decide whether or not the result is statistically significant
  5. Report the conclusion 

  See details [here](https://docs.google.com/document/d/1dw07lpLci5yKaV8ZJIDL6C46eaTE1OW_YNeHbXh-KN0/edit)
</div>
</details>



## Programming-related

**Include questions about Data Structures/Algorithms/Coding Concepts. Since I assume for those questions, coding practice should be focused more.**

	What are some pros and cons about your favorite statistical software?
<details>
<summary>ANS</summary>
<div>
 For Python and R:
 
 * Pros:
 
 	* A large number of repositories in GitHub

 	* Packages for Data Science

 * Cons:

 	* Python doesn't have good documentation

 	* R is an erratic tool for machine learning projects

 	* R is a slow programming language

  See more details [here](https://bbvaopen4u.com/en/actualidad/pros-and-cons-python-and-r-data-science) and [here](https://it.unt.edu/rss-pros-and-cons-software-packages)
</div>
</details>

	How would you sort a large list of numbers?
<details>
<summary>ANS</summary>
<div>

  See details [here](https://en.wikipedia.org/wiki/Sorting_algorithm)
</div>
</details>

	What Native Data Structures Can You Name in Python?
<details>
<summary>ANS</summary>
<div>
 List, Dictionary, Set, String, Tuple
 
  See details [here](https://www.springboard.com/blog/python-interview-questions/)
</div>
</details>

	In Python, How is Memory Managed?
<details>
<summary>ANS</summary>
<div>
 In Python, memory is managed in a private heap space. This means that all the objects and data structures will be located in a private heap. However, the programmer won’t be allowed to access this heap. Instead, the Python interpreter will handle it. At the same time, the core API will enable access to some Python tools for the programmer to start coding.  
 
 See details [here](https://www.springboard.com/blog/python-interview-questions/)
</div>
</details>	

	What is worst case time complexity of quick sort?
	
	What is average case time complexity of quick sort?
	
	
	
	What is worst case time complexity of looking up a value in a hashtable?
	
	
	What is average case time complexity of looking up a value in a hashtable?
	
	
	What is average case time complexity of looking up a value in a hashtable?
	
	
	What is the difference between black-red tree with binary search tree?
	
	
	What is the largest possible height of a binary tree with n elements?
	
	
	What is the largest possible height of a balanced binary search tree with n elements?

## SQL-related

	Tell me the difference between an inner join, left join/right join, and union.
<details>
<summary>ANS</summary>
<div>
 In a Venn diagram the inner join is when both tables have a match, a left join is when there is a match in the left table and the right table is null, a right join is the opposite of a left join, and a full join is all of the data combined. 
 
 See details [here](https://www.springboard.com/blog/joining-data-tables/)
</div>
</details>	

	What does UNION do? What is the difference between UNION and UNION ALL?
<details>
<summary>ANS</summary>
<div>
 UNION removes duplicate records (where all columns in the results are the same), UNION ALL does not.
 
 See details [here](https://stackoverflow.com/questions/49925/what-is-the-difference-between-union-and-union-all)
</div>
</details>	



## Deep Learning-related 