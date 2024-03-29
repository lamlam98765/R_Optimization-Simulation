# R Statistical Project: 

In this workbook I play with some statistical methods to solve some easy problems: 

## Task 1: Optimization of continuous function

Finding the maximum of a complex function by building from the scratch the ***steepest ascent algorithm (aka gradien descent)***. 

I use *backtracking* to adjust the learning rate (*alpha*), meaning when the new candidate produce smaller value than the current candidate, then it overshoots, the learning rate and learning step are too big so the new *alpha* is adjusted as 1/2 old *alpha*.


## Task 2: Optimization of discrete function
- Task: Selecting a best subset of regressors to explain a sale price for houses, meaning we try to eliminate unrelated variables out of model.
- Method: ***changes in n-neighborhood algorithm***, systematically changes the neighborhood in two phases: firstly, descent to find a local optimum and second phase is to get out of the corresponding valley by changing n predictor. I build it from the scratch also. 
- Steps: 
  -  Draw 8 random starts contains 60 predictors, with 1 as *this predictor included* and 0 as *this predictor not included*.
  - Using change in 1-neighborhood algorithm (change one factor from 0 to 1 - from exclude to include or vice versa) and using information criteria BIC to have convergence towards 8 best models.
  - Use BIC to decide which one in 8 models is the best.
  - *Note:* we can increase the number of random starts and change in 2 or 3-neighborhood but it will be computationally more expensive.

- *Idea behind it*: a function can have multiple local maximum, we can get stuck easily on one, it's hard to get out of it and explore the whole distribution. That's why I have 8 random starts converge to 8 (local) optimums in hope of exploring the whole distribution.

- Additional note: This is just one approach, for this task we can use other techniques like Shrinking method (Ridge, Lasso) or Machine Learning model.
- For discrete optimization we can apply more complex procedures like simulated annealing or genetic algorithm.


## Task 3: Monte Carlo algorithm for estimation

I include rmd file and html file. Please head to https://htmlpreview.github.io/ and paste html link to see the preview.
