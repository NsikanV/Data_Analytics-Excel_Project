# Data_Analytics-Excel_Project
A project showcasing the Excel skills I acquired from an online Excel course

# Project 1: Excel Salary Dashboard    
 ![Data Science Salary Calculator](https://github.com/user-attachments/assets/9e470431-7542-4304-a501-955fbd574ab0)  

## Introduction  
This Excel-based Data Science Salary Dashboard was developed as part of a YouTube course tutorial to deepen my skills in Excel functions, data analysis, and dashboard design. The project offers critical insights into:  
-	📍 Median salaries across various data roles based on job type and location
-	🧭 Frequency of job postings by platform
-	🌍 Distribution and count of jobs by country and job schedule  
________________________________________
### 🛠️ Excel Skills Applied  
- 📈 Data Visualizations (Bar & Map Chart)
-	🧮 Formulas & Functions (e.g., MEDIAN(), IF(), FILTER())
-	✅ Data Validation  
________________________________________

### Dashboard File
[My final dashboard](https://github.com/NsikanV/Data_Analytics-Excel_Project/blob/main/Project_1%20Dashboard.xlsx)  

## Dataset  
Sourced from a real-world 2023 dataset curated by Luke Barousse 🎓, who made it assessable for the purpose of this course. The link to this dataset is available on his YouTube video for Excel course. This dataset includes:
-	Job titles
-	Locations 🌍
-	Average salaries 💰
-	Job types
-	Skills and so on.  
[Watch Course on YouTube](https://www.youtube.com/watch?v=pCJ15nGFgVg&t=38046s&pp=0gcJCbAJAYcqIYzv)  
________________________________________
## 📉 Dashboard Breakdown  
### Charts   
![bar chart](https://github.com/user-attachments/assets/30cdd386-e1d4-4ec1-b2eb-0263e51e846e)  
📊 A horizontal bar chart was used to visualize median salaries by role. Roles such as Data Analysts earned less compared to Senior Data Engineers and Data Scientists – an important salary stratification based on specialization and seniority.  

![Map Chart](https://github.com/user-attachments/assets/e61dcdd8-8b0c-41d4-8522-e52e3b458656)  
🗺️ This map chart highlights the geographical spread of job salaries, identifying high-paying countries and salary discrepancies across regions.  
### Formulas and Functions  
![Median Salary](https://github.com/user-attachments/assets/5ba1eb50-7888-40d0-9a7d-17ebd660a1d0)  

Median salary calculations used the `MEDIAN()` function with nested `IF()` statements and array formulas to dynamically filter and compute based on:
- Job title
- Country
-	Schedule type  
```
=MEDIAN(
IF(
(jobs[job_country]=A3)*
(jobs[salary_year_avg]<>0)*
(jobs[job_title_short]=title)*
(ISNUMBER(SEARCH(type,jobs[job_schedule_type]))),
jobs[salary_year_avg]
)
)
```

📊 Job counts by schedule type (Full-time, Part-time, etc.) were calculated using FILTER() and UNIQUE() functions to:
![job count](https://github.com/user-attachments/assets/6164a59e-601c-4ef6-8c3e-123d5616c8b2)  

-	Remove duplicates
-	Omit zero counts
-	Ensure dynamic aggregation

### Data Validation  
![Dropdown list](https://github.com/user-attachments/assets/eebcfd62-1bf9-46f4-9684-bbec4f0bfb27)  

📌 Implemented dropdown lists to:
-	Restrict user inputs
-	Maintain data consistency
-	Preserve calculation integrity

________________________________________  

# 💡 Project 2: Salary & Skill Analysis  

## Introduction  
In the advanced section of the course, I performed deeper analysis to answer the following:
-	What are the Top 10 In-Demand Skills in Data Science? 🧠
-	Do more skills = higher pay? 💼
-	How does salary vary across countries?
-	What is the median salary per top skill?
________________________________________
### 🧰 Excel Skills Used:  
-	🔄 Power Query (ETL)
-	📊 Pivot Tables & Charts
-	🧠 Power Pivot & DAX
-	🧬 Data Modeling  

[My final project](Project_2-Analysis)  
________________________________________
### ⚙️ ETL Workflow in Power Query  
![2_Project_Analysis_Screenshot3](https://github.com/user-attachments/assets/73fe6184-7654-4d08-9d9c-9c269840a17b)  

**Extract:**    
Power Query was used to extract the original data and created two queries:
1.	Complete job listings
2.	Skills per job ID  

**Transform:**  
The two queries were then transformed by:  
-	Removing irrelevant columns
-	Cleaning and splitting the skills data 
-	Trimming whitespaces and normalizing text  

**Load:**  
Finally, they were loaded into the workbook. This laid the foundation for subsequent analysis.  
________________________________________
![Top Skills](https://github.com/user-attachments/assets/b3399e4b-0f5d-4eed-82af-ec879a804755)  

This chart shows the top skills per job title. Using slicers + pivot charts, I filtered skill frequency by job title.  
**📈 Analysis:** SQL, Python, and AWS consistently ranked as top skills for high-paying roles.  

### 💸 Skills vs Salary 
Built a data model with the two queries (*data_jobs_salary_all* and *data_jobs_skills*) and created a relationship between them in Power Pivot using the job_id column   
![Power Pivot Diagram View](https://github.com/user-attachments/assets/5e43f5ca-57e4-4930-9d4a-c0cac1d0a9f8)  

Calculated the skills per job and the median salary of the various job roles using DAX. 
![Salary Vs  Skills](https://github.com/user-attachments/assets/916c460a-fe3c-4190-a08f-66de4a6c8919)  
**📈 Analysis:** A clear positive correlation – more skills often lead to higher salaries. “More skills, higher paycheck.” Employers reward versatility.  

### 📊 Skill-Based Salary Trends  
Using `CROSSFILTER()` and advanced DAX, I found median salaries tied to specific skills. With DAX I also found the skill likelihood per Data Science job roles  

![Skill Salary Analysis](https://github.com/user-attachments/assets/e9720d1a-e812-47e4-a61d-9347e09ecf35)  

**📈 Analysis:** This chart shows that SQL and Python are amongst the top paying essential skills needed by Job Seekers seeking a breakthrough in Data Science.  
________________________________________
## 🧠 Key Takeaways  
These projects were more than just dashboard exercises – they were career-guiding:  
-	🌐 Opened my eyes to Excel’s potential beyond basic functions;
-	💼 Gave me clarity on the job market landscape in Data Science;
-	💸 Informed me of salary expectations by skillset and location;
-	🔧 Strengthened my data modeling and ETL capabilities in Power Query and Power Pivot; and  
-	📈 Boosted my confidence to tackle real-world data challenges.    
________________________________________
# 🚀 Final Thoughts  
These Excel projects taught me more than just technical execution – they equipped me with actionable insights into career development, salary expectations, and in-demand skills in the Data space.
