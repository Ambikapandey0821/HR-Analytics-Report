# HR-Analytics-Dashboard

### Dashboard Link : [https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection](https://app.powerbi.com/links/6zlyjcLS-q?ctid=9bb2360a-034c-4ecf-8228-aafe1a12b953&pbi_source=linkShare)

## Problem Statement

This dashboard helps the Organisation understand Employees better. It helps the Organisation know if their Employees are satisfied.
Through different factors,they get to know their improvement area, & thus they can improve by identifying these area. 
They can further work on factors responsible for Employees leaving the organisation.

Since, number of Employee leaving from medical education field is Approx. 37% and Medical is Approx. 27%. Also large Employee is leaving the employees is in the Age-Group b/w 26-35.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : 6 Card visuals were added to the canvas, representing the following details Total Employees, Employee_attrition, Average years worked in the organisation, Attrition rate, Average Salary, Average Employee Age.
- Step 5 : 1 Clustured column chart added which shows the emoloyee who left with the Age-Group
- Step 6 : 2 Filters Added. 1 filter of Department and second of Gender.In the report view, under the insert tab, using image option two images added in the Gender filter.
- Step 7 : 1 Area Chart added which shows the data of employees who left by years at company.
- Step 8 : 1 Donut Chart added which shows the data of employees who left by Education field.
- Step 9 : In the report view, under the insert tab, 1 text box was added to the canvas, in one of them name HR Analytics Dashboard.
          
- Step 10 : New measure was created to find total count of customers.

Following DAX expression was written for the same,
        
        Count of Customers = COUNT(airline_passenger_satisfaction[ID])
        
A card visual was used to represent count of customers.

![image](https://github.com/Ambikapandey0821/HR-Analytics-Report/assets/162020155/7ee5e683-ca1c-4f8f-b8b5-c071f4ef4c41)

        
 - Step 11 : New measure was created to find the Attrited Employees,
 
 Following DAX expression was written to find Employee_Attriton,
 
         Employee_Attriton = CALCULATE([Employee Count],'HR_Analytics (2)'[Attrition]="Yes")
 
 A card visual was used to represent this perecntage.
 
![image](https://github.com/Ambikapandey0821/HR-Analytics-Report/assets/162020155/5e2a87ba-5d5c-4e46-8003-173e0f956450)

 
 - Step 12 : New measure was created to calculate Average years Emoployee working in the organisation.
 
 Following DAX expression was written to find Average years Emoployee working in the organisation,
 
         Avg Years = (round(AVERAGE('HR_Analytics (2)'[YearsAtCompany]),0)&" Year")
 
![image](https://github.com/Ambikapandey0821/HR-Analytics-Report/assets/162020155/81637293-df4b-4a84-8e9b-974630b3a05c)
 
 - Step 13 : New measure was created to calculate Attrition Rate.
 
 Following DAX expression was written to find Attrition Rate,
 
         Attrition Rate = DIVIDE([Employee_Attriton],[Employee Count])
 
![image](https://github.com/Ambikapandey0821/HR-Analytics-Report/assets/162020155/a188eb87-aad8-4cff-9fa3-70782445c0d1)

 - Step 14 : New measure was created to calculate Average Salary of the all Employess.
 
 Following DAX expression was written to find Average Salary of the all Employess,
 
         Avg Salary = AVERAGE('HR_Analytics (2)'[MonthlyIncome])
 
![image](https://github.com/Ambikapandey0821/HR-Analytics-Report/assets/162020155/ec9fb8ab-2589-488e-9aa3-409fc4409b69)

 - Step 15 : New measure was created to calculate Average Age of the all Employess.
 
 Following DAX expression was written to find Average Age of the all Employess,
 
         Average Employee Age = AVERAGE('HR_Analytics (2)'[Age])
 
![image](https://github.com/Ambikapandey0821/HR-Analytics-Report/assets/162020155/a20100b1-885d-4814-b26c-a5b54f75d88d)


# Snapshot of Dashboard (Power BI Service)

![image](https://github.com/Ambikapandey0821/HR-Analytics-Report/assets/162020155/b0a482c9-987e-4f36-805e-abbebc09248e)

 
 # Report Snapshot (Power BI DESKTOP)

 
![image](https://github.com/Ambikapandey0821/HR-Analytics-Report/assets/162020155/bcf3b40e-e9c3-4aca-8c69-730c57b6edfa)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

# Total Number of Employees = 1470

 -  Number of Employees (Male) = 882 

 -  Number of Employee (Female) = 588 

 -  Number of Employees Attrited (Male) = 150 (17 %)

 - Number of Employees Attrited (Female) = 87 (14.8 %)

 Thus, higher number of Male Employees Leaving the Organisation.
           

 # Some other insights
 
 # Attrition by Years at Company
 
 - 41.4% Employee leave the company with in the less than One Year.
 
 - 35.5 % Employee leave the company in the One Year.
 
 - 20.5 % Employee leave the company in the two Year.
 
   Thus, we can see that 0-1 year has the highest attrition rate. And if employees works for 5 years then attrition rate comes to 11%.
 
 # Age Group
 
 -  32.5 % Employees leave the Organisation of '18-25' age group.
 
 -  19 % Employees leave the Organisation of '26-35' age group.
 
 -  10.6 % Employees leave the Organisation of '36-45' age group.
 
 -  15.1 % Employees leave the Organisation of '46-55' age group.

 -  19.2 % Employees leave the Organisation of '55+' age group.
 
   Thus, we can see that '18-25' Agw group has the highest attrition rate. And '36-45' Age group has the lowest Attrition rate.
         
# Education Field

- 34 % Employee leave the orgnisation from life Science Education Field.

- 29.3 % Employee leave the orgnisation from Medical Field.

- 22 % Employee leave the orgnisation from Technical Field.

- 13 % Employee leave the orgnisation from Marketing Field.

- 2.67 % Employee leave the orgnisation from Human Recources Field.
       
  Thus, we can see that 34 %  Attrition is from life Science which is the highest attrition rate. And 2.67 % Employee leave the orgnisation from Human Recources Field which is lowest.

# Job Role and Job Satisfaction

- 1 is the lowest rating and 4 is the highest rating.
- Lowest Rating has the highest Attrition rate. and Highest rating has the lowest Attrition rate.
