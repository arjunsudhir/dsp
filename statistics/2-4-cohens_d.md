[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> **Exercise 2.4** Using the variable `totalwgt_lb`, investigate whether first babies are lighter or heavier than others. Compute Cohen’s *d* to quantify the difference between the groups. How does it compare to the difference in pregnancy length?

```python
# compare the means
print("total weight means")
print("firsts =",firsts.totalwgt_lb.mean())
print("others =",others.totalwgt_lb.mean())
print("diff in means =",firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean())
```

>> total weight means  
firsts = 7.201094430437772  
others = 7.325855614973262  
diff in means = -0.12476118453549034  

```python
# calculate cohen's d effect size
diff = firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean()
var1 = firsts.totalwgt_lb.var()
var2 = others.totalwgt_lb.var()
n1, n2 = len(firsts.totalwgt_lb), len(others.totalwgt_lb)

pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
cohend = diff / np.sqrt(pooled_var)
```

>> `cohend` = -0.0886729270726  

>> The difference in live birth weight means for first babies versus others is 0.089 standard deviations, which is almost as small as the difference in pregnancy length (0.029).
