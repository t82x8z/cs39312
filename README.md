java c
Problem set 2 - EC 356
Note: You have to submit an electronic version of your homework as a PDF on blackboard on the due date. This problem set has to be typed up using a Word Processor (MS Word, Google Docs, ...), then converted to a PDF. You can insert Figures that you exported directly into a word file and copy and paste Tables from the Stata results window. Another easy way is to take screenshots of Tables and Figures and insert those into a Word document. Note that Figures  Tables are not enough, you also have to write concise explanations of your results and make sure to label the question numbers etc.
Important: Late submissions will not be accepted. Make sure you use backups and leave enough time for mishaps (scanner not working, your computer breaks, ...).
Introduction
A core part of labor economics is about empirical work to understand how labor markets work. In this problem set you will get an introduction into this kind of work. We will use data from the Current Population Survey (CPS), which is a survey conducted by the U.S. Bureau of Labor Statistics. The CPS interviews a random sample of around 50,000 households every month. This is the main datasource the federal government uses to estimate labor market indicators like the unemployment rate and job growth. For this problem set we will only use information from the month of March of each year, covering 1984 to 2010. Furthermore the dataset is restricted to single women age 16 to 44. It has around 300,000 observations. I downloaded it from the IPUMS website - https://cps.ipums.org/cps/. You can download it from blackboard. The dataset contains information on hours worked per week, whether the individual was employed last year, income last year, number of children under the age of 18 and information on education and ethnicity.
Problem 1: Estimating the intensive margin labor supply elasticity.
There is no need to submit pages and pages of Stata log files. Wherever possible, edit your results and present them neatly.
a) [5 points] Summarize all the variables in the data (no need to report the results). What is the average number of children in this data? What is the share of hispanic women in this data?
b) [5 points] In order to estimate the effect of the wage on labor supply we need a measure of the hourly wage. We will use the two variables incwage (which is yearly income) and uhrswork (hours worked per week) and define the hourly wage to be the ratio: wage = (52∗uhrswork)/incwage. Generate this variable and label it “Hourly wage”.
What is the mean and standard deviation of this variable?
How many missing values does the variable wage have? Why does it have missing values?
c) [5 points] There is a variable nKids which takes the number of children younger than age 18 and an indicator variable emp_ind which takes value 1 if women are in the labor force. Let’s start by examining how labor force participation of these women depends on the number of their children. Use the tab and sum commands and answer the following questions:
–What is the overall rate of labor force participation in the sample?
–What is the rate of labor force participation among women who have no children? What is the rate for 1 or 2 children?
–The rate of labor force participation among women with 10 children seems very high. Can you think why that may be?
d) [10 points] What is the correlation between the wage and uhrswork? Create a scatterplot of of the two variables restricting your data to t代 写EC 356 Problem Set 2Java
代做程序编程语言he year 2000.
e) [10 points] Now we will estimate the regression model:
uhrsworki = β0 + β1 × wagei + εi
Use the regress command to estimate this model. We call the estimate for β1 usually βˆ1.
–What is your estimate βˆ1?
–What is the standard error and the t-statistic for βˆ1?
–Is the coefficient βˆ1 statistically significant?
–Based on your estimate of β1 how much do the number of hours worked increase if the wage increases by $1?
–Calculate the elasticity of labor supply that is implied by your estimate of β1.
For this, use the fact that β1 =∂ wage/∂ uhrswork, and the elasticity is given as e = ∂ wage/∂ uhrswork uhrswork/wage. Calculate the elasticity using the average wage and hours worked in your sample.
f) [10 points] Usually when estimating labor supply models we use the logarithm of hours worked and the logarithm of the wage as variables and estimate the model:
log(uhrsworki) = β0 + β1 × log(wagei) + εi
In order to estimate this first generate two new variables: loghours and logwage using the ’gen’ command, by typing gen loghours = log(uhrswork) and similarly for log-wage. Regress loghours on logwage. What is your estimate of the female labor supply elasticity?
–What is your estimate βˆ1?
–What is the standard error and the t-statistic for βˆ1?
–Is the coefficient βˆ1 statistically significant?
–In class we showed that: e =∂ wage/∂ uhrswork uhrswork/wage =∂ log(wage)/∂ log(uhrswork), therefore you can view βˆ1 directly as an estimate for the elasticity of labor supply. How does this estimate compare to the elasticity you calculated in e)?
–If the wage increases by 10% by how much would you predict the number of hours to increase (in percent)?
g) [10 points] Calculate the covariance between logwage and age and the variance of log-wage. You can use the command: corr logwage age, covariance
In the table the topleft number is the variance of logwage and the bottomleft the covari-ance. Suppose that the effect of age on loghours is 0.0053. Using the omitted variable bias formula, how much do you think your estimate of the labor supply elasticity will change if you control for age?
h) [10 points] Estimate the labor supply elasticity as in f) but controlling for age. Does this line up with your calculations in g)?
i) [10 points] Re-estimate the model in part f), but now control for years of education, age and age squared (you have to create a new variable for this), year, and the ethnicity variables.
–Does the estimated labor supply elasticity stay the same as in part f)? Explain
–Comment briefly on the coefficients on the education, age, year and ethnicity vari-ables.
j) [10 points] How does the elasticity depend on whether women have children? Run the regression in i) but once restricting the sample to women with no children and once restricting the sample to women with more than one child.
Why do you think the elasticity might be different for women with and without children?
k) [5 points] Suppose you trust the estimate of e in part i), what would the tax revenue maximizing tax rate be? What would the optimal linear tax rate be if ¯g = 0.5?
l) [10 points] Come up with one omitted variable that may affect our estimate here and lead to an omitted variable bias? What is the variable? How would it be correlated with wages and hours? Would this omitted variable likely lead to a positive or negative bias for our estimated parameter βˆ1?





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
