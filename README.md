# Least squares for Bernoulli random variables

The least-squares method of deriving statistics for the parameters of random variables works by minimising the "spread" of the variables around the expectation.  If we have n random variables (![](https://render.githubusercontent.com/render/math?math=X_i)) from a distribution with an expectation of ![](https://render.githubusercontent.com/render/math?math=\mathbb{E}(X)) this "spread" is defined as:

![](https://render.githubusercontent.com/render/math?math=S^2=\frac{1}{n}\sum_{i=1}^{n}[X_i-\mathbb{E}(X)]^2

If the ![](https://render.githubusercontent.com/render/math?math=X_i) in this expression are Bernoulli random variables ![](https://render.githubusercontent.com/render/math?math=\mathbb{E}(X)=p) so that above expression is thus:

![](https://render.githubusercontent.com/render/math?math=S^2=\frac{1}{n}\sum_{i=1}^{n}[X_i-p]^2

To obtain an estimator for p we find the value of p that minimises the above expression as shown below:

![](https://render.githubusercontent.com/render/math?math=\frac{\textrm{d}S^2}{\textrm{d}p}= - \frac{2}{n}\sum_{i=1}^{n}[X_i-\mathbb{E}(X)]\qquad\rightarrow\qquad\p=\frac{1}{n}\sum_{i=1}^n X_i)

To complete this exercise you need to write code in the panel on the left that shows how the estimator of for p depends on the number of samples it is computed from.  To complete the exercise you will need to

1. Finish the function `bernoulli`. This function should take a single argument `p`. It should return a Bernoulli random variable from a distribution with parameter `p`. 
2. Set the first element of the array called `indices` equal to 1, the second element of the array called `indices` to 2 and so on.
3. Set the first element of the array called `estimator` equal to an estimate of the parameter of the distribution that is calculated by generating 1 Bernoulli random variable with parameter `pval`, the second element of the array `estimator` equal to an estimate of the parameter of the distribution that is calculated by generating 2 Bernoulli random variables with parameter `pval`, set the third element of the array called `estimator` equal to an estimate of the parameter of the distribution that is calculated by generating 3 Bernoulli random variables with parameter `pval` and so on until you have computed an estimate of the parameter of the distribution from 200 Bernoulli random variables. 

When your code is complete a graph will be generated.  The red dots are the values of the least-squares estimator for the parameter of the distribution you sampled from.  The black dashed line is then the true value of the parameter.  You should see that the estimator converges to the true value of the parameter. 
