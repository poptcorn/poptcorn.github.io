Gambling
---

In this post, I wanted to look at how possible it is to predict a film's success based on attributes we know before release.

The first thing to do would be to look at a simple correlation matrix of the numeric variables to see if any are obviously correlated. For the input variables we have: budget, runtime, number of directors, number of actors, and number of writers. For prediction variables we have: revenue, average vote, and number of votes.

![correlation matrix](../assets/post3/corr_matrix_cmap_annotated.png)

I immediately noticed three things in this correlation matrix:
1) Budget is a decent predictor of *revenue* (it's also a good predictor of number of votes, I guess higher budget movies have more advertising which increases both of those), but it's *negatively correlated with the average vote and the percent profit at the end.*
2) Running time is strongly correlated with the final average score, but not very correlated with percent profit.
3) The number of writers is positively correlated with the revenue but inversely correlated with the final rating. Having multiple directors is also more correlated with higher revenue.

Also, it looks like number of votes, budget, and revenue are all highly correlated. This makes sense for high profile films with large advertising campaigns.

Anyways, to see if we can predict the success of a film based on the inputs, I just quickly implemented a few simple regressors. Out of our dataset of ~23 thousand items, ~3 thousand have a complete set of attributes. We split this into a training set and and a testing set, and success was determined by the Pearson correlation coefficient between the estimated and true values of the testing set. The algorithms are just a nearest neighbor (NN) and the scikit-learn bayesian regression (BR), adaboost.R2 regression (AB), and random forest (RF) regression.

We tabulate the average Pearson correlation coefficients of the predicted and actual values for revenue, percent profit (revenue/budget), and average rating, for a few different training and testing set iterations.

Predicting

 | Revenue | Percent Profit | Rating |
NN | .54 | .12 | .27 |
AB | .61 | .28 | .46 |
BR | .71 | .19 | .38 |
RF | .76 | .31 | .49 |

In the past on other problems, I've tended to have good success with the random forest method, and it seems to perform well on these data as well. All of these predictors work substantially better than the nearest neighbor. As an example of the predictors, we plot the estimations of the different algorithms.

![algo predictions](../assets/post3/algo_predictions.png)

Visually, the random forest and adaboosted trees both perform decently (well better than random) at predicting the final score of a film based on the input data of: budget, runtime, number of directors, number of actors, and number of writers. That's pretty interesting.

After this, I'm just going to focus on the rating as the metric for success since I'm more interested in that than the revenue or profitability here.

So, let's go ahead and look at the average and deviations of film ratings for directors.

![director scores](../assets/post3/directors.png)

Now, I wasn't going to point out the lowest average rating directors, but the second lowest average was M. Night Shyamalan and that seems completely unfair to me. Say what you will, "Unbreakable" (2000) was a masterpiece.

The actors and writers have similar distributions sort of flaring out from a point at high-ratings, low variability.

![director scores](../assets/post3/directors.png)



tsne of films? color coded by rating / revenue ... revenue/budget as a percent profit?


Section 2 - actors, directors, writers with the best ratings, consistancy of actors, directors, writers






---
---
I’d like to thank the themoviedb.org folks, who gave me access to their API which was relatively painless to use. I am not affiliated with them in any way and my opinions are my own. I’d also like to thank the developers and maintainers of: Python, Gephi, and matplotlib.

themoviedb.org | python.org | scikit-learn.org | matplotlib.org
![the movie db](../assets/credit/tmdb.png) | ![python](../assets/credit/python.png) | ![gephi](../assets/credit/scikit.png) | ![matplotlib](../assets/credit/mpl.png)

---
---
