# Project 2 Analysis  
## Introduction  
I've always been surprised by the lack of data exploring the most optical jobs and skills in the data science market. I set out to understand what skills top employers request and how to land more pay.
### Questions to Analyze  
To understand the data science job market, I asked the following:

 1.Do more skills get better pay?  
 
 2.What's the salary for data jobs in different regions?  
 
 3.What are the top skills of data professionals?  
 
 4.What's the pay for the top 10 skills?
 ## Excel Skills Used
 The following Excel skills were utilized for analysis:
 - 📊Pivot Tables
 - 📚Pivot Charts
 - 🧮DAX(Data Analysis Expressions)
 - 🔁Power Query
 - 📝Power Pivot

## Data Jobs Dataset
The dataset used for this project contains real-world data science job information from 2023.

It includes detailed information on:
- 👩‍💻Job Titles
- 📍Job Locations
- 💸Salaries
- 👥Skills

## 1️⃣. Do more skills get you better pay?

### Skill:Power Query(ETL)

*♻️Extract*
- I first used Power Query to extract the original data (data_salary_all.xlsx)and create two queries:
  - First one with all the data jobs information.
  - The second listing the skills for each job ID.

*🔄Transform*
- Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.
 - data_jobs_all
<img width="313" height="351" alt="Screenshot 2025-07-19 213428" src="https://github.com/user-attachments/assets/d00c22a6-0907-43a1-9398-549fb0fe890d" />

 - data_job_skills
<img width="301" height="307" alt="Screenshot 2025-07-19 214536" src="https://github.com/user-attachments/assets/b925b9b4-d296-4c3e-9631-27162fd156d3" />

*📥Load*
- Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.
 - data_jobs_all
  
<img width="1904" height="817" alt="Screenshot 2025-07-19 214713" src="https://github.com/user-attachments/assets/712e384f-8091-4750-a53c-8e9f91fbe097" />  

 - data_jobs_skills
   
<img width="1911" height="818" alt="Screenshot 2025-07-19 214834" src="https://github.com/user-attachments/assets/6c881627-c7d5-43dc-8bc1-852b37fb75ad" />


### Analysis

*Insights*
- There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like Senior Data Engineer and Data Scientist.

  - Roles that require fewer skills, like Business Analyst, tend to offer lower salaries, suggesting that more specialized skill sets command higher market value.
<img width="649" height="359" alt="Screenshot 2025-07-19 065155" src="https://github.com/user-attachments/assets/ca4802b3-dde8-4f64-80f1-75c69ebac623" />

## 2️⃣.What's the salary for data jobs in different regions?   

### Skills:Pivot Tables & DAX
### 📊Pivot Table
- I created a Pivot Table using the Data Model I created with Power Pivot.
- I moved the job_title_short to the row area and salary_year_avg into the values area.
- Then I added new measures to calculate the median salary for United States jobs.
```
=CALCULATE(
    MEDIAN(data_jobs[salary_year_avg]),
    data_jobs_all[job_country] = "United States")
```
### 🧮DAX
- To calculate the median year salary I used DAX.
  
`Median Salary:=MEDIAN(data_jobs_all[salary_year_avg])`
### Analysis
*Insights*
- Job roles like Senior Data Engineer and Data Scientist command higher median salaries both in US and internationally, showing the global demand for high-level data expertise.
- The salary disparity between US and Non-US roles is particularly notable in high-tech jobs, which might be influenced by the concentration of tech industries in the US.
<img width="620" height="283" alt="Screenshot 2025-07-19 065518" src="https://github.com/user-attachments/assets/a1316870-680b-466a-806a-ec5b1dc57863" />

### So What
- These salary insights are important for planning and salary negotiations, helping professionals and companies align their offers with market standards with considering geographical variations.

## 3️⃣.What are the top skills of data professionals?

### Skill:Power Pivot

*📝Power Pivot*
- I created a data model by integrating the data_jobs_all and data_jobs_skills tables into one model.
- Since I had already cleaned the data using Power Query;Power Pivot created a relationship between these two tables.

*🧱Data Model*
- I created a relationship between my two tables using the job_id_column.
### Analysis
*Insights*

🔗 Linked data tables using job_id helped create a unified view of job roles and their corresponding skills.

🧠 Power Pivot's data model enabled smarter and more dynamic cross-table analysis.

🛠️ Allowed for efficient use of DAX functions to perform advanced calculations and aggregations.

🚀 Improved data performance and made it easier to generate deep, skill-based insights for each job role.

<img width="849" height="648" alt="Screenshot 2025-07-19 221623" src="https://github.com/user-attachments/assets/7fd8f79b-bbc8-4156-84f8-d26d458030c0" />

### So What
- Understanding prevalent skills in the industry not only helps professionals stay competitive but also guides training and educational programs to focus on the most impactful technologies.
<img width="596" height="360" alt="Screenshot 2025-07-19 065239" src="https://github.com/user-attachments/assets/fa18cca0-81bc-4259-a39d-171132cb7fae" />

## 4️⃣.What's the pay of the top 10 skills?

### Skill: Advanced Charts(Pivot Chart)
*📚PivotChart*
- I created a combo PivotChart to plot median salary and skill likelihood(%)from my PivotTable.
   - Primary Axis: Median Salary (as a clustered column)
   - Secondary Axis: Skill Likelihood (as a line with markers)
- To customize the chart, I added a title axis title, removed the lines (skill likelihood), and changed the markers to diamonds.
### Analysis

*Insights*  
- 💼 Skills with higher likelihood percentages tend to align with moderate salary ranges, suggesting they are more common and in demand across multiple roles.

- 💸 Higher median salaries are often linked to niche or specialized skills, which appear less frequently (lower likelihood %) in the dataset.

- 📈 The combo chart effectively highlights this inverse relationship, helping distinguish between highly sought-after vs. highly paid skills.

- 🔍 The diamond markers on the line chart make it easier to track skill likelihood trends across different salary levels.
  
<img width="596" height="355" alt="Screenshot 2025-07-19 065339" src="https://github.com/user-attachments/assets/894343f3-4552-48d7-b23a-62c284865a40" />

### So What
- This Chart highlights the importance of investing time in learning high-value skills like Python and SQL, which are evidently tied to higher paying roles, especially for those looking to maximize their salary in the tech industry.

## Conclusion
In this project, I analyzed job market data using Pivot Tables, Power Query, and Power Pivot in Excel. I cleaned and transformed the dataset, then summarized it to find key insights like job skill counts, averages, and medians. These tools helped me efficiently model and explore the data. The analysis highlights the most in-demand job skills and supports data-driven decision-making. This project strengthened my skills in Excel-based data analysis and business intelligence.



   
