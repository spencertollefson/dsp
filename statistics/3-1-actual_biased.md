[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>>
```
sp = nsfg.ReadFemResp()
numkids = resp.numkdhh
kidspmf = thinkstats2.Pmf(numkids, label='original')
kidshist = thinkstats2.Hist(numkids)

thinkplot.Hist(kidshist, label ='Distribution of number of children in households')
thinkplot.Config(xlabel='Number of chilren', ylabel='Count of households')

thinkplot.Hist(kidspmf, label ='Distribution of number of children in households')
thinkplot.Config(xlabel='Number of chilren', ylabel='Probability')


def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf


biased_pmf = BiasPmf(kidspmf, label='biased')
thinkplot.Pmf(biased_pmf, label='Biased PMF distribution')
thinkplot.Config(xlabel='Number of children in household', ylabel='Probability')

thinkplot.PrePlot(2)
thinkplot.Pmfs([kidspmf, biased_pmf])
thinkplot.Config(xlabel='Number of children in household', ylabel='probability')

print('Mean of original: ', kidspmf.Mean())
print('Mean of bias: ', biased_pmf.Mean())
```
