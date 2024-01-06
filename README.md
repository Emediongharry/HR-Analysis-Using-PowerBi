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
In order to calculate the total number of attrition, I wrote a DAX query to convert "Yes" to 1 and "No" to 0. The query can be seen here

'''
Attrition Count = switch(true(), 'HR-Employee-Attrition'[Attrition] = "Yes", 1, 'HR-Employee-Attrition'[Attrition] = "No", 0,0)
'''

After this, I found the sum of the "Attrition Count". This gave the total attrition count which is 237.

Then to find the total number of active employees I created a measure using this query:

'''
AE = SUM('HR-Employee-Attrition'[EmployeeCount]) - SUM('HR-Employee-Attrition'[Attrition Count])
'''

This query subtracts the total attrition count from the total number of employees in the company. This gave us the active employee count as 1233.

