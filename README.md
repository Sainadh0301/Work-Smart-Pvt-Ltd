# Work Smart Pvt Ltd Laziness Index Analysis – Power BI Dashboard

## 📌 Project Overview
WorkSmart Pvt Ltd wanted to understand employee productivity patterns and identify signs of workplace laziness across departments and work modes. This project analyzes **200 employee activity records** collected over one month to calculate a custom **Laziness Index**, classify employees into productivity categories, and surface actionable insights for HR intervention.

As a Data Analyst, I built an end-to-end Power BI dashboard covering data cleaning, DAX-based KPI modeling, and interactive visual analysis.

---

## 🏢 Business Problem
WorkSmart currently has employee activity data but lacks a centralized analytical solution for understanding productivity.

HR management needs answers to questions such as:

Which department has the highest average Laziness Index?
Are WFH employees more likely to fall into the High Laziness category?
Does salary level have any relationship with productivity?
Is excessive social-media usage associated with missed deadlines?
Which employees demonstrate the strongest productivity?
Does meeting attendance affect task completion?
Which departments should HR prioritize for intervention?

The challenge is to move from raw employee activity data → meaningful insights → actionable HR decisions.

---

## 📊 Dataset
**Records:** 200 employees | **Frequency:** Weekly activity summary

| Column | Description |
|---|---|
| Employee_ID | Unique ID (EMP001–EMP200) |
| Department | HR, Sales, IT, Finance, Marketing |
| Work_Mode | WFH / Office |
| Login_Hours | Total login hours per week |
| Active_Work_Hours | Actual productive hours |
| Idle_Time_Hours | System idle hours |
| Break_Time_Hours | Break duration |
| Tasks_Assigned | Number of tasks assigned |
| Tasks_Completed | Number of tasks completed |
| Deadline_Missed | Yes / No |
| Meetings_Attended | Count of meetings |
| Social_Media_Usage_Hours | Hours spent on non-work browsing |
| Performance_Rating | 1 to 5 |
| Salary_Level | Low / Medium / High |

**Data characteristics (realistic twist):**
- 10 employees with extremely high social media usage
- 15 employees with a perfect task completion rate
- 5 employees with zero missed deadlines

---

## 🧮 Business Definition: Laziness Index

```
Laziness Index = (Idle Time + Break Time + Social Media Usage) / Login Hours
```

| Index Range | Category |
|---|---|
| < 0.25 | Productive |
| 0.25 – 0.40 | Moderate |
| > 0.40 | High Laziness |

---

## 🛠️ Tech Stack

| Technology             | Purpose                        |
| ---------------------- | ------------------------------ |
| **Power BI**           | Dashboard & visualization      |
| **Power Query**        | Data cleaning & transformation |
| **DAX**                | Measures & calculated columns  |
| **Excel / CSV**        | Dataset                        |
| **GitHub**             | Version control & portfolio    |
| **Data Visualization** | Business storytelling          |


---

**🧹 Data Preparation**

The dataset was prepared using Power Query.

**Data cleaning steps**

Removed unnecessary spaces.

Standardized column names.

Verified Employee IDs.

Checked duplicate records.

Corrected data types.

Converted numerical fields to appropriate numeric types.

Standardized categorical values.

Validated Yes/No deadline values.

Checked missing values.

Verified task counts.

Validated Laziness Index values.

---

## ⚙️ Part 1: Data Modeling

**Steps performed:**
1. Imported the 200-record dataset into Power BI
2. Cleaned and standardized column names
3. Created calculated columns:
   - `Task Completion %`
   - `Laziness Index`
   - `Productivity Category`

---

## 📈 Dashboard Components

**1. KPI Cards**

- Total Employees
- Avg Laziness Index
- Avg Completion %
- High Laziness Employees

**2. Bar Chart** – Laziness Index by Department

**3. Stacked Column Chart** – Work Mode vs Productivity Category

**4. Pie Chart** – Productivity Category Distribution

**5. Scatter Plot** – Login Hours vs Tasks Completed (bubble size = Social Media Usage)

**6. Table** – Top 10 Most Lazy Employees

**7. Slicers**
- Department
- Work Mode
- Salary Level

---

## 🚀 Advanced Features

Dynamic dashboard titles
Conditional formatting
Employee drillthrough
Decomposition Tree
What-If analysis
Interactive slicers
Executive-level KPI reporting

---

## ❓ Analytical Questions Answered
1. Which department has the highest average laziness?
2. Is WFH more associated with laziness than working from office?
3. Does salary level impact productivity?
4. What is the relationship between social media usage and missed deadlines?
5. Who are the top 5 most productive employees?
6. Is meeting attendance affecting task completion?
7. Which department needs HR intervention the most?

---

**💡 Business Insights**

The dashboard is designed to identify patterns such as:

**Productivity Risk**

Employees with:

High idle time
High Laziness Index
Low task completion
High social-media usage

may represent a higher productivity-risk group.

**Department Performance**

Departments with consistently high Laziness Index values and lower task completion may require targeted HR investigation.

**Work Mode**

WFH and Office employees should be compared using multiple productivity indicators instead of assuming that one work mode is inherently better.

**Meeting Efficiency**

High meeting attendance does not necessarily mean high productivity. Meeting load should be evaluated alongside task completion.

**Employee Benchmarking**

High-performing employees can be analyzed to identify positive productivity patterns that may be replicated across teams.

---

**🔐 Responsible Analytics**

The Laziness Index should be treated as an **analytical indicator rather than a definitive judgment of an employee's work ethic.**

Employee productivity can be influenced by many factors, including:

Workload 

Task complexity

Job responsibilities

Meeting requirements

Deadlines

Work mode

Team structure

Individual circumstances

Therefore, the dashboard should be used to identify patterns and areas for further investigation, not as the sole basis for employee disciplinary decisions.

---
## 💡 Key Insights
*(Fill in with your actual findings after building the dashboard, e.g.:)*
- The **[Department]** team shows the highest average Laziness Index, driven mainly by high social media usage.
- **WFH** employees show a **[X]%** higher average Laziness Index compared to Office employees.
- Employees with **Low salary levels** show comparatively **[higher/lower]** productivity than Medium/High salary bands.
- Higher social media usage strongly correlates with a higher rate of missed deadlines.
- **[Department]** is flagged for HR intervention due to consistently high laziness scores and low completion rates.

---


## 📁 Repository Structure
```
├── Laziness_Analysis.pbix        # Power BI dashboard file
├── dataset/
│   └── Laziness_Analysis_200_Records.csv     # Source dataset (200 records)
├── screenshots/
│   └── dashboard_overview.png    # Dashboard preview images
└── README.md                     # Project documentation
```


---

⭐ If you found this project useful, consider giving it a star on GitHub!
