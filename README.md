# 🚴 Cyclistic Bike-Share Analysis — Google Data Analytics Capstone

![Cyclistic Bike-Share Analysis Banner](banner-image.png)

## 📘 Project Description

[![Project Status](https://img.shields.io/badge/status-complete-brightgreen)](https://github.com/frankTheCodeBoy/cyclistic-bike-share-analysis/)
[![Power BI](https://img.shields.io/badge/tool-Power%20BI-yellow)](https://powerbi.microsoft.com/)
[![Google Certificate](https://img.shields.io/badge/Google%20Data%20Analytics-Capstone-blue)](https://www.coursera.org/professional-certificates/google-data-analytics)
[![Made with Markdown](https://img.shields.io/badge/documentation-Markdown-blueviolet)](https://www.markdownguide.org/)

This capstone project is the culmination of the **Google Data Analytics Professional Certificate**, completed by Francis Olum. It explores how casual riders and annual members use Cyclistic’s bike-share service differently, with the goal of converting casual riders into loyal annual members.

Using **Power BI**, **Power Query**, and structured business analytics methodology (ASK → ACT), this project delivers a stakeholder-ready dashboard, actionable insights, and strategic recommendations.

---

## 🎯 Business Task

> **How do annual members and casual riders use Cyclistic bikes differently?**

Cyclistic’s marketing team wants to understand rider behavior to design campaigns that convert casual riders into annual members—who contribute higher profit margins and long-term value.

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** (dashboard design & storytelling)
- **Microsoft Excel with Power Query** (data cleaning & transformation)
- **Markdown** (modular documentation)
- **PDF Report** (visual summary)
- **Google Data Analytics Professional Certificate**  
  [Verify Credential](https://coursera.org/verify/professional-cert/SLZ7ERDFU7TL)

---

## 📁 Repository Structure
```
Cyclistic-Capstone/
├── ASK.md
├── PREPARE.md
├── PROCESS.md
├── ANALYZE.md
├── SHARE.md
├── ACT.md
├── Cyclistic_Report_Visuals.pdf
├── README.md
```
---

## 📊 Key Findings

- Casual riders take longer rides (~20–25 mins), mostly on weekends and afternoons.
- Members ride more frequently (~8–12 mins), especially during weekday commute hours.
- Electric bikes are more popular among members; casual riders prefer classic bikes.
- Casual riders favor stations near parks and tourist areas; members use transit-linked stations.
- Targeted promotions and commute incentives can drive membership conversions.

---

## 📈 Dashboard Preview

> ![Dashboard Preview](screenshots/cyclistic-dashboard.png)

---

## 🧠 What I Learned

- How to apply the full data analysis lifecycle: Ask → Prepare → Process → Analyze → Share → Act
- Data cleaning and transformation using Power Query
- Building interactive dashboards in Power BI
- Communicating insights through visual storytelling
- Translating data into strategic business actions

---

## 📬 Author

**Francis Olum**  
Creative full-stack developer | data analytics practitioner  
📍 Nairobi, Kenya  
🔗 📧 [olumfrank48@gmail.com](mailto:olumfrank48@gmail.com)

---

## 📜 License

This project is licensed for educational and portfolio use.  
All data used is publicly available and anonymized.  
No proprietary or confidential information is included.

---

## 📚 Additional Resources

[![Slicer Guide](https://img.shields.io/badge/guide-slicers%20%26%20filters-blue)](slicer-and-filters-guide.md)

For deeper insight into how slicers and filters shape the dashboard experience, see:

👉 [`slicer-and-filters-guide.md`](docs/slicer-and-filters-guide.md) — *A modular walkthrough of slicer logic, filter propagation, and best practices for interactivity.*

---

## 🧩 Dynamic Chart Titles with `_MetaMeasures`

[![DAX Titles](https://img.shields.io/badge/DAX-dynamic%20titles-orange)](https://dax.guide/)

To improve clarity and interactivity, this dashboard uses dynamic chart titles powered by reusable DAX measures stored in a metadata table called `_MetaMeasures`.

Each measure reflects slicer selections such as:

- `rideable_type`
- `day_of_week`
- `StartHour`
- `member_casual`

These measures are displayed using **Card visuals** above each chart.

### 🧪 Example Measure

```DAX
DynamicChartTitle = 
"Ride Analysis for " & 
IF(ISFILTERED('rides'[rideable_type]), SELECTEDVALUE('rides'[rideable_type]), "All Rideable Types") & 
" on " & 
IF(ISFILTERED('rides'[day_of_week]), SELECTEDVALUE('rides'[day_of_week]), "All Days") & 
" during " & 
IF(ISFILTERED('rides'[StartHour]), SELECTEDVALUE('rides'[StartHour]), "All Hours") & 
" by " & 
IF(ISFILTERED('rides'[member_casual]), SELECTEDVALUE('rides'[member_casual]), "All Rider Types")
```

> 🔍 Example Output: `"Ride Analysis for electric_bike on Saturday during 14 by casual"`

---
