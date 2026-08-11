HR Analytics Dashboard — Recruitment, Workforce & Performance

What does the current workforce look like by department, gender, education, employment type, and work arrangement?
Which recruitment channels contribute the most employees?
Which previous employers are represented in the workforce?
How are employees distributed across performance ratings?
How does performance relate to promotion activity, tenure, and bonus?
What is the current attrition level?
Which HR metrics could be monitored by management?
Key KPIs
Total Employees: 120
Active Employees: 96
Attrition Rate: 20%
Average Salary — Active Employees: 4.52K AZN
Average Engagement — Active Employees: 7.28 / 10
Average Job Satisfaction — Active Employees: 6.84 / 10
Average Absenteeism Rate: 6.08%
Total Promotions: 239
Average Total Compensation: 65.76K AZN
Dashboard Pages
1. Overview
Executive snapshot of workforce size, active headcount, attrition, salary, engagement, satisfaction, recruitment source, absenteeism, department headcount, and gender mix.
2. Recruitment & Workforce Analysis
Analysis of:
Recruitment source
Previous employer
Education level
Employment type
Office / Remote / Hybrid distribution
3. Performance Analysis
Analysis of:
Performance rating distribution
Promotion count by performance rating
Performance by department
Average bonus by performance rating
Role tenure by performance rating
Compensation indicators
4. Attrition Analysis
Designed to investigate employee turnover and identify potential patterns across employee characteristics and HR indicators.
Main Findings
Agency is the largest recruitment source in the dataset with 27 employees.
Operations has the largest department headcount with 20 employees.
Engineering follows with 18 employees.
MBA is the most common education level with 32 employees.
Full-time employees represent the largest employment type group with 83 employees.
Hybrid is the most common work arrangement with 47 employees.
Meets Expectations is the largest performance category with 51 employees.
The overall attrition rate is 20%, with 24 inactive employees out of 120.
Tools & Skills
Power BI
Power Query
DAX
Data Cleaning & Transformation
Data Modeling
KPI Design
HR / People Analytics
Data Visualization
Business Insight & Recommendation
Data Preparation
Typical transformation steps included:
Data type validation
Date field standardization
Missing-value review
KPI preparation
Active/inactive employee segmentation
Aggregation by department, recruitment source, performance, and work arrangement
DAX measures for dashboard KPIs
Suggested DAX Measures
```DAX
Total Employees = COUNTROWS(EmployeeData)

Active Employees =
CALCULATE(
    [Total Employees],
    EmployeeData[Active Status] = "Active"
)

Attrition Rate =
DIVIDE(
    CALCULATE([Total Employees], EmployeeData[Active Status] = "Inactive"),
    [Total Employees]
)

Average Salary =
CALCULATE(
    AVERAGE(EmployeeData[Base Salary (AZN)]),
    EmployeeData[Active Status] = "Active"
)

Average Engagement =
CALCULATE(
    AVERAGE(EmployeeData[Engagement Score (1-10)]),
    EmployeeData[Active Status] = "Active"
)

Average Job Satisfaction =
CALCULATE(
    AVERAGE(EmployeeData[Job Satisfaction Score (1-10)]),
    EmployeeData[Active Status] = "Active"
)
```
