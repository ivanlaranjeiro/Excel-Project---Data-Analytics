# Excel Project - Data Analytics

## Introduction 
As a job seeker pursuing Data Analyst positions, it’s essential to connect skill development with a clear understanding of the market I’m entering. In this project, I used Excel to identify which skills are worth learning and how they relate to salary levels. [You can access my Excel workbook here](https://github.com/user-attachments/files/32414415/PROJECT.-.DATA.ANALYTICS.xlsx)

<img width="2306" height="1357" alt="Picture 1 - Title" src="https://github.com/user-attachments/assets/ccf1ca68-43c0-4748-b889-f6cac0bd62bb" />

<img width="2091" height="1520" alt="Picture 2 - Title" src="https://github.com/user-attachments/assets/f98ed5bb-15e3-4e48-820d-c89f167710c2" />

## Questions to Analyze
To better understand the Data Job Market, I tried to answer the following questions:
1. Do more skills get you better pay?
2. What's the salary for Data Jobs in different Regions?
3. What are the top skills of Data professionals?
4. What's the pay for the top 10 skills?

## Excel Skills Used
I used, and learned, the following Excel skills for analysis:
- Pivot Tables
- Pivot Charts
- DAX (Data analysis Expressions)
- Power Query
- Power Pivot

## Data Jobs Dataset
The dataset used for this project contains real-world data science job information from January 2023 until September 2026. [The dataset is available here](https://drive.google.com/drive/folders/10s_Wl4WMrq1zvYcWqLs0QMAN0LQjvcZh). It provides a foundation for analyzing data using Excel. It includes detailed information on:

- Job Titles
- Salaries
- Locations
- Skills

## 1. Does having more skills result in better pay?
### Skill: Power Query (ETL)
**Data Extraction**  
I used Power Query to extract the original data ([data_jobs_salary_all.xlsx](https://github.com/user-attachments/files/32415026/data_jobs_salary_all.xlsx)) and create two queries:
- First one with all the data jobs information
- The second listing the skills for each job ID

**Data Transformation**  
I then transformed each query by changing column types, removing unnecessary column, cleaning text to eliminate specific words and trimming excess whitespace.  
- data_jobs_all  
<img width="244" height="312" alt="2_Project_Analysis_Screenshot1" src="https://github.com/user-attachments/assets/050ee8fb-3f9f-4558-b893-1d794313bf4e" />  

- data_jobs_skills
<img width="243" height="328" alt="2_Project_Analysis_Screenshot2" src="https://github.com/user-attachments/assets/41990668-986a-4503-8942-68a43830c3a2" />  

I then loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.  
- data_jobs_all
<img width="1916" height="649" alt="2_Project_Analysis_Screenshot3" src="https://github.com/user-attachments/assets/e7cfd167-dbb7-4849-a996-14cca0967d3d" />

- data_jobs_skills
<img width="1914" height="702" alt="2_Project_Analysis_Screenshot4" src="https://github.com/user-attachments/assets/b1f1cca9-9566-465f-bec2-dcec065615f6" />  


### Analysis 
- Senior Data Engineer and Data Scientist roles show the clearest positive link between the number of skills requested and median salary, a trend that also appears across other roles.
- Roles that requires fewer skills, like Business Analyst and Data Analst, tend to offer lower salaries. More specialized skill sets seem to command higher market values.  
<img width="874" height="537" alt="2_Project_Analysis_Chart1" src="https://github.com/user-attachments/assets/3a7a395a-c710-4075-b355-f2650fcef015" />

## 2. What's the salary for Data jobs in different regions?
### Skills: Pivot Tables & DAX  
**Pivot Table** 
- I used Power Pivot to create a Data Model that allowed me to build a PivotTable.
- Moved the job_title_short to the rows area and the salary_year_avg into de values area.
- Then I added a new measure to calculate the median salary for United States jobs.

`=Calculate(
  MEDIAN(data_jobs_all[salary_year_avg]),
  data_jobs_all[job_country] = "United States")`  

**DAX**
- To calculate the median year salary I used DAX.  
`Median Salary := MEDIAN(data_jobs_all[salary_year_avg])`  
### Analysis 




