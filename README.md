# DSA-POWER-BI-PROJECT
This work is part of the statutory requirement for the completion of a data analysis training by Digital Skill-up Africa. We were thought quiet a lot but the training focued on SQL, Excel and PowerBI. Meanwhile, this work shows a step by step approach for the analysis of Palmora Employee data which focused on gender distributuion accros regions, salary distribution acros gender, salary gap analysis etc.
## TOPIC: PALMORA GROUP HR ANALYSIS

### PROJECT OVERVIEW

This project aim to provide insight into the Palmora Group HR data so as toi provide a reasonable conclution on the salary distribution accros gender. By analysis various parameters available to us on this data set, we want to know how salary is distributed in order to know whwether there is salary payment gap among gender. We also want to analyse the performance rating to be able to know that will give us an idea on bonus distributions based on employee performance acros department and region.

### DATA SOURCES
The data was supplied by Digital Skill-up Africa

### TOOLS USED
PowerBI for data cleaning and visualizzation [Download here](https://apps.microsoft.com/detail/9NTXR16HNW1T?hl=en-us&gl=US&ocid=pdpshare)

### DATA PREPARATION
#### Cleaning and preparation of Data

- Remove NULL Departments: Filter out rows where Department = NULL.
- Filter Active Employees: Remove rows where Salary is blank or 0 (indicates they’ve left).
- Handle Missing Genders: Replace blank or NULL Gender values with "Undisclosed.
- Ensure Salary is Numeric: change data type.

### POWER BI DATA MODEL
#### Tables used
- Employee Data: Main employee table with Gender, Salary, Department, Region, etc.
- Bonus Rules: Table with performance ratings and bonus percentages or amounts.
- 
 #### Relationships
Created a relationship between Employee Data[Rating] and Bonus Rules[Rating].

### MEASURESS (DAX)
#### Bonus Amount
Bonus Amount = IF('Employee'[Rating] > 3, 'Employee'[Salary] * 0.1, 0)VAR Rating = EmployeeData[Rating]
Total Pay (Salary + Bonus)
Total Compensation = [Bonus Amount] + EmployeeData[Salary]

### VISUALISATIONS AND INSIGHTS
#### Gender Distribution
- Pie Chart: Overall Gender distribution
- Stacked Bar Chart: Gender by Region
- Matrix Table: Gender by Department and Region
#### Rating Analysis
- Bar Chart: Average Rating by Gender
- Clustered Column Chart: Rating by Gender and Department
#### Gender Pay Gap
- Boxplot (Custom Visual): Salary by Gender
- Bar Chart: Average Salary by Gender per Region
- Treemap: Salary by Gender and Department
#### Compliance with Minimum Salary ($90,000)
- Card Visual: % of employees below $90,000
- Histogram or Bar Chart: Salary bands ($10k increments)
- Stacked Column Chart: Salary bands by Region
#### Bonus Allocation
- Table: Employee Name, Rating, Salary, Bonus, Total Compensation
- Bar Chart: Total Bonus per Region
- Card Visual: Company-wide total payout
#### Slicers
Add slicers to make the report interactive:
- Gender
- Department
- Region

### ANALYSIS 


[BI Project PDF.pdf](https://github.com/user-attachments/files/21091581/BI.Project.PDF.pdf)

