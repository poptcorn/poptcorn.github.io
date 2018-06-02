Gambling
---

In this post, I wanted to look at how possible it is to predict a film's success based on attributes we know before release.

The first thing to do would be to look at a simple correlation matrix of the numeric variables to see if any are obviously correlated. For the input variables we have: budget, runtime, number of directors, number of actors, and number of writers. For prediction variables we have: revenue, average vote, and number of votes.

![correlation matrix](../assets/post2/corr_matrix_cmap_annotated.png)

I immediately noticed two things in this correlation matrix:
1) Budget is a decent predictor of revenue (it's also a good predictor of number of votes, I guess higher budget movies have more advertising which increases both of those), but it's negatively correlated with the average vote at the end.
2) Along with a high budget, having more directors and more writers seems to lower the final average rating of the film. Maybe artistic collaboration is actually more of a conflict.

Anyways, to see if we can predict the success of a film based on the inputs, I just quickly implemented a few simple regressors. Out of our dataset of ~23 thousand items, ~3 thousand have a complete set of attributes. We split this into a training set and and a testing set, and success was determined by the Pearson correlation coefficient between the estimated and true values of the testing set. The algorithms are just a nearest neaighbor (KD) and the scikit-learn support vector regression, bayesian regression, and random forest regression.

# Predicting Revenue
 | 1 | 2 | 3
KD  | 0.54 | 0.52 | 0.54
SVM | 0.05 | 0.09 | 0.08
BR  | 0.74 | 0.72 | 0.72
RF  | 0.75 | 0.71 | 0.75

# Predicting Rating
 | 1 | 2 | 3
KD  | 0.28 | 0.27 | 0.32
SVM | 0.20 | 0.22 | 0.21
BR  | 0.45 | 0.36 | 0.42
RF  | 0.50 | 0.50 | 0.54


#Section 2 - actors, directors, writers with the best ratings, consistancy of actors, directors, writers


Budget | 1.0 |0.72 |0.17 |-0.07 |0.57 |0.06 |0.26 |0.15 |
Revenue | 0.72 |1.0 |0.19 |0.15 |0.78 |0.08 |0.34 |0.11 |
Runtime | 0.17 |0.19 |1.0 |0.35 |0.19 |-0.12 |0.25 |-0.06 |
Avg. Vote | -0.07 |0.15 |0.35 |1.0 |0.32 |0.01 |0.2 |-0.04 |
Num. Votes | 0.57 |0.78 |0.19 |0.32 |1.0 |0.05 |0.4 |0.1 |
Num. Dirs. | 0.06 |0.08 |-0.12 |0.01 |0.05 |1.0 |-0.03 |0.13 |
Num. Actors | 0.26 |0.34 |0.25 |0.2 |0.4 |-0.03 |1.0 |0.06 |
Num. Writers | 0.15 |0.11 |-0.06 |-0.04 |0.1 |0.13 |0.06 |1.0 |
 | Budget | Revenue | Runtime | Avg. Vote | Num. Votes | Num. Dirs. | Num. Actors | Num. Writers |



---
---
I’d like to thank the themoviedb.org folks, who gave me access to their API which was relatively painless to use. I am not affiliated with them in any way and my opinions are my own. I’d also like to thank the developers and maintainers of: Python, Gephi, and matplotlib.

themoviedb.org | python.org | gephi.org | matplotlib.org
![the movie db](../assets/credit/tmdb.png) | ![python](../assets/credit/python.png) | ![gephi](../assets/credit/gephi.png) | ![matplotlib](../assets/credit/mpl.png)

---
---
