# R Statistical Project: 

In this workbook I play with some statistical methods to solve some easy problems: 

## Task 1: Optimization of continuous function

Finding the maximum of a complex function by building from the scratch the ***steepest ascent algorithm (aka gradien descent)***. I use *backtracking* to adjust the learning rate (alpha), meaning in case the new candidate produce smaller value than the current candidate, I know that the step is too big and ajust new alpha = 1/2 alpha.

## Task 2: Optimization of discrete function
- Task: Selecting a best subset of regressors to explain a sale price for houses, meaning we try to eliminate unrelated variables out of model.
- Method: ***changes in n-neighborhood algorithm***, systematically changes the neighborhood in two phases: firstly, descent to find a local optimum and second phase is to get out of the corresponding valley by changing n predictor. I build it from the scratch also. 
- Idea behind it: a function can have multiple local maximum, we can get stuck easily on one local optimum, it's hard to get out of it and explore the whole distribution. 
- Steps: 
  -  Draw 8 random starts contains 60 predictors with 1 - variable included and 0 - variable not included.
  - Using change in 1-neighborhood algorithm and BIC to have convergence towards 8 best models.
  - Use BIC to decide which one in 8 models is the best.
  - *Note:* we can increase the number of random starts and change in 2 or 3-neighborhood but it will be computationally more expensive.

- Additional note: This is just one approach, for this task we can use other methods like Shrinking method (Ridge, Lasso) or Machine Learning model.
- For discrete optimization we can apply more complex method like simulated annealing or genetic algorithm.

## Task 3: Monte Carlo algorithm for estimation

I include rmd file and html file. Please head to https://htmlpreview.github.io/ and paste html link to see the preview.
