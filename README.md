Logistic Regression to demostrate the use of HYperparameter Tuning.

Dataset Used: Iris Dataset
DataModel : Losgistc Regression
Independent Varibales: sepal_length,sepal_width,petal_length and petal_width
Dependent Variables:Species
Goal: find the species of the flowers given the sepal_length,sepal_width,petal_length and petal_width by fine tuning hyperparameters using GridSearchCV.


GridSearchCV:
GridSearchCV is a method provided by scikit learn to systematically work through multiple combinations of parameter tunes,cross-validate each combination and determine the best parameter set.

Parameters Provided Here Are:
1.Penalty : L1,L2 and Elasticnet
*   L1(lasso) : adds absolute value of coefficients as penalty term to loss function.This can lead of spare models where some coefficents are exactly zero.Effective for feature selection.
*   L2(Ridge) : adds squared value of the coefficients as peablty term to losss function.This doesnt compelted shrink coefficients to zero.
*   ElasticNet : A combination of L1 and L2 penalities. 
2.C Value : Regularization parameter that controls the inverse strength of regularization (1/lambda)
*   High C Value : Implies weaker regularization,meaning model will try to fit the model as close as possible to training data.
*   Low C Value : Implies stronger regularization,meaning model is less likely to overfit.


How these work together:
Objective Function = Data Loss + 1/C * Penalty Term

* Penalty : Determins type of regualrization
* C       : controls strength of regularization, where a lower (C) means stronger regularization and Higher(C) means weaker regularization
3.Max iterations: In logistic regression and other algos,it refers to maximum number of iterations that algorithm is allowed to run.This parameter is important for alogorithm that rely on iterative methods to converge to a solution,such as Gradient Descent.

For Example: max_iteratiosn =200,
then model will attempt to converge within 200 iterations.

Importance:
* Convergence : if max_iter is low,alogorithm may stop before finding optimal solution,leading to underfitting of the model.

* Efficiency:if max_iter is too high,algorithm may waste time trying to converge when its not necessary,consuming more computational resources.

Therefore adjusting this would be part of Hyperparmeter Tuning.
