# 🎬 Netflix Analytics Dashboard — Power BI

An interactive **Power BI dashboard** designed to analyze Netflix's global weekly viewing data, country-level Top 10 performance, category trends, and all-time title performance.

This project transforms Netflix datasets into an interactive two-page analytical dashboard using **Power Query, Data Modeling, DAX, and Power BI**.

---

## 📊 Dashboard Preview

### 🌍 Netflix Overview Dashboard

![Netflix Overview Dashboard](Netflix%20Overview%20Dashboard.png)

### 🌎 Netflix Country Analysis Dashboard

![Netflix Country Analysis Dashboard](Netflix%20Country%20Analysis%20Dashboard.png)

---

## 📌 Project Overview

The **Netflix Analytics Dashboard** provides an interactive view of Netflix viewing performance across different time periods, categories, titles, and countries.

The dashboard is divided into two main pages:

1. **Overview Dashboard**
2. **Country Analysis Dashboard**

Users can interact with filters and visuals to explore Netflix performance from both a global and country-level perspective.

---

## 🎯 Project Objectives

- Analyze Netflix global weekly viewing performance
- Track total titles, viewing hours, and views
- Analyze weekly viewing trends over time
- Compare performance across Netflix categories
- Identify top titles based on viewing hours
- Analyze country-level Top 10 performance
- Identify the longest-running titles in the Top 10
- Track titles reaching the #1 position
- Create an interactive and visually consistent Power BI dashboard

---

# 📈 Dashboard 1 — Netflix Overview

The **Netflix Overview Dashboard** provides a high-level view of global Netflix viewing performance.

### 🔢 Key KPIs

- **Total Titles**
- **Total Weekly Hours**
- **Total Weekly Views**
- **Latest Week**
- **Latest Week Hours**
- **Latest Week Views**
- **Total Countries**

### 🏆 All-Time KPIs

- **#1 All-Time Title**
- **All-Time Hours**
- **All-Time Titles**
- **All-Time Views**

### 📊 Visualizations

- Total Weekly Hours by Date
- Weekly Views Trend by Category
- Top 10 Titles by Weekly Hours
- Viewing Hours by Category
- Year slicer
- Category slicer

The dashboard allows users to filter the weekly analysis by **Year** and **Category**.

---

# 🌍 Dashboard 2 — Country Analysis

The **Country Analysis Dashboard** focuses on Netflix's country-level Top 10 rankings.

### 🔢 Key KPIs

- **Country Titles**
- **#1 Ranked Titles**

### 📊 Visualizations

- Top 10 Countries by Number of Titles
- Weekly Unique Titles Trend
- Top 10 Longest-Running Titles
- Titles by Category
- Latest Top 10 Titles
- Top 10 Countries by #1 Ranked Titles
- Country slicer

The country slicer allows users to explore Netflix Top 10 performance for individual countries.

---

## 🗂️ Data Model

The Power BI data model combines multiple Netflix datasets and supporting dimension tables.

### Main Tables

- **Global Weekly**
- **Country Weekly**
- **Global All-Time**
- **Date**
- **Country**

### Key Relationships

- `Date[Date]` → `Global Weekly[week]`
- `Date[Date]` → `Country Weekly[week]`
- `Country[Country ISO2]` → `Country Weekly[country_iso2]`

The **Global All-Time** table is used independently for all-time performance metrics.

---

## 🧮 DAX Measures

Several DAX measures were created to support the dashboard analysis.

Examples include:

```DAX
Total Titles =
DISTINCTCOUNT('Global Weekly'[show_title])
```

```DAX
Total Weekly Hours =
SUM('Global Weekly'[weekly_hours_viewed])
```

```DAX
Total Weekly Views =
SUM('Global Weekly'[weekly_views])
```

```DAX
Total Countries =
DISTINCTCOUNT('Country Weekly'[country_name])
```

```DAX
Country Titles =
DISTINCTCOUNT('Country Weekly'[show_title])
```

DAX was also used for:

- Latest-week calculations
- Country-level analysis
- #1 ranked title analysis
- Top 10 appearances
- Longest-running title analysis
- All-time performance KPIs

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard development and visualization |
| **Power Query** | Data cleaning and transformation |
| **DAX** | Measures and analytical calculations |
| **Excel** | Source dataset format |
| **GitHub** | Project documentation and version hosting |

---

## 🧹 Data Preparation

The project involved:

- Importing multiple Netflix datasets
- Checking data quality and missing values
- Correcting data types
- Creating a dedicated Date table
- Creating a Country dimension table
- Building table relationships
- Creating calculated measures using DAX
- Formatting measures for dashboard presentation
- Validating country-level and weekly calculations

---

## 📁 Repository Structure

```text
Netflix-Analytics-Power-BI/
│
├── DataSet/
│   ├── 2026-09-18_country_weekly.xlsx
│   ├── 2026-09-18_global_alltime.xlsx
│   └── 2026-09-18_global_weekly.xlsx
│
├── Icons/
│   └── Dashboard KPI icons
│
├── Netflix Dashboard.pbix
├── Netflix Overview Dashboard.png
├── Netflix Country Analysis Dashboard.png
└── README.md
```

---

## ✨ Dashboard Features

- 🎯 Interactive KPI cards
- 📅 Year-based filtering
- 🎬 Category-based filtering
- 🌍 Country-level filtering
- 📈 Weekly trend analysis
- 🏆 #1 ranked title analysis
- 🔥 Top-performing title analysis
- ⏳ Longest-running Top 10 title analysis
- 📊 Global and country-level analytics
- 🎨 Netflix-inspired black and red dashboard theme

---

## 🚀 How to Use the Project

1. Clone or download this repository.
2. Open **`Netflix Dashboard.pbix`** using **Power BI Desktop**.
3. If required, update the dataset file paths in Power Query.
4. Refresh the data.
5. Use the **Year**, **Category**, and **Country** slicers to interact with the dashboards.
6. Explore the Overview and Country Analysis pages.

---

## 📚 Skills Demonstrated

- Data Cleaning
- Data Transformation
- Power Query
- Data Modeling
- DAX
- KPI Development
- Time-Series Analysis
- Ranking Analysis
- Data Visualization
- Dashboard Design
- Business Intelligence
- Data Storytelling

---

## 📌 Project Files

- **`Netflix Dashboard.pbix`** — Complete interactive Power BI dashboard
- **`Netflix Overview Dashboard.png`** — Overview dashboard preview
- **`Netflix Country Analysis Dashboard.png`** — Country analysis dashboard preview
- **`DataSet/`** — Source datasets used for analysis
- **`Icons/`** — Icons used in dashboard KPI cards

---

## 👤 Author

**Rahul Shewale**

Data Analyst | Power BI | SQL | Excel | Tableau

---

## ⭐ About This Project

This project was created as a **Data Analytics portfolio project** to demonstrate practical skills in data preparation, data modeling, DAX calculations, analytical thinking, and interactive dashboard development using Power BI.

If you find this project useful, feel free to ⭐ the repository.
