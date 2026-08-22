# Tabular Data

| x | y  |
| 0 | 1  |
| 0 | 2  |
| 3 | 1  |
| 0 | -1 |

- Measuring distances:
	- Euclidean: $\sqrt{ \sum_{i=1}^m (x_i - y_i)^2}$
	- Manhattan: $\sum_{i=1}^m |x_i - y_i|$

- Understanding high dimensional data:
	- Understand 2 dimensions, then extrapolate to higher dimensions
- Data + Distance Metric, what can we know:
	- What data points are closest to eachother
	- Ex: I have customer Mueen's data, who is closest to Mueen's data?
- Ex, how does learning start:
	- With comparing, then addition, subtraction, mult, division, 
	  exponentiation, etc.
- Why Euclidean distance:
	- A standard
	- Not only a function, but also a metric
	- Distance Metric (when does a distance function become a distance 
	  metric?):
		1. Non-negative ($\mathbb{R}^+$)
		2. Distance is zero if and only if the vectors are equal
		3. Symmetric: $d(\bar x, \bar y) = d (\bar y, \bar x)$
		4. Triangle Inequality: 
		  $d(\bar x, \bar y) + d(\bar x, \bar z) \ge d(\bar y, \bar z)$
		  
- Curse of High Dimensionality:
	- The higher the dimensions go, the 'looser' the triangle inequality
	  seems, though there is always the chance for equality
- What about the units of a distance metric:
	- The units of a distance metric is nonsensicle, we want to normalize
	  things, s.t. the columns do not have units

## z-Normalization

$$
\hat x_i = (\frac{x_i - \mu}{\sigma})
$$

$$
\mu = \frac{\sum_i^m x_i}{m}
$$

Sample Standard Deviation:
$$
\sigma = \sqrt{ \frac{\sum_{i=1}^m(x_i - \mu)^2}{m - 1}
$$

- Normalizing: How far are you from the mean?
- Why normalize?
	- To make data more comprehensible, what does the distance actually 
	  mean?
	- Can conversion be done? That is common:
		- What if all columns are measures are of distance, can convert
		  to common units, and can even do a log v
