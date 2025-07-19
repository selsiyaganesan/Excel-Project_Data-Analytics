# Excel Salary Dashboard   
![Salary_Dashboard_Final_Dashboard](https://github.com/selsiyaganesan/Excel-Project_Data-Analytics/blob/main/Project%201%20Dashboard/Screenshot%202025-07-19%20052000.png)  

## Introduction  
This data job salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.  
The data is from my Excel course which provides a foundations in analyzing data using this powerful tools. The data contains detailed information on job title, salaries, locations and essential skills that are presented here.  

## Dashboard File  
My Dashboard is in (https://github.com/selsiyaganesan/Excel-Project_Data-Analytics/blob/main/Project%201%20Dashboard.xlsx)  

## Excel Skills Used  
The following Excel skills were utilized for dashboard analysis  
- 📈Charts
- 🔢Formulas and Functions
- ✅Data validation  

## Data Jobs Datasets  
The dataset used for this project contains real-world data science job information from 2023.It includes detailed information on:  
- 👨‍💼Job titles
- 💰Salaries
- 🌎Locations
- 🛠️skills

## Dashboard Build
## 📈Charts
### Data Science job salaries-Bar Chart
![project 1 dashboard](https://github.com/selsiyaganesan/Excel-Project_Data-Analytics/blob/main/Project%201%20Dashboard/Screenshot%202025-07-19%20052032.png)
- Excel Features: Utilized bar chart features(with formatted salary values) and optimized layout for clarity.
- Design choice: Horizontal bar chart for visual comparison of median salaries.
- Design Organization: Sorted job titles by ascending salary to improve readability.
- Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than analyst roles.

## Country Median Salary-Map Chart  
![map_chart](https://github.com/selsiyaganesan/Excel-Project_Data-Analytics/blob/main/Project%201%20Dashboard/Screenshot%202025-07-19%20052323.png)  
- Excel Features: Utilized Excel's Map Chart feature to plot median salaries globally.
- Design Choice: Color-coded Map to visually differentiate salary levels across regions.
- Data Representation: Plotted median salary for each country eith available data.
- Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- Insights Gained: Enables quick grasps of global salary disparities and highlights high/low salary regions.

## Formulas and Functions  
### Median salary by Job Titles  
```
MEDIAN=(
IF(
   (jobs[job_title_short]=A2)*
   (jobs[job_country=country])*
   (ISNUMBER(SERACH(type,jobs[job_schedule_type])))*
   (jobs[salary_year_avg<>0),
   jobs[salary_year_avg]
 )
 )  
 ```
- 🔍Multi-Criteria Filtering: Checks job titles, country, schedule type, and excludes blank salaries.
- 🧮Array Formula: Utilizes MEDIAN() Function with Nested IF() statement to analyze an array.
- 🧠Tailored Insights: Provides specific salary information for job titles, regions and schedule types.
- 🔢Formula purpose: This formula populates the table below, returning the median salary based on job title, country, and type.
### Background Table  
![dashboard_table](https://github.com/selsiyaganesan/Excel-Project_Data-Analytics/blob/main/Screenshot%202025-07-19%20130104.png)  

### Dashboard Implementation   
## Data Validation  
Filtered list  
- ✅Enhanced data validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the data tab ensures:
  - 🎯The user input is restricted to predefined, validated schedule types
  - ❌Incorrect or inconsistent entries are prevented
  - 🚀Overall usability of the dashboard is enhanced.
  
![data_valid](https://github.com/selsiyaganesan/Excel-Project_Data-Analytics/blob/main/Screen%20Recording%202025-07-19%20052458.gif)
## Conclusion  
I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel dataset, I explored multiple dimensions such as job titles, salary ranges, company locations, employment types, and experience levels. The dashboard provides a visual summary of how these factors influence salary distributions in the data industry.

By applying data cleaning techniques, Excel functions, pivot tables, charts, slicers, and interactive filters, I transformed raw data into meaningful insights. This project help me strengthen my Excel and dashboarding skills while building a better understanding of compensation trends in data-focused roles.
 
 
   
