# MSCS_634_Lab_4

The purpose of this lab was to gain experience with various kinds of regression models and how to tune them. 

Firstly, I started by loading and exploring the diabetes dataset. It had no missing values, so I did not have to implement any procedure for handling them.

For measuring accuracy, we do MAE, MSE, RMSE, and R2. MAE measures mean absolute error, meaning how far away from the correct prediction the regression was. MSE measures the same, but squares the error. That means that errors that were further away from the correct prediction are much more punishing than with MAE. RMSE is a mixture of both, where the value is brought back to non-squared units; however, even in this case, having larger errors is more punishing than missing by a little bit. Finally, R2 measured the proportion of variance in the dependent variable that can be explained by the independent variable. 

Firstly, I implemented simple linear regression using BMI as a predictor. At first sight, it looked like it did not perform that well, but later on, it turned out not to be that bad in comparison. 
- Mean Absolute Error (MAE): 52.26
- Mean Squared Error (MSE): 4061.83
- Root Mean Squared Error (RMSE): 63.73
- R² Score: 0.23

Secondly, I tried multiple regression, which turned out to be much more accurate. 
Mean Absolute Error (MAE): 42.79
Mean Squared Error (MSE): 2900.19
Root Mean Squared Error (RMSE): 53.85
R² Score: 0.45

Thirdly, I tried polynomial regression with several degree values. However, none of them turned out to be more accurate than even the simple regression model and with higher degree levels the accuracy even went down. With high degree values, it even led to R² being negative. 

Lastly, I implemented Lasso and Ridge regressions with several Alpha values. Alpha basically applies weights to features and makes some of them more and less important. The higher the alpha, the more of this weight coefficient is applied. Surprisingly, I got the best result with alpha coefficient of 0,1.

- Ridge Regression (alpha=0.01)
- MAE: 41.46
- MSE: 2732.67
- RMSE: 52.27
- R²: 0.48


- Lasso Regression (alpha=0.01)
- MAE: 41.12
- MSE: 2698.03
- RMSE: 51.94
- R²: 0.49

When I increased the Alpha values, the model became less accurate.

All of these results lead me to only one conclusion. The dataset is best explained by multiple linear regression - the data is mostly linear. 
