# HR Analytics Dashboard - Power BI

## Overview
This Power BI dashboard provides key HR analytics insights, allowing users to explore workforce trends, employee demographics, and performance metrics. The interactive dashboard helps HR teams make data-driven decisions to optimize workforce planning and management.

![Screenshot HR Dashboard](https://github.com/amgfigueiredo/Power-BI-Dashboards/blob/3b19ff1d6819d7e022ebcddf15640d14f5ad5873/Human-Resources/PowerBI_HR_Dashboard.gif)



## Features

- Employee Demographics Analysis: Gender distribution, age groups, and department-wise breakdown.

- Attrition Analysis: Identify patterns and factors influencing employee attrition.

- Performance Metrics: Insights into employee performance and productivity.

- Salary Distribution: Visualizations of compensation trends across departments and roles.

- Interactive Filtering: Users can apply dynamic filters to customize the dashboard view.

## Technologies Used

- **Power BI:** Data visualization and dashboard creation.

- **DAX (Data Analysis Expressions):** Custom calculations and measures.

- **Excel/CSV:** Data sources for employee records and HR metrics.

## Datasets Used

- **Employee Information Dataset**: Contains employee details such as name, department, gender, age, salary, and tenure.

- **Performance Ratings Dataset:** Data on employee performance scores and promotions.

## Key DAX Functions Used

`Total Emp = COUNTROWS('HR Analytics Data')`

`Male = CALCULATE([Total Emp],'HR Analytics Data'[Gender]="male")`

`Female = CALCULATE([Total Emp],'HR Analytics Data'[Gender]="female")`

`% male=DIVIDE([Male],[Total Emp],0)`

`% female = DIVIDE([Female],[Total Emp],0)`

`Due for promotion = if(ISBLANK(CALCULATE([Total Emp],'HR Analytics Data'[Promotion Status]="Due for promotion")),0,CALCULATE([Total Emp],'HR Analytics Data'[Promotion Status]="Due for promotion"))`

`Not due = CALCULATE([Total Emp],'HR Analytics Data'[Promotion Status]="Not due")`

`% not due = DIVIDE([Not due],[Total Emp],0)`

`% due promotion = DIVIDE([Due for promotion],[Total Emp],0)`

`On Service = if(ISBLANK(CALCULATE([Total Emp],'HR Analytics Data'[Retreanchment statuts]="on services")),0,CALCULATE([Total Emp],'HR Analytics Data'[Retrenchment statuts]="on services"))`

`% on service = DIVIDE([On Service],[Total Emp],0)`

`Will be retrenched = if(ISBLANK(CALCULATE([Total Emp],'HR Analytics Data'[Retrenchment statuts]="Will be retrenched")),0,CALCULATE([Total Emp],'HR Analytics Data'[Retrenchment statuts]="Will be retrenched"))`

`% on service = DIVIDE([On Service],[Total Emp],0)`

# Step-by-Step Guide

## 1. Data Preparation

- Load datasets into Power BI from Excel/CSV files or SQL database.

- Clean and transform data using Power Query.

- Create relationships between tables for seamless data integration.

## 2. Building the Data Model

- Define relationships between employee, attrition, and performance tables.

- Create calculated columns and measures using DAX.

## 3. Designing the Dashboard

- Add visual elements such as bar charts, line graphs, and pie charts.

- Implement slicers for interactive filtering.

- Format visuals for better readability and user experience.

## 4. Implementing DAX Measures

- Write DAX formulas for key metrics (e.g., attrition rate, average salary, headcount trends).

- Validate calculations to ensure accuracy.

## 5. Publishing and Sharing

- Publish the Power BI dashboard to Power BI Service.

- Embed reports into organizational portals if needed.

## How to Use

- Clone this repository.

- Open the Power BI (.pbix) file.

- Ensure datasets are connected properly.

- Explore the visualizations and interact with filters.

## Contributing

If you’d like to contribute, feel free to fork the repository and submit pull requests with improvements.

