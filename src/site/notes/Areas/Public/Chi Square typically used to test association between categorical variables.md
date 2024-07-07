---
{"dg-publish":true,"dg-path":"Public/Chi Square typically used to test association between categorical variables.md","permalink":"/public/chi-square-typically-used-to-test-association-between-categorical-variables/","title":"Chi Square typically used to test association between categorical variables","tags":["PermanentNote"],"created":"2023-03-30","updated":"2023-03-30"}
---


- #### Chi-Square test of independence can be used to determine if there is an association between two categorical variables in a many different settings
	- Here are a few examples:
		- We want to know if gender is associated with political party preference so we survey 500 voters and record their gender and political party preference.
		- We want to know if a person’s favorite color is associated with their favorite sport so we survey 100 people and ask them about their preferences for both.
		- We want to know if education level and marital status are associated so we collect data about these two variables on a simple random sample of 50 people.
	- In each of these scenarios we want to know if two categorical variables are associated with each other.
		- In each scenario, we can use a Chi-Square test of independence to determine if there is a statistically significant association between the variables. 
- #### Null hypothesis for Chi-Square test of independence is that the variables are independent
	- **H0: (null hypothesis)** The two variables are ==independent==.
	- **H1: (alternative hypothesis)** The two variables are _not_ independent. (i.e. they are associated)

> [!info] Chi-Square Formula
> We use the following formula to calculate the Chi-Square test statistic $X^2$:
> - $X^2 = \sum(O-E)^2/E$
> - where:
> 	- **O:** observed value
> 	- **E:** expected value
> 
> If the p-value that corresponds to the test statistic X2 with (#rows-1)*(#columns-1) degrees of freedom is less than your chosen significance level then you can reject the null hypothesis.

## References
- [Chi-Square Test of Independence: Definition, Formula, and Example (statology.org)](https://www.statology.org/chi-square-test-of-independence/)

