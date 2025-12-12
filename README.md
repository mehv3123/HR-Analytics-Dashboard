## HR - ANALYTICS DASHBOARD

## Dashboard Link :
 https://app.powerbi.com/links/QrJ7D_obcE?ctid=03cb5f0c-1f82-4993-9621-36330f6309ec&pbi_source=linkShare&bookmarkGuid=2f4a8280-e8eb-4d67-a88e-e491b6153c45
 
## Problem Statment
This dashboard helps the HR department understand their employees better. 
It provides insights into employee demographics, performance distribution, attrition trends, department-wise hiring, salary patterns, and workforce productivity.

With these insights, HR teams can identify improvement areas, manage talent more effectively, and address issues such as rising resignations, low performance, or high turnover rate.

Since the number of resignations has significantly increased over the years and the turnover rate is more than 51%, organizations must focus on employee engagement and retention strategies.

Also, the dashboard highlights performance imbalances across departments, salary variations, and gender distribution, helping HR take corrective and data-driven decisions.
 
## Steps Followed :

Step 1 : 
    Loaded multiple HR datasets into Power BI Desktop (Employee Info, Salary Info, Performance Rating, Attrition Data, Training Hours, Hiring Details)

Step 2 : 
    Opened Power Query Editor & checked column distribution, column profile, and column quality for detecting missing values or outliers.

Step 3 : 
    Performed data cleaning by removing nulls, fixing data types, and creating relationships between Employee tables.

Step 4 : 
    Calculated new columns such as Age Group and Job Role Segmentation.

    Example DAX for Age Group:

    Age Group =
        IF(Employee_Info[Age] <= 25, "Under 25",
        IF(Employee_Info[Age] <= 35, "25-35",
        IF(Employee_Info[Age] <= 45, "35-45",
        IF(Employee_Info[Age] <= 55, "45-55",
        "55+"))))


Step 5 : 
    Created measures for all key HR metrics such as:

        Total Headcount = COUNT(Employee_Info    [EmployeeID])

        Average Age = AVERAGE(Employee_Info[Age])

        Attrition Count = COUNTROWS(FILTER(Employee_Info, Employee_Info[Attrition] = "Yes"))

        Avg Tenure = AVERAGE(Employee_Info[Tenure])

        Total Hires = SUM(Employee_Info[Hires]) 


Step 6 : 
    Designed visuals for representing Gender Distribution, Department-wise Headcount, Age vs Job Role, Performance Ratings, Attrition Over Years, and New Hires.

Step 7 : 
    Added slicers for Department, Gender, Job Role, Age Group, and Year to filter insights dynamically.

Step 8 :
    Applied theme formatting for a consistent dashboard look.

Step 9 : 
    Added KPI cards showing Total Employees, Average Age, Total Attrition, Average Tenure, Hires, and Turnover Rate.

Step 10 : 
    Inserted multiple charts such as Line Chart, Pie Chart, Bar Chart, Matrix, Heatmap, and Gauge Visuals to present HR insights clearly.

Step 11 : 
    Salary distribution visuals were created using stacked bar charts for Year, Department, and Gender.

Step 12 :
    Attrition analysis was done using trend visuals showing resignations over multiple years.

Step 13 : 
    Inserted text boxes and shapes to highlight important KPIs and category titles.

Step 14 : 
    The report was optimized for Power BI Service and then published.
## Snapshot of Dashboard

Workforce Overview : 

![Dashboard Screenshot](https://github.com/user-attachments/assets/49136c59-0b96-4517-a538-0645d83ad5ae)

Performance and Attribution insights :

![Dashboard Screenshot](https://github.com/user-attachments/assets/49136c59-0b96-4517-a538-0645d83ad5ae)

Requriment and tranning :

![Dashboard Screenshot](https://github-production-user-asset-6210df.s3.amazonaws.com/168076377/525787782-bdff07aa-03e3-4a53-bf44-a66393004d79.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20251212%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20251212T082307Z&X-Amz-Expires=300&X-Amz-Signature=7ef4163023bd2021c97958d2f17f5c00d33e0b1f6c873ffbf130b49d312c31d6&X-Amz-SignedHeaders=host)


## Insights :

A multi-page HR report was created in Power BI Desktop & published to Power BI Service.
Following insights can be drawn from the dashboard:

[1] Workforce Overview

       Total Number of Employees = 2442

       Average Employee Age = 40.62

       Gender is fairly balanced across departments.

        Departments with highest employee count include Sales, HR, and Operations.


[2] Performance Insights

        High performer and low performer gauges show clear performance segmentation.

        Performance heatmap shows:

        IT, Sales, and Customer Support have stronger performance

        Some departments need targeted training and improvement plans.


[3] Attrition Insights
 
        Total Attrition = 2558

        Average Tenure = 9 years

        Resignations have increased sharply from 2018 to 2024.

        Certain job roles show a higher leaving rate, indicating workload or management issues.


[4] Hiring & Salary Analysis

        Total Hires = 5000

        Turnover Rate = 51.16%

        Salary distribution varies significantly by department.

        Salary for female employees slightly surpasses male salary in some categories due to higher representation in senior roles.

         New hires by gender:

            Males hired: 341.4M salary

            Females hired: 344.3M salary


[5] Age & Job Role Insights

        Majority of employees belong to 35–54 age group.

        Younger employees (Under 25) are fewer and need more internship/entry-level hiring programs.

        Manager, Senior Manager, and Executive roles show significant salary differences.
        
## Conclusion :
The HR Analytics Dashboard provides deep insights into the workforce including hiring patterns, performance rating, attrition behavior, salary trends, age distribution, and departmental metrics.
These insights can help HR leaders improve employee satisfaction, reduce turnover, enhance productivity, and support long-term organizational planning.
