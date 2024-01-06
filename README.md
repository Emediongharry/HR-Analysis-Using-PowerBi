# HR-Analysis-Using-PowerBi

Employee attrition refers to the rate at which employees leave a company. It impacts organizational stability, productivity, and overall performance. Analyzing attrition data provides insights to address challenges and implement strategic solutions.

The purpose of this data analysis project is to uncover patterns, trends, and influential factors related to employee attrition. Key goals include optimizing talent management, enhancing retention strategies, and improving organizational performance.

>> You can interact with the PowerBi dashboard **[here](https://www.novypro.com/project/hr-employee-attrition-visualization).**


## Skills Demonstrated
1. Exploratory data analysis
2. Data cleaning
3. DAX  query


## Data Cleaning
The following data-cleaning processes were carried out:

- Deleting redundant columns.
- Renaming the columns.
- Dropping duplicates.
- Cleaning individual columns.
- Remove the NaN values from the dataset
- Check for some more Transformations


## DAX and Measures
To calculate the total number of attrition, I wrote a DAX query to convert "Yes" to 1 and "No" to 0. The query can be seen here
```
Attrition Count = switch(true(), 'HR-Employee-Attrition'[Attrition] = "Yes", 1, 'HR-Employee-Attrition'[Attrition] = "No", 0,0)
```
After this, I found the sum of the "Attrition Count". This gave the total attrition count which is 237.

Then to find the total number of active employees, I created a measure using this query:
```
AE = SUM('HR-Employee-Attrition'[EmployeeCount]) - SUM('HR-Employee-Attrition'[Attrition Count])
```
This query subtracts the total attrition count from the total number of employees in the company. This gave us the active employee count as 1233.


## Dashboard Creation
A Power BI dashboard was developed to visually represent key insights derived from the analysis. It includes dynamic visualizations for attrition trends, departmental breakdowns, predictive insights, and other relevant metrics.

##  Insights and Recommendations:
 -**Key Insights**
Attrition is highest in certain departments, indicating a need for targeted interventions.
Employees with shorter tenures exhibit higher turnover rates.
Compensation misalignments are identified as a significant factor in attrition.
Predictive models suggest potential future attrition based on current trends.
6.2 Recommendations:
Implement targeted retention strategies in high-attrition departments.
Review and adjust compensation structures to align with industry standards.
Focus on onboarding and engagement initiatives for employees with shorter tenures.
Monitor predicted attrition trends and proactively address identified risk areas.
By addressing these insights and recommendations, the organization can strategically manage employee attrition, fostering a more stable and productive work environment.





