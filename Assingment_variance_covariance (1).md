
__Variance__<br>
Variance (σ2) is a measurement of the spread between numbers in a data set. It measures how far each number in the set is from the mean and is calculated by taking the differences between each number in the set and the mean, squaring the differences (to make them positive) and dividing the sum of the squares by the number of values in the set.Variance measures the variation of a single random variable.<br><br>
$$\sigma^2 = \sum_{i=0}^n \frac{({x_{i}- \bar{x}})^2} {n} $$ <br>
where ${x_{i}} =  i^{th}$ data point<br>
      $ {\bar {x}} $ = mean of all data point<br>
      n = the number of data points<br><br>
      
A variance value of zero indicates that all values within a set of numbers are identical; all variances that are non-zero will be positive numbers. A large variance indicates that numbers in the set are far from the mean and each other, while a small variance indicates the opposite.

__Covariance__<br>
The covariance of two variables (x and y) can be represented as cov(x,y). If E[x] is the expected value or mean of a sample ‘x’, then cov(x,y) can be represented in the following way:<br><br>
 $$ Cov(x,y) =  \sum_{i=0}^n \frac {({x_{i}- \bar{x}})({y_{j}- \bar{y}})}{n}$$<br><br>
 If we look at a single variable, say ‘x’, cov(x,x), the expression can be written in the following way:<br>
 $$ Cov(x,x) =  \sum_{i=0}^n \frac {({x_{i}- \bar{x}})({x_{j}- \bar{x}})}{n}$$
 For a sample covariance, the formula is slightly adjusted:
    $$ Cov(x,y) =  \sum_{i=0}^n \frac {({x_{i}- \bar{x}})({y_{j}- \bar{y}})}{n - 1}$$<br>
    where: ${x_{i}}$ = the values of the x-variable <br>
${y_{i}}$ = the values of the y-variable <br>
$\bar{x}$ = the mean (average) of the x-variable <br>
$\bar{y}$ = the mean (average) of the y-variable <br>
n = the number of the data points<br>
n - 1 = degree of freedom<br><br>

Degrees of freedom is the number of independent data points that went into calculating the estimate. As we see in the example above, it is not necessarily equal to the number of items in the sample (n).<br>

Covariance is used to analyze the linear relationship between the two variable.The positive and negative value in covariance matrix denotes the increasing and decreasing relationship between the two variables.<br>

__What is the variance-covariance matrix?__<br>
The diagonal of covariance matrix provides the variance of each individual matrix whereas the off-diagonal element provides the covariance between two variables.<br>
A variance-covariance matrix is a square matrix that contains the variances and covariances associated with several variables. The diagonal elements of the matrix contain the variances of the variables and the off-diagonal elements contain the covariances between all possible pairs of variables.<br>
The variance-covariance matrix is symmetric because the covariance between X and Y is the same as the covariance between Y and X. Therefore, the covariance for each pair of variables is displayed twice in the matrix: the covariance between the ith and jth variables is displayed at positions (i, j) and (j, i).<br>

Many statistical applications calculate the variance-covariance matrix for the estimators of parameters in a statistical model. It is often used to calculate standard errors of estimators or functions of estimators. For example, logistic regression creates this matrix for the estimated coefficients, letting you view the variances of coefficients and the covariances between all possible pairs of coefficients.<br>

__Properties of Covariance Matrix__<br><br><br><br>
__Addition to constant vectors__<br>
Let $a$ be a constant  K*1 vector and let x be a  K*1 random vector. Then,<br>
$$Var[a + x] = Var[x]$$<br>
__Multiplication by constant matrices__<br>
Let  $b$ be a constant  $M * K$ matrix and let  x be a  K*1 random vector. Then,<br>
$$Var[bx] = bVar[x]  b ^t$$<br>
__Linear transformations__<br>
Let $a$ be a constant  $M * 1$ vector,  $b$ be a constant  $M * K$ matrix and  $x$ a  Kx1 random vector. Then, combining the two properties above, one obtains<br>
$$Var[a + bx] = bVar[x]  b ^t$$<br>
__Symmetry__<br>
The covariance matrix  $Var[x]$  is a symmetric matrix, that is, it is equal to its transpose:<br>
$Var[x]  b ^t = E[(x - E[x])(x - E[x]^t)]^t$ <br>
             $= E[((x - E[x])(x - E[x]^t)^t]$<br>
             $= E[(x - E[x])(x - E[x]^t)]$<br>
             $= Var[x] $ 

__Semi-positive definiteness__<br>
The covariance matrix  $Var[x]$ is a positive-semidefinite matrix, that is, for any  $1 * K$ vector $a$:<br>
$$ aVar[x]a^t\geq = 0 $$

__Bias of an Estimator:__<br>
The bias (or bias function) of an estimator is the difference between this estimator's expected value and the true value of the parameter being estimated. An estimator or decision rule with zero bias is called unbiased. Otherwise the estimator is said to be biased. In statistics, "bias" is an objective property of an estimator, and while not a desired property.
Bias can also be measured with respect to the median, rather than the mean (expected value), in which case one distinguishes median-unbiased from the usual mean-unbiasedness property. Bias is related to consistency in that consistent estimators are convergent and asymptotically unbiased (hence converge to the correct value as the number of data points grows arbitrarily large), though individual estimators in a consistent sequence may be biased (so long as the bias converges to zero); see bias versus consistency.
