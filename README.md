# HR-Analysis-Using-PowerBi

Employee attrition refers to the rate at which employees leave a company. It impacts organizational stability, productivity, and overall performance. Analyzing attrition data provides insights to address challenges and implement strategic solutions.

The purpose of this data analysis project is to uncover patterns, trends, and influential factors related to employee attrition. Key goals include optimizing talent management, enhancing retention strategies, and improving organizational performance.

>> You can interact with the PowerBi dashboard **[here](https://www.novypro.com/project/hr-employee-attrition-visualization).**

<iframe title="HR-Attrition MeriSkill" width="600" height="373.5" src="https://app.powerbi.com/view?r=eyJrIjoiMDEwOWE3MTAtN2UwYi00MjNlLWI5NDItYzZmOGY0ZmI0Y2NhIiwidCI6IjY0MjBkMTZmLWNmNTctNGZmMC04NjM4LTI2MjkyMDM0MDU4NyJ9&embedImagePlaceholder=true" frameborder="0" allowFullScreen="true"></iframe>

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
1. There are more males than females in the company. Hence attrition is higher in males compared to females.
2. The overall attrition rate of the company is 16.12%.
3. Attrition is highest in the sales department with a total of 20.63%, closely followed by the human resource department with a total of 19.05%.
4. Employees with shorter tenures exhibit higher turnover rates. This observation suggests that the rate at which employees leave the organization is more pronounced among those who have recently joined. High turnover among employees with shorter tenures may indicate various factors such as dissatisfaction, mismatch of expectations, or challenges in adapting to the organizational culture.
5. There is a negative correlation between performance rating and employee attrition. Employees with low-performance ratings were more likely to leave the company compared to employees with high-performance ratings.
6. There was a high turnover rate for employees who were very dissatisfied with the environment.

<br>

   -**Recommendations**
1. Focus on onboarding and engagement initiatives for employees with shorter tenures.
2. Conduct exit interviews for employees who have left the company to identify common reasons for their departure. This interview can be conducted anonymously approximately 2 weeks after an employee's exit.
3. Come up with strategies to improve the performance rating of employees. This might make them feel productive enough to remain in the company
4. Identify a way to measure how employee training programs contribute to attrition in the company.
5. To improve the company's work environment, plans can be made to foster an inclusive and diverse workplace where all employees feel valued and respected, provide Employee Assistance Programs that offer support for personal challenges or crises, organize team-building activities and events to foster a sense of camaraderie among employees and implement wellness programs that focus on physical and mental health.

By addressing these insights and recommendations, the organization can strategically manage employee attrition, fostering a more stable and productive work environment.





