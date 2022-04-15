# intro_stat_learning
This repo contains my notes and code from working through the Introduction to Statistical Learning book by James, Witten, Hastie, and Tibshirani


## Translation Idiosyncracies from R to Python
R is excellent for statistics. Many of the things statisticians need are already built into the language.

Python has a mix of different libraries to do statistics, but that doesn't mean they're great at every aspect of doing statistics.

1. [Python starting in 3.10 is building in a statistics library](https://docs.python.org/3/library/statistics.html), but the documentation says it is about as good as a graphing calculator and should not be relied on for more exacting calculations. 

2. Scikit-learn has a lot of community support, but is not a true statistics library. You can think of it instead as a well supported applied statistics library for machine learning. It is difficult to extract coefficients and p-values, which are things you would expect to do as a statistician. [Discussion here](https://www.reddit.com/r/datascience/comments/fotjm9/statsmodels_vs_sklearn_for_the_linear_models/)

3. Numpy has some statistics functions, but looks like it is more designed to do array mathematics. See this [Quora answer](https://qr.ae/pvs4Mh)

4. Scipy also has statistics but it is missing some useful functions that are in R. It also seems to have a heavier focus on distributions, and "setting up statistics problems"

5. Statsmodels is going to be needed for how it handles regression. However, statsmodels needs assistance from Scipy.


Moving forward, and even rolling back with some refactoring, likely will rely on a combination of scipy and statsmodels to do the actual statistical calculations.