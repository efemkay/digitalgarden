---
{"dg-publish":true,"dg-path":"Statistics/use t test to determine if two groups have significant differences.md","permalink":"/statistics/use-t-test-to-determine-if-two-groups-have-significant-differences/","title":"use t test to determine if two groups have significant differences","tags":["PermanentNote"],"created":"2023-10-28","updated":"2023-10-28"}
---


### When to use a t test 
- #### A t test can only be used when comparing the means of two groups (a.k.a. pairwise comparison).
	- If you want to compare more than two groups, or if you want to do multiple pairwise comparisons, use an ANOVA test or a post-hoc test. 
- #### t test is a [[Areas/Statistics/choosing statistical test depends on whether predictor is quantitative or categorical\|parametric]] test of difference, meaning that it makes the same assumptions about your data as other parametric tests. The t test assumes your data: 
	- are independent 
	- are (approximately) normally distributed 
	- have a similar amount of variance within each group being compared (a.k.a. homogeneity of variance) 
- #### Iyldaid the groups come from a single population (e.g., measuring before and after an experimental treatment), perform a paired t test. This is a within-subjects design. 
	- If the groups come from two different populations (e.g., two different species, or people from two separate cities), perform a two-sample t test (a.k.a. independent t test). This is a between-subjects design. 
	- If there is one group being compared against a standard value (e.g., comparing the acidity of a liquid to a neutral pH of 7), perform a one-sample t test. 

### One-tailed or two-tailed t test? 
- #### If you want to know whether one population mean is greater than or less than the other, perform a one-tailed t test. 
	- If you only care whether the two populations are different from one another, perform a two-tailed t test. 
	- The formula for the two-sample t test (a.k.a. the Student’s t-test) is shown below. 
		- $$
		  t = \frac{\bar{x_1} - \bar{x_2}}{\sqrt{s^2( \frac{1}{n_1} - \frac{1}{n_2} )}}
		  $$

> [!info]+ One-Tailed Hypothesis Tests 
> 
> One-tailed hypothesis tests are also known as directional and one-sided tests because you can test for effects in only one direction. When you perform a one-tailed test, the entire significance level percentage goes into the extreme end of one tail of the distribution. 
> 
> In the examples below, I use an alpha of 5%. Each distribution has one shaded region of 5%. When you perform a one-tailed test, you must determine whether the critical region is in the left tail or the right tail. The test can detect an effect only in the direction that has the critical region. It has absolutely no capacity to detect an effect in the other direction. 
> 
> In a one-tailed test, you have two options for the null and alternative hypotheses, which corresponds to where you place the critical region. 
> 

- ### Youtube Videos on one-tailed t test 
	- ![Hypothesis Testing: One-tailed t test for mean](https://www.youtube.com/watch?v=fiMFqfatieE) 
	- ![One-tailed Independent Samples T-Test](https://www.youtube.com/watch?si=pMaxId4TdMs64Kcc&v=LTmWT6YGICs&feature=youtu.be) 

## References 
- [An Introduction to t Tests | Definitions, Formula and Examples (scribbr.com)](https://www.scribbr.com/statistics/t-test/) 
- [One-Tailed and Two-Tailed Hypothesis Tests Explained - Statistics By Jim](https://statisticsbyjim.com/hypothesis-testing/one-tailed-two-tailed-hypothesis-tests/)
