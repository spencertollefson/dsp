[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

numbers = np.random.random(1000)

numbers_pmf = thinkstats2.Pmf(numbers, label='numbers_pmf')

numbers_cdf = thinkstats2.Cdf(numbers, label='numbers_cdf')

-----

thinkplot.pmf(numbers_pmf, linewidth=0.08)

thinkplot.Config(xlabel='numbers', ylabel='probability')

-----

##### The PMF is a collection of 1000 solid vertical lines. There is a vertical line for each of the 1000 numbers in the sample, and each has exactly a 1/1000 probability of being chosen at random.

##### There is replacement, so it is possible but certainly uncommon for a number to be chosen twice since they are selected out to about 6 or 7 decimal places.

-----

thinkplot.Pdf(numbers_cdf)

thinkplot.Config(xlabel='numbers', ylabel='probability')