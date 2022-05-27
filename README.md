![Can a single statistic predict MLB 1987 hitters salary](https://user-images.githubusercontent.com/90852678/170703197-d85c4c3b-dea2-4173-8ca5-2ed72447ad7a.png)
# Predicting MLB hitters salary in 1987 using 1986 performance statistics.

![](https://img.shields.io/badge/Status-Active-green?style=for-the-badge)
![](https://img.shields.io/badge/Complexity-Low-blue?style=for-the-badge)
[![GitHub issues](https://img.shields.io/github/issues/nsqlabs/MLB-Hitters-performance-against-salary-1986?style=for-the-badge)](https://github.com/nsqlabs/MLB-Hitters-performance-against-salary-1986/issues)
[![GitHub Stars](https://img.shields.io/github/stars/nsqlabs/MLB-Hitters-performance-against-salary-1986?style=for-the-badge)](https://github.com/nsqlabs/MLB-Hitters-performance-against-salary-1986/stars)
[![GitHub Stars](https://img.shields.io/github/last-commit/nsqlabs/MLB-Hitters-performance-against-salary-1986?style=for-the-badge)](https://github.com/nsqlabs/MLB-Hitters-performance-against-salary-1986/last-commit)


> Is a single variable enough to predict a player salary?
> Can it be reliable?

I asked myself these questions when exploring this dataset. Previous to the "moneyball" era, batting average (AVG) was the golden statistic for evaluating hitters so I decided to explore this assumption and test if this argument is strong enough to back it up with data. I am building multiple simple linear regression models to try to measure which statistics ensures a better performance for predicting salary.

# Table of contents

- [Project Title](#predicting-mlb-hitters-salary-in-1987-using-1986-performance-statistics)
- [Table of contents](#table-of-contents)

# Some definitions before starting
## A. What is the problem to solve?
### Informal Definition

I want to find the best single predictor for the salary of a hitter in the mlb during 1986.

### Formal definition

- **Task** (_T_): Predict the salary of a mlb player during 1986 based on his performance evaluated by 1 metric.
- **Experience** (_E_): Multiple stats belonging to each player's performance and his salary.
- **Performance** (_P_): $R^2$ score. The percentage of variance that we can explain in the dataset thanks to a single predictor

### Assumptions

- **I'm sure that there is more than one factor in game when choosing salary of a player but the purpose of this project is to create a simple linear regression model**
- The model should not be used on current players due to the boom in the mlb players salary in the last decades (and inflation of course).
- **We are only evaluating hitting data when fielding data could be another good factor**
- Are the physical qualities of players are exluded in the dataset.
- There is no data about personality, age, etc.
> *Due to the non existence of the moneyball approach during the previous century, I suspect that the batting average might be one of the best predictors but I want to test these assumptions objectively.*

The next assumptions are taking into consideration in order to check if the data is suitable for performing a Linear Regression Analysis 

- **Linear relationship:** There exists a linear relationship between the independent variable, x, and the dependent variable, y. This means that as x increases, y will also increase in a linear fashion.
- **Independence in the residuals:** In particular, this assumption ensures that there is no pattern in the residuals (errors) over time.
- **Homoscedasticity:** The residuals have constant variance at every level of the independent variable. This means that the model is not biased by outliers, which are points that lie far away from the rest of the data.
- **Normality:** The residuals of the model are normally distributed, which means that there is not a bias or they are not skewed.

## B. Why does this problem needs to be solved.

The main scope of this project is not to create a perfect model because it won't be possible due to the wide ammount of factors influencing the salary but to try to choose the best single predictor and compare performances of the model with multiple predictors.

> At the end, this is a learning project so the scope is not to achieve a 100% accuracy by tuning hyperparameters but to apply the whole process to a simple model like Simple Linear Regression. **This problem might be solved in a much better way with other models**

## C. How would I solve the problem?

> Here is an [article](https://medium.com/data-and-me/30-days-of-data-science-day-2-simple-linear-regression-5558c20ac0c3) written by me explaining how linear regression works. 

The target in our dataset is a number so this is a Linear Regression task. Like we want to get the best single predictor to a salary, we should:

- [X] Explore the dataset and check the available columns.
- [X] Check if the dataset requires or not preprocessing.
- [X] Do an exploratory data analysis on the dataset to find out if data is suitable for regression (are there visual linear trends?)
- [X] Choose the best estimator based in a correlation analysis
- [X] Prepare data for training
- [X] Train multiple simple linear regressors with different predictors
- [X] Compare performance using different regression metrics and visualizations
- [ ] Improve performance for the model that gets the best results
- [ ] Write conclusions for the project
