# Introduction
    📊 Focusing on data analyst roles, this project explores 💰 top paying jobs, 🔥in-demand skills and 📈 where high demand meets high salary in data analytics

🔎 SQL queries? Check them out here [project_sql folder](/project_sql)

# Background

# Tools I used
For this project, key tools used includes

- **SQL:** This was the backbone of my analysis, allowing me to query the database and reveal critical insights
-**PostgreSQL:** The chosen database managemnt system, ideal for handling the job posting data.
-**Visual Studio Code:** My go-to for database managemnt and executing SQL queries
-**Git & Github:** Essential for version control and sharing mySQL scripts and analysis, ensuring collaboration and project tracking.

# The Analysis
Each query for this project aimed at investing specific aspects of the data analyst job market. 
Here's how I approached each question: 

### 1. Top Paying Data Analyst Jobs
To Identify the highest-paying roles, I filtered data analyst positions by average yealy salary ad location, focusing on remote jobs. This query highlights the high paying opportunities in the field.

```sql
SELECT 
    job_id,
    job_title,
    job_location,
    job_schedule_type,
    salary_year_avg,
    job_posted_date,
    name AS company_name
FROM 
    job_postings_fact
LEFT JOIN company_dim ON job_postings_fact.company_id = company_dim.company_id
WHERE 
    job_title_short = 'Data Analyst' AND 
    job_location = 'Anywhere' AND 
    salary_year_avg IS NOT NULL
ORDER BY 
    salary_year_avg DESC
LIMIT 10
```

# What I Learned

Throughout this nproject, I improved mySQL skills 

- **Complex Query Crafting:** Mastered the art of advanced SQL, merging tables like a pro and using WITH clauses for master level Table maneuvers
- **Data Aggregation:** Got cozy with GROUP BY and turned aggregate functions like COUNT() and AVG() into my data_summarizing sidekick
- **Analytical Thinking:** Leveled up my real-world ouzzle-solving skills, turning questions into actionable, insightful SQL queries.

# Conclusion

This project helped me to be confident in my SQL skills
