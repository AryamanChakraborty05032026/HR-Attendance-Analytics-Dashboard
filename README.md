# HR Attendance Analytics Dashboard

A **people analytics project** that transforms raw employee attendance logs into **actionable HR insights and an interactive dashboard**.

This project analyzes multi-month attendance data using **Python and pandas**, performs feature engineering to derive meaningful workforce metrics, and presents insights through **interactive visualizations built with Plotly and Streamlit**.

The goal is to demonstrate how HR teams can move from static attendance sheets to **data-driven workforce insights** that help identify patterns in attendance, leave usage, work-from-home behavior, and potential absenteeism risk.

---

# Project Overview

Organizations collect large volumes of attendance data every month, but it often remains underutilized in static spreadsheets.

This project converts **Excel attendance sheets into a structured analytics workflow** that:

- Cleans and standardizes raw HR attendance data  
- Engineers meaningful workforce metrics  
- Performs exploratory analysis  
- Presents insights through an **interactive HR dashboard**

The result is a **simple people analytics tool** that HR teams could use to monitor attendance patterns and employee leave behavior.

---

# Business Problem & Objectives

Attendance data provides valuable signals about **workforce engagement, absenteeism, and operational planning**, but it is rarely analyzed beyond simple totals.

HR teams often need to answer questions such as:

- Which employees have **consistent attendance patterns**?
- Who may be at **risk of absenteeism**?
- How widely is **work-from-home (WFH)** being used?
- What types of **leave are most common**?
- Are there **daily attendance patterns** HR should monitor?

### Objectives of the Project

- Convert raw attendance logs into **structured analytics data**
- Build **HR-relevant KPIs** for workforce monitoring
- Identify **leave behavior trends**
- Analyze **WFH usage patterns**
- Detect **potential absenteeism risk signals**
- Build an **interactive dashboard** for easy exploration

---

# Dataset Description

The dataset consists of **employee attendance records across multiple months**, stored in an Excel workbook.

**File:**  
`Attendance-Sheet-2022-2023.xlsx`

### Structure

- Multiple sheets representing **different months**
- One row per **employee per month**

### Example Columns

| Column | Description |
|------|-------------|
| Employee Code | Unique employee identifier |
| Employee Name | Employee name |
| Daily Attendance Columns | Attendance status for each day |
| Present | Total present days |
| Work From Home (WFH) | WFH days |
| Paid Leave (PL) | Paid leave days |
| Sick Leave (SL) | Sick leave days |
| Leave Without Pay (LWP) | Unpaid leave |
| Weekly Off (WO) | Weekend days |
| Holidays (HO) | Public holidays |
| Other Leave Types | Birthday leave, floating festival leave, bereavement leave, etc. |

### Attendance Status Codes

| Code | Meaning |
|-----|--------|
| P | Present |
| WFH | Work From Home |
| PL | Paid Leave |
| SL | Sick Leave |
| LWP | Leave Without Pay |
| WO | Weekly Off |
| HO | Holiday |

---

# Features & Analysis

The project performs **feature engineering and exploratory analysis** to generate HR insights.

## Workforce KPIs

Key workforce metrics are calculated to summarize overall attendance behavior.

Examples include:

- **Total Employees**
- **Average Attendance Rate**
- **Total Leave Days**
- **WFH Utilization Rate**
- **Leave Without Pay (LWP) Rate**

These KPIs provide a quick snapshot of **organizational attendance health**.

---

## Employee Attendance Analysis

This section focuses on **individual attendance performance**.

Key analyses include:

- **Top 10 employees by attendance**
- **Employees with highest leave days**
- **LWP leaderboard (potential absenteeism signals)**
- **Employee attendance rate comparison**

These metrics help HR identify both **highly consistent employees** and **employees with potential attendance concerns**.

---

## Leave Type Analysis

Understanding leave behavior helps HR teams manage **workforce planning and policies**.

Analysis includes:

- Distribution of **different leave types**
- **Stacked bar chart** showing leave mix by employee
- Usage of **special leave categories**, such as:
  - Birthday leave
  - Floating festival leave
  - Bereavement leave
  - Menstrual leave

This helps HR evaluate how employees **utilize available leave policies**.

---

## Work-From-Home (WFH) Insights

WFH usage has become an important workforce metric.

This section analyzes:

- **WFH share of total attendance**
- Employees with **highest WFH usage**
- WFH distribution across months

These insights help HR understand **remote work adoption and workforce flexibility**.

---

## Daily Patterns & Absenteeism Risk

Beyond monthly summaries, the project explores **daily attendance patterns**.

Key visualizations include:

- **Daily attendance trend**
- **Attendance heatmaps**
- **Absenteeism leaderboard**

### Absenteeism Score

A simple risk score was created using:

- Leave Without Pay (LWP)
- Sick Leave
- Total leave days

This score helps highlight employees who may require **additional HR attention or support**.

---

# Tech Stack

### Programming Language
- Python

### Libraries
- pandas  
- numpy  
- plotly  

### Tools
- Streamlit (interactive dashboard)
- Jupyter Notebook (data exploration)
- Excel (data source)

---

# Project Structure

```
HR-Attendance-Analytics-Dashboard
│
├── data
│   └── Attendance-Sheet-2022-2023.xlsx
│
├── notebooks
│   └── attendance_analysis.ipynb
│
├── images
│   └── dashboard_screenshots.png
│
├── app.py
├── requirements.txt
└── README.md
```

### Key Files

**attendance_analysis.ipynb**  
Contains data cleaning, feature engineering, and exploratory data analysis.

**app.py**  
Main Streamlit dashboard application.

**data/**  
Raw attendance dataset.

**images/**  
Dashboard screenshots for documentation.

---

# How to Run the Project

## 1. Clone the Repository

```bash
git clone https://github.com/yourusername/hr-attendance-analytics-dashboard.git
cd hr-attendance-analytics-dashboard
```

---

## 2. Create a Virtual Environment

Using **venv**

```bash
python -m venv venv
source venv/bin/activate
```

Or using **conda**

```bash
conda create -n hr-analytics python=3.10
conda activate hr-analytics
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Run the Notebook (Optional)

For step-by-step analysis and exploration:

```bash
jupyter notebook
```

Open:

```
notebooks/attendance_analysis.ipynb
```

---

## 5. Run the Streamlit Dashboard

```bash
streamlit run app.py
```

The dashboard will launch automatically in your browser.

---

# Dashboard Overview

The Streamlit application contains several interactive sections.

### Sidebar Filters

Users can filter the dashboard by:

- Month
- Employee
- Optional department or team filters (if available)

### Dashboard Tabs

**Overview**

- Core workforce KPIs
- Attendance rate gauge
- WFH vs office pie chart
- Attendance comparison by month

**Attendance**

- Top attendance performers
- Highest leave days
- LWP leaderboard
- Employee metrics table

**Leaves**

- Leave type distribution
- Leave mix stacked bar chart
- Special leave usage

**WFH**

- Top WFH users
- WFH share of attendance

**Daily & Risk**

- Daily attendance trends
- Attendance heatmap
- Absenteeism risk leaderboard

---

# Example Insights

Some example findings from the analysis include:

- Identified employees with **higher absenteeism risk using an LWP-weighted scoring model**
- Observed **consistent high attendance performers across multiple months**
- Found that **WFH represented a measurable portion of total attendance**
- Identified **variation in leave type usage**, with some special leave categories rarely used
- Detected **days with consistently lower attendance**, which may relate to holidays or operational patterns

These insights illustrate how attendance data can support **HR decision-making and workforce planning**.

---

# Potential Extensions / Next Steps

Possible improvements to expand the project include:

- Integrating with a **database instead of Excel**
- Adding **department or team-level analytics**
- Implementing **authentication and role-based access**
- Deploying the dashboard on **Streamlit Cloud**
- Adding **predictive absenteeism models**
- Performing **longer time-series analysis across multiple years**

---

# About Me / Learning Goals

I built this project as part of my transition into **data analytics and people analytics**.

The goal was to practice:

- Working with **real-world HR data**
- Performing **data cleaning and feature engineering with pandas**
- Designing **HR-relevant workforce KPIs**
- Building **interactive dashboards using Streamlit**

This project reflects my approach to learning analytics by **combining technical tools with practical HR questions**.

If you have suggestions, feedback, or ideas for improvement, feel free to open an issue or connect.
