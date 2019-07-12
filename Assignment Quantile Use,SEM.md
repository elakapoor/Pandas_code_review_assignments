

```python
import numpy as np
import statsmodels.api as sm
import pylab
```


```python
test = np.random.normal(20, 5, 1000)
```


```python
sm.qqplot(test, loc = 20, scale = 5, line = '45')
pylab.show
```




    <function matplotlib.pyplot.show(*args, **kw)>




![png](output_2_1.png)


__Q1.) Explain why the points don’t lie on the line y=x<br>__
Ans.) A Q-Q plot is a scatterplot created by plotting two sets of quantiles against one another. If both sets of quantiles came from the same distribution, we should see the points forming a line that’s roughly straight.<br>

The quantile-quantile (q-q) plot is a graphical technique for determining if two data sets come from populations with a common distribution.<br>

Both Qs stand for “quantile.” A quantile is a slice of a dataset such that each slice contains the same amount of data. Imagine you have a sorted dataset of integers. If you specify that your dataset has two quantiles, then the first 50% of your dataset is in the first quantile (all of the integers from the minimum integer to the median integer) and then the last 50% of your dataset is in the second quantile (all of the integers from the median integer to the maximum integer).<br>

A Q-Q plot compares the quantiles of a dataset and a set of theoretical quantiles from a probability distribution. Therefore a Q-Q plot is trying to answer the question: “How similar are the quantiles in my dataset compared to what the quantiles of my dataset would be if my dataset followed a theoretical probability distribution?” <br>

In a Q-Q plot each data point in your dataset is put in its own quantile, then a data point is generated from the corresponding theoretical quantile.<br>

The points in the Q-Q plot does not form a straight line since the quantiles of the dataset does not match what the quantiles of the dataset would theoretically be if the dataset was normally distributed.<br>

__Q2.) Explain in your own words what is standard error of the mean?__

The standard error of the mean, also called the standard deviation of the mean, is a method used to estimate the standard deviation of a sampling distribution. 

As an example, consider an experiment that measures the speed of sound in a material along the three directions (along x, y and z coordinates). By taking the mean of these values, we can get the average speed of sound in this medium. The standard error of the mean refers to the change in mean with different experiments conducted each time.<br>

Mathematically, the standard error of the mean formula is given by:<br>

Standard Error of the Mean<br>

$$\sigma_M = \frac{\sigma}{\sqrt{N}}$$ <br>

$\sigma_M$ = the standard deviation of the original distribution <br>

$N$ = the sample size<br>

${\sqrt{N}}$ = root of the sample size<br>

It can be seen from the formula that the standard error of the mean decreases as N increases. This is expected because if the mean at each step is calculated using many data points, then a small deviation in one value will cause less effect on the final mean.<br>

The standard error of the mean tells us how the mean varies with different experiments measuring the same quantity. Thus if the effect of random changes are significant, then the standard error of the mean will be higher. If there is no change in the data points as experiments are repeated, then the standard error of mean is zero.<br>

__Q3.) Simulate SEM example using NumPy?__


```python
random_array = np.random.rand(20)
standard_deviation = (np.std(random_array)/np.sqrt(len(x)))
standard_deviation
```




    0.1575786922030988


