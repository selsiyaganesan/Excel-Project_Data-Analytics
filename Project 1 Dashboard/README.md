# Excel Salary Dashboard   
![Screen Recording 2025-07-20 162149](https://github.com/user-attachments/assets/d075b446-409d-4cd4-ac58-dddda664cdbd)



## Introduction  
This data job salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.  
The data is from my Excel course which provides a foundations in analyzing data using this powerful tools. The data contains detailed information on job title, salaries, locations and essential skills that are presented here.  

## Dashboard File  
My Dashboard is in [Excel Dashboard Project 1.xlsx](https://github.com/user-attachments/files/21334457/Excel.Dashboard.Project.1.xlsx)


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
<img width="461" height="506" alt="Screenshot 2025-07-19 052032" src="https://github.com/user-attachments/assets/6ee81eb2-9177-458c-8048-690411529c7b" />
  
- Excel Features: Utilized bar chart features(with formatted salary values) and optimized layout for clarity.
- Design choice: Horizontal bar chart for visual comparison of median salaries.
- Design Organization: Sorted job titles by ascending salary to improve readability.
- Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than analyst roles.

## Country Median Salary-Map Chart  
<img width="502" height="495" alt="salary dash 4" src="https://github.com/user-attachments/assets/3005ebb9-fe2c-4bec-ad46-2e411ec798b4" />  

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
<img width="315" height="264" alt="Screenshot 2025-07-19 130104" src="https://github.com/user-attachments/assets/9807e4a4-6a10-4205-8dd0-49bea431d8c6" />

### Dashboard Implementation   
## Data Validation  
Filtered list  
- ✅Enhanced data validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the data tab ensures:
  - 🎯The user input is restricted to predefined, validated schedule types
  - ❌Incorrect or inconsistent entries are prevented
  - 🚀Overall usability of the dashboard is enhanced.
  
![Screen Recording 2025-07-20 161044](https://github.com/user-attachments/assets/d9fa4578-c972-4cbf-84b1-3fa0f852556e)


  
## Conclusion  
I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel dataset, I explored multiple dimensions such as job titles, salary ranges, company locations, employment types, and experience levels. The dashboard provides a visual summary of how these factors influence salary distributions in the data industry.

By applying data cleaning techniques, Excel functions, pivot tables, charts, slicers, and interactive filters, I transformed raw data into meaningful insights. This project help me strengthen my Excel and dashboarding skills while building a better understanding of compensation trends in data-focused roles.
 
 
   
