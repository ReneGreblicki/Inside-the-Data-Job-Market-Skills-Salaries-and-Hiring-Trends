# 📊 Inside the Data Job Market: Skills, Salaries, and Hiring Trends

## 📌 Project Overview

### ❓ Which skills lead to better opportunities and higher salaries?

I used data to identify the skills, job titles, and market trends that have the largest impact on compensation. Using a dataset of real-world data job postings from **2023 to 2025**, I analysed salary patterns, geographic differences, and skill requirements to better understand what employers are looking for and how professionals can position themselves for success.

This project was completed entirely in **Excel** using:

- 🔍 Power Query
- 💪 Power Pivot
- 🧮 DAX (Data Analysis Expressions)
- 📊 PivotTables
- 📈 PivotCharts

The data comes from the [Luke Barousse's jobseeker dataset](Assets/data_jobs_salary_all.xlsx).

---

## 📂 The Final File:

The final file can be found in: [Decoding the Data Job Market.xlsx](Decoding%20the%20Data%20Job%20Market.xlsx)


## ⚙️ Setup Instructions (Important)

Please note: for the [Decoding the Data Job Market.xlsx](Decoding%20the%20Data%20Job%20Market.xlsx) file to work properly on your end, you must first access the [Luke Barousse's jobseeker dataset](Assets/data_jobs_salary_all.xlsx). You have two options:

- 📥 Option 1: Download the dataset (Assets/data_jobs_salary_all.xlsx) and store it locally on your computer
OR
- 🌐 Option 2: Connect directly to the online dataset source (if available)

Once you have access to the data, open the analysis Excel file and go to:

### Data → Get Data → Data Source Settings

From there, update the data source path to point to either your **local file location** or the **online dataset source**, depending on which option you chose.

This ensures all Power Query connections refresh correctly and the data model functions as intended.

---

## 🎯 Business Questions

To better understand the data job market, the four key questions were explored:

1. Does having more technical skills correlate with higher salaries?
2. How do salaries vary across regions?
3. Which skills appear most frequently in data-related job postings?
4. Which skills are associated with the highest salaries?

---

## 📂 Dataset

The dataset contains **tens of thousands of data-related job postings** collected between **2023 and 2025** and includes information such as:

- 👨‍💼 Job Titles
- 💰 Salary Information
- 📍 Geographic Locations
- 🛠️ Required Skills
- 🆔 Job Identifiers

The data provides a realistic view of hiring trends across the data and analytics industry.

---

## 🛠️ Tools and Techniques Used

### 📊 Excel Skills Applied

- 🔍 Power Query (ETL and Data Preparation)
- 💪 Power Pivot (Data Modelling)
- 📊 PivotTables
- 📈 PivotCharts
- 🧮 DAX (Data Analysis Expressions)

### 🧹 Data Preparation

The raw job posting dataset was imported into Power Query. To support analysis, the data was separated into two related tables:

#### 📋 data_jobs_all

Contains job-level information such as:

- 👨‍💼 Job title
- 💰 Salary
- 📍 Location

#### 🛠️ data_job_skills

Contains the skills associated with each job posting.

### 🔄 Data Transformation

Within Power Query:

- Corrected data types
- Removed unnecessary fields
- Standardised text values
- Eliminated excess whitespace
- Prepared the data for relational modelling

### 🔗 Data Modelling

Both tables were loaded into Excel and connected through a shared **job_id** field using Power Pivot.

---

# 1️⃣ Do More Skills Lead to Higher Salaries?

## 🔍 Method

The relationship between the number of skills listed in a job posting and the corresponding median salary was analysed to investigate whether broader skill requirements were associated with higher compensation.

## 💡 Key Findings

- 📈 Positions requiring a larger number of technical skills generally offered higher salaries.
- 👨‍💻 Senior-level technical roles, particularly **Data Engineers** and **Data Scientists**, showed the strongest relationship between skill breadth and compensation.
- 💼 Business Analyst roles typically required fewer technical skills and had lower median salaries compared to more specialised data positions.

## 🤔 Interpretation

The results suggest that employers place a premium on candidates who possess a diverse technical toolkit. Expanding technical competencies may increase access to higher-paying opportunities, particularly in engineering and advanced analytics roles.

## 📊 Visual

![Skills vs Salary](images/skills_vs_salary.png)

---

# 2️⃣ Salary Differences Across Regions

## 🧮 Method

Using Power Pivot and DAX, measures to calculate median salaries and compare compensation between U.S. and international markets were created.

### Example DAX Measure

```DAX
Median Salary :=
MEDIAN(data_jobs_all[salary_year_avg])
```

PivotTables connected to the data model were used to evaluate salary differences by job title and region.

## 💡 Key Findings

- 💼 Senior Data Engineers and Data Scientists consistently earned the highest salaries across both domestic and international markets.
- 🇺🇸 U.S.-based positions generally offered higher compensation than comparable international roles.
- 💰 The salary gap was most noticeable in highly technical positions.

## 🤔 Interpretation

Geographic location remains a significant factor in compensation. Professionals seeking remote or international opportunities should consider regional salary benchmarks when evaluating offers and negotiating compensation.

## 📊 Visual

![Salary by Region](images/salary_by_region.png)

---

# 3️⃣ What Skills Are Most In Demand?

## 💪 Method

Relational data model linking job postings and skills through the **job_id** field was built using Power Pivot. This allowed to aggregation of skill frequencies across thousands of postings and identifying the technologies most requested by employers.

## 💡 Key Findings

- 💻 SQL and Python appeared most frequently across data-related job postings.
- ☁️ Cloud technologies such as AWS and Azure were also highly represented.
- 📈 Technical skills consistently outweighed business productivity tools in employer demand.

## 🤔 Interpretation

The findings reinforce the importance of foundational analytical skills. SQL and Python continue to serve as core requirements across multiple data disciplines, while cloud platforms are becoming increasingly valuable as organisations scale data operations.

## 📊 Visual

![Top Skills](images/top_skills.png)

---

# 4️⃣ Which Skills Command the Highest Salaries?

## 📈 Method

To compare skill demand with compensation a combined PivotChart was created, displaying:

- 💰 Median Salary by Skill
- 👍 Skill Occurrence Rate Across Job Postings

This allowed for indentification of highly compensated and highly demanded skills.

## 💡 Key Findings

- 🐍 Python, SQL, and Oracle were associated with some of the highest median salaries.
- 🏗️ Skills linked to data engineering and database management generally produced stronger salary outcomes.
- 📉 General business software such as Microsoft Word and PowerPoint appeared less frequently and were associated with lower salaries.

## 🤔 Interpretation

Not all skills contribute equally to earning potential. Technical competencies that directly support data management, automation, and analytics appear to deliver the strongest return on investment for professionals entering or advancing within the field.

## 📊 Visual

![Skills and Salary Comparison](images/skill_salary_comparison.png)

---

# 🔑 Key Takeaways

This project revealed several important trends in the data job market:

- 📈 Broader technical skill sets are often associated with higher salaries.
- 💻 SQL and Python remain foundational skills for data professionals.
- ☁️ Cloud technologies continue to grow in importance across the industry.
- 🌍 Geographic location significantly influences compensation.
- 💰 Specialised technical skills tend to provide greater salary advantages than general business software skills.

---

# ⚠️ Limitations

Most of the dataset was collected from U.S.-based job postings, meaning international markets are underrepresented and salary trends may not fully reflect global conditions. Additionally, while the dataset is large, it represents only a subset of the overall data job market, so the findings should be viewed as indicative rather than definitive.

---

# 🏁 Conclusion

This project combined data cleaning, modelling, analysis, and visualisation techniques to explore the relationship between skills and compensation in the data job market.

By leveraging Excel's advanced analytical capabilities, I transformed raw job posting data into actionable insights about:

- 📊 Hiring trends
- 💰 Salary expectations
- 🛠️ In-demand skills

Beyond answering the original business questions, the project reinforced the value of data-driven decision-making and demonstrated how tools such as Power Query, Power Pivot, DAX, and PivotTables can be used to uncover meaningful patterns within large datasets.

For aspiring analysts, the findings provide a practical roadmap for prioritising skill development and understanding which competencies are most closely aligned with career growth and higher earning potential.
