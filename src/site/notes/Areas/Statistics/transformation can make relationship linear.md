---
{"dg-publish":true,"dg-path":"Statistics/transformation can make relationship linear.md","permalink":"/statistics/transformation-can-make-relationship-linear/","tags":["LiteratureNote"],"created":"2022-05-09","updated":"2022-05-09"}
---


- #### some relationship can be made linear by an appropriate transformation of the data
	- common transformation include the log, square root and reciprocal
	- sometimes there are mathematical justification for choosing a transformation, while some other times we simply use trial and error
- #### we can transform the response variable ($\hat y$), the explanatory variable or both
	- typically, it is the response variable that is transformed
		- as we can have multiple explanatory/independent variable, it’s difficult to tell which x variable to transform
	- [[Projects/Accuracy of Heuristics/residual plot for linear regression\|residual plot]] can help to visualise if there’s a need to transform the data
		- a visible trend (either upward/downward or curved) on the residuals indicate the relationship is not linear
- #### square root transformation is less strong than log transformation
	- if using log transformation the data correction seems to be overcooked, you may try square root
	- **other common transformations**
		- $x^2$ to correct upward curve line
		- $1/x$ to correct downward curve line
		- $log(x)$ to correct tapering convex
		- $\sqrt x$ to correct a weaker tapering convex
	- example charts
		- log(x) and sqrt(x)
			```chart
			type: line
			labels: [1,10,20,30,40]
			series:
			  - title: log(x)
				data: [0,2.303,2.996,3.401,3.689]
			  - title: sqrt(x)
				data: [1,3.162,4.472,5.477,6.325]
			spanGaps: true
			tension: 0.3
			width: 80%
			beginAtZero: true
			```
		- 1/x
			```chart
			type: line
			labels: [1,2,3,4,5]
			series:
			  - title: 1/(x)
			    data: [1,0.500,0.333,0.250,0.200]
			spanGaps: true
			tension: 0.3
			width: 80%
			beginAtZero: true
			```
		- x^2
			```chart
			type: line
			labels: [1,2,3,4,5]
			series:
			  - title: x^2
			    data: [1,4,9,16,25]
			spanGaps: true
			tension: 0.3
			width: 80%
			beginAtZero: true
			```
	- pictures
		- ![Pasted image 20220509165442.png](/img/user/Areas/General/Pasted%20image%2020220509165442.png)
		- ![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/81/Logarithm_plots.png/450px-Logarithm_plots.png)
		- ![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4a/Square_root_0_25.svg/600px-Square_root_0_25.svg.png)
- alternatively, we can find the best transformation using [[Areas/Public/Box-Cox function help find best transformation to normalise variable\|Box-Cox function help find best transformation to normalise variable]]

## References
- [Simple Linear Regression: Transformations - YouTube](https://www.youtube.com/watch?v=HIcqQhn3vSM)
- [Introduction to Regression: Transformations - YouTube](https://www.youtube.com/watch?v=8461OtzimhA)