1.Download file HR.employee_Attrition.csv from www.kaggle.com (https://www.kaggle.com/datasets/rishikeshkonapure/hr-analytics-prediction/data)

2.Import data: Home > Get data > Text/CSV 

3.Transform Data > Remove Columns (unecessary columns) > Reorder Column (in order to have the primary key as first column) > Remove Duplicates

//Decomposition tree: 

//1st version (row number): 

4.Create measure 'HC': 'COUNTA(HR_Employee_Attrition__1[EmployeeNumber])'

5.Add data to your visual > drag field "Department" and "EducationField" in "Explain by" field and 'HC' measure

//2st version (row number): 

6. Add data to your visual > drag field "Department" and "EducationField" in "Explain by" field

7. Create measure: 'tot HC': 'CALCULATE([HC], REMOVEFILTERS(HR_Employee_Attrition__1[Department], HR_Employee_Attrition__1[EducationField], HR_Employee_Attrition__1[JobRole]))'

8. Create measure 'HC %': '[HC]/[Tot HC]'

9.Drag measure 'HC %' into "Analyze" field

