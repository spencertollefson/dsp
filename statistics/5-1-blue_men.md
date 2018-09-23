[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

import scipy.stats

mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)
type(dist)

dist.mean(), dist.std()

dist.cdf(mu-sigma)

-----


```
# converting from inches to cm and setting variables
lowheight = 2.54 * 70
maxheight = 2.54 * 73
print('lowheight: ', lowheight)
print('maxheight: ', maxheight)

# calculating difference between percentage of population up
# to 6'1" and removing percentage less than 5'10"
percentagemales = dist.cdf(maxheight) - dist.cdf(lowheight)
print(percentagemales)
```
##### 34.275% of the male population are between 5'10 and 6'1
