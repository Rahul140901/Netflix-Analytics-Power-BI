# 🎬 Netflix Weekly Analytics Dashboard — Power BI

An interactive **Power BI dashboard** designed to analyze Netflix's **weekly viewing performance**, including global viewing trends, weekly views, weekly hours viewed, category performance, country-level Top 10 rankings, and all-time title performance.

This project transforms Netflix weekly datasets into an interactive two-page analytical dashboard using **Power Query, Data Modeling, DAX, and Power BI**.

---

## 📊 Dashboard Preview

### 🌐 Netflix Overview Dashboard

![Netflix Overview Dashboard](Netflix%20Overview%20Dashboard.png)

### 🌍 Netflix Country Analysis Dashboard

![Netflix Country Analysis Dashboard](Netflix%20Country%20Analysis%20Dashboard.png)

---

## 📌 Project Overview

The **Netflix Weekly Analytics Dashboard** provides an interactive analysis of Netflix viewing performance using **weekly global and country-level Top 10 data**.

Unlike a static Netflix catalog analysis, this project focuses on understanding **how titles perform week by week**, how viewing trends change over time, and how titles rank across different countries and categories.

The analysis focuses on:

- Weekly viewing trends
- Weekly views and hours viewed
- Latest-week performance
- Category-wise viewing performance
- Top titles by weekly viewing hours
- Country-level Top 10 performance
- Weekly title rankings
- Longest-running Top 10 titles
- #1 ranked titles by country
- All-time title performance

The dashboard contains two analytical pages:

1. **Netflix Overview Dashboard** — focuses on global weekly viewing trends and overall performance.
2. **Netflix Country Analysis Dashboard** — focuses on weekly country-level Top 10 performance and title rankings.

---

## 🎯 Project Objectives

The main objectives of this project are to:

- Analyze Netflix's weekly global viewing performance
- Track total weekly views and viewing hours
- Monitor the latest available week's performance
- Identify changes in viewing trends over time
- Compare performance across Netflix categories
- Identify top-performing titles based on weekly viewing hours
- Analyze country-level Top 10 rankings
- Track unique titles appearing in country Top 10 lists
- Identify titles that remain in the Top 10 for the longest period
- Analyze titles reaching the #1 position
- Compare global weekly analysis with all-time title performance
- Build an interactive and visually consistent Power BI dashboard

---

# 📈 Dashboard 1 — Netflix Overview

The **Netflix Overview Dashboard** provides a high-level view of Netflix's global weekly viewing performance.

It allows users to analyze how Netflix titles perform across different weeks, years, and content categories.

## 🔢 Key Weekly KPIs

- **Total Titles**
- **Total Weekly Hours**
- **Total Weekly Views**
- **Latest Week**
- **Latest Week Hours**
- **Latest Week Views**
- **Total Countries**

## 🏆 All-Time KPIs

The dashboard also includes a separate all-time section for comparison with weekly performance:

- **#1 All-Time Title**
- **All-Time Hours**
- **All-Time Titles**
- **All-Time Views**

## 📊 Overview Visualizations

- **Weekly Views Trend by Category**
- **Total Weekly Hours by Date**
- **Top 10 Titles by Weekly Hours**
- **Viewing Hours by Category**
- **Year Slicer**
- **Category Slicer**

The **Year** and **Category** slicers allow users to interactively explore weekly Netflix performance across different time periods and content categories.

---

# 🌍 Dashboard 2 — Country Analysis

The **Netflix Country Analysis Dashboard** focuses on Netflix's **weekly country-level Top 10 rankings**.

Users can select an individual country and analyze how different titles perform within that country's weekly Top 10 lists.

## 🔢 Country KPIs

- **Country Titles**
- **#1 Ranked Titles**

## 📊 Country-Level Visualizations

- **Top 10 Countries by Number of Titles**
- **Weekly Unique Titles Trend**
- **Top 10 Longest-Running Titles**
- **Titles by Category**
- **Latest Top 10 Titles**
- **Top 10 Countries by #1 Ranked Titles**
- **Country Slicer**

The **Country slicer** allows users to dynamically explore weekly Top 10 performance for individual countries.

---

## 📅 Weekly Analysis Focus

A key feature of this project is its focus on **weekly analytics** rather than only analyzing a static catalog of Netflix titles.

The dashboard allows analysis of:

- How viewing activity changes from week to week
- Which titles generate the most weekly viewing activity
- How category performance changes over time
- Which titles repeatedly appear in country Top 10 lists
- How many unique titles appear each week
- Which titles remain in the Top 10 for multiple weeks
- Which titles achieve the #1 ranking
- How the latest week's performance compares with historical weekly data

This makes the dashboard useful for analyzing **time-based viewing patterns and ranking behavior**, rather than simply describing the Netflix content catalog.

---

## 🗂️ Data Model

The Power BI data model combines multiple Netflix datasets with supporting dimension tables.

### Main Tables

- **Global Weekly**
- **Country Weekly**
- **Global All-Time**
- **Date**
- **Country**

### Key Relationships

```text
Date[Date]
    │
    ├──► Global Weekly[week]
    │
    └──► Country Weekly[week]

Country[Country ISO2]
    │
    └──► Country Weekly[country_iso2]
```

The **Date** table supports time-based weekly analysis.

The **Country** dimension supports country-level filtering and analysis.

The **Global All-Time** table is used independently for the all-time performance KPIs.

---

## 🧮 DAX Measures

Multiple DAX measures were created to support weekly, country-level, latest-week, ranking, and all-time analysis.

### Example Measures

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

```DAX
Weekly Unique Titles =
DISTINCTCOUNT('Country Weekly'[show_title])
```

Additional DAX calculations were created for:

- Latest-week identification
- Latest-week viewing hours
- Latest-week views
- Country-specific latest-week analysis
- Country Top 10 appearances
- #1 ranked title analysis
- Longest-running Top 10 titles
- All-time title metrics

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard development and interactive visualization |
| **Power Query** | Data cleaning and transformation |
| **DAX** | KPI measures and analytical calculations |
| **Data Modeling** | Table relationships and filter propagation |
| **Excel** | Source dataset format |
| **GitHub** | Project documentation and portfolio hosting |

---

## 🧹 Data Preparation

The project involved several data preparation and modeling steps:

- Imported multiple Netflix datasets
- Checked data quality and missing values
- Corrected column data types
- Prepared weekly date fields
- Created a dedicated **Date table**
- Created a dedicated **Country dimension**
- Built relationships between weekly and dimension tables
- Created DAX measures for weekly analysis
- Created latest-week calculations
- Developed country-level ranking measures
- Validated country-level Top 10 records
- Formatted KPIs for clear dashboard presentation
- Tested slicer and visual interactions

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

- 📅 Weekly performance analysis
- 📈 Weekly viewing trend analysis
- 🎯 Interactive KPI cards
- 🎬 Title-level performance analysis
- 🌍 Country-level Top 10 analysis
- 🏆 #1 ranked title analysis
- ⏳ Longest-running Top 10 title analysis
- 🔥 Top-performing title analysis
- 📊 Category-wise analysis
- 📆 Year-based filtering
- 🌐 Country-based filtering
- 🎞️ Category-based filtering
- 🏅 All-time performance KPIs
- 🎨 Netflix-inspired black, red, and white dashboard theme

---

## 🔍 Key Analytical Questions

This dashboard helps answer questions such as:

- How have Netflix weekly views changed over time?
- How have weekly viewing hours changed over time?
- Which categories generate the most viewing activity?
- Which titles receive the highest weekly viewing hours?
- What is the latest week's viewing performance?
- Which countries have the largest number of Top 10 titles?
- How many unique titles appear in a country's Top 10 each week?
- Which titles remain in the Top 10 for the longest period?
- Which countries have the most #1 ranked titles?
- Which titles are currently appearing in a selected country's Top 10?
- How does weekly performance compare with all-time title performance?

---

## 🚀 How to Use the Project

1. Clone or download this repository.
2. Open **`Netflix Dashboard.pbix`** using **Power BI Desktop**.
3. If required, update the source file paths in **Power Query**.
4. Refresh the dataset.
5. Open the **Netflix Overview Dashboard** to explore global weekly performance.
6. Use the **Year** and **Category** slicers to filter the weekly analysis.
7. Open the **Netflix Country Analysis Dashboard**.
8. Use the **Country** slicer to explore weekly Top 10 performance for individual countries.

---

## 📚 Skills Demonstrated

This project demonstrates practical experience with:

- Power BI
- Power Query
- DAX
- Data Cleaning
- Data Transformation
- Data Modeling
- Data Validation
- KPI Development
- Weekly Trend Analysis
- Time-Series Analysis
- Ranking Analysis
- Country-Level Analysis
- Data Visualization
- Interactive Dashboard Development
- Business Intelligence
- Data Storytelling

---

## 📌 Project Files

- **`Netflix Dashboard.pbix`** — Complete interactive Power BI dashboard
- **`Netflix Overview Dashboard.png`** — Global weekly analysis dashboard preview
- **`Netflix Country Analysis Dashboard.png`** — Country-level weekly analysis dashboard preview
- **`DataSet/`** — Netflix weekly and all-time datasets used in the analysis
- **`Icons/`** — Icons used in the dashboard KPI cards

---

## 👤 Author

**Rahul Shewale**

Aspiring Data Analyst | Power BI | SQL | Excel | Tableau

---

## ⭐ About This Project

This project was developed as a **Data Analytics portfolio project** to demonstrate practical skills in **Power BI, Power Query, DAX, data modeling, weekly trend analysis, ranking analysis, and interactive dashboard development**.

The project emphasizes **weekly Netflix viewing and Top 10 performance analysis**, while also incorporating country-level rankings and all-time performance metrics for additional context.

If you find this project useful, feel free to ⭐ the repository.
