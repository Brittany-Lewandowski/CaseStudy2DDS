# Executive Summary

DDSAnalytics is looking to leverage data science to help their Fortune500 clients with talent management. Before DDSAnalytics pursues this initiative, the company wants to verify that data science can provide valuable and trusted insights. Consequently, DDSAnalytics has tasked their employee, Brittany Lewandowski, to use an Attrition data set for their client Frito Lay to:

1.	Identify job role specific trends in the data set.
2.	Identify the top 3 factors that contribute to turnover.
3.	Create a classification model for Attrition that attains model metrics of 60% sensitivity and 60% specificity.
4.	Create a linear regression model for Monthly Income with an RMSE <$3000.

With the requirements above, Brittany began by analyzing the Attrition data set for job role specific trends. Using R and RStudio Brittany found the following insights:

1.	In descending order, Job Roles with the highest attrition are: Sales Executives (33), Research Scientists (32), and Laboratory Technicians (30). Job roles with the lowest attrition are: Research Directors (1), Manufacturing Directors (2), and Managers (4).
2.	Job Roles of Sales Executives, Research Scientists and Laboratory Technicians account for roughly 60% of the data set. As a result, it is not a surprise that these Job Roles have both the highest values for attrition. Conversely, Research Directors account for the fewest employees, therefore I am not surprised to see that they have the lowest Attrition volume. 
3.	Not considering the Job Roles of Sales Executives, Research Scientists, and Laboratory Technicians, we should investigate attrition seen in the Job Roles of Healthcare Representatives, Managers, and Sales Representatives as the number of employees in these roles are more closely related. 
4.	Sales Executives have the highest job satisfaction followed by Research Scientists and Laboratory Technicians. Human Resource employees, Managers and Research Directors all have the lowest job satisfaction. 
5.	Job satisfaction does not appear to have a positive relationship to whether or not an employee churns. For example, the lowest churning job roles, (Research Directors, Manufacturing Directors and Managers), all have low reported job satisfaction levels. Conversely the highest churning roles, (Sales Executives, Research Scientists, and Laboratory Technicians), all have the highest reported job satisfaction levels.
6.	Managers make the highest median income, followed by Research Directors and Manufacturing Directors. Conversely, Human Resource employees make the lowest median income, followed by Laboratory Technicians and Sales Representatives. 
7.	The highest churning job roles, (Sales Executive, Research Scientists and Laboratory Technicians), have mostly worked at Frito Lay for a year. 
8.	Employees that are in the age group of 28-33 tend to churn more than other employees. 
9.	There does not appear to be a positive correlation between Years Since Last Promotion and employees that have churned. (As the number of years since an employee has received a promotion increases, churn does not increase linearly.)


After performing her initial exploratory data analysis, Brittany built a Naïve Bayes classifier for Attrition. In the process of building this classifier Brittany noticed that the “Attrition” column was imbalanced with 730 “No” values and 140 “Yes” values. This imbalance negatively impacted model metrics therefore Brittany up sampled the column to balance the data. Once the data was up sampled, there were 584 “No” and “Yes” values and Brittany was able to proceed with her analysis. 

With the up sampled data, Brittany used feature selection to identify the top 3 variables that contribute to Attrition. The results showed that columns “Age,” “JobRole,” and “YearsAtCompany” were the most significant. These variables were included as explanatory variables in the classifier. Next, Brittany ran the classifier and achieved the following model metrics:

1.	100% model accuracy 
2.	100% model specificity
3.	100% model sensitivity

To conclude her project, Brittany built a linear regression model predicting an employee’s monthly income. Up sampling was not necessary as each observation of monthly income is unique. As a result, Brittany used the original Attrition data set to predict Monthly Income.

Again, using feature selection, Brittany identified that the top 3 variables influencing Monthly Income are: “YearsAtCompany,” JobRole,” and “Age.” After running the model, the following model metrics were achieved:

1.	Adjusted R-Squared: 0.8358
2.	RMSE: 1694.557

Upon completing this analysis Brittany has provided the following 3 recommendations for Frito Lay:
1.	Increase the annual salary of Laboratory Technicians as they have a high attrition rate and a low yearly salary. 
2.	Consider implementing employee retention programs that foster a culture of belonging. These programs can organize events such as Top Golf outings and happy      hours to strengthen the comradery amongst employees. 
4.	Avoid promoting employees as a retention mechanism. The data shows a negative relationship exists between years since last promotion and attrition.

#Introduction

Brittany Lewandowski, an employee of DDSAnalytics, was provided with an Attrition data set for client, Frito Lay. Brittany was then asked to leverage data science to identify insights within the data set that will help Frito Lay retain their talent.

Specifically, Brittany was asked to:
1.	Identify job role specific trends in the data set.
2.	Identify the top 3 factors that contribute to turnover.
3.	Create a classification model for Attrition that attains model metrics of 60% sensitivity and 60% specificity.
4.	Create a linear regression model for Monthly Income with an RMSE <$3000.

Using RStudio, Brittany completed this analysis. Answers to the above questions of interest, along with the R code Brittany wrote are included in this repository. The PowerPoint presentation given to CEO of Frito Lay, Professor Lindsey, and the CFO of Frito Lay is included as well. The RMarkdown file contains comments explaining each piece of code and was annotated with reproducibility in mind. Should you have any questions about this analysis, please contact Brittany Lewandowski at: blewandowski@smu.edu

#Conclusion

Upon analyzing Frito Lay’s attrition data set, Brittany determined: 
1.	Job Roles with the highest attrition are: Sales Executives, Research Scientists, and Laboratory Technicians.
2.	Job roles with the lowest attrition are: Research Directors, Manufacturing Directors, and Managers.
3.	Naïve Bayes classified attrition with an accuracy of 100%.
4.	Linear Regression model predicted monthly income with an RMSE of 1694. 

#Extending This Research

This analysis was time constrained and was completed in two weeks. With this in mind, research can be extended on this project in the following ways:

1.	Performing cross validation on both the up sampled and original data sets to refine the models in this deliverable.
2.	Testing the models in this deliverable with updated attrition data to view model performance. 
3.	Tuning the models. 

