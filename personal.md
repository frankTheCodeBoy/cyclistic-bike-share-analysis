# 📘 Personal README: Cyclistic Dashboard Design & Presentation Guide

## 👤 Author: Frank Olum  

Creative full-stack developer | Business analytics practitioner  
Capstone project: Cyclistic case study (Power BI)

---

## 🎯 Purpose of This Guide

This document is my personal reference for designing, refining, and presenting the Cyclistic dashboard. It helps me:

- Understand why each chart matters
- Use filters and slicers effectively
- Pin the right visuals to the dashboard
- Avoid common mistakes
- Choose a theme that supports clarity
- Tell a compelling story to stakeholders

---

## 📊 Relevance of Visualizations (from PDF Report)

| Visualization                          | Why It Matters                                                   |
|----------------------------------------|------------------------------------------------------------------|
| Rider Type Distribution (Donut Chart)  | Shows conversion potential between casual and member riders     |
| Rides by Day of Week (Bar Chart)       | Reveals behavioral patterns → informs campaign timing           |
| Rides by Hour of Day (Heatmap)         | Identifies peak hours → supports commute-based promotions       |
| Bike Type Usage (Stacked Bar)          | Highlights product preferences → electric bike incentives       |
| Avg Ride Duration (Bar Chart)          | Differentiates leisure vs. commute behavior                     |
| Monthly Ride Trends (Line Chart)       | Tracks seasonality → helps time marketing pushes                |
| Station Frequency (Stacked Bar)        | Pinpoints high-traffic stations → geo-targeted campaigns        |
| Map of Start/End Stations              | Visualizes rider hotspots → supports station optimization       |

✅ All visuals directly support the business goal: **convert casual riders into annual members**

---

## 🧮 Filters vs. Slicers

| Feature   | Filters                                  | Slicers                                  |
|-----------|------------------------------------------|------------------------------------------|
| Scope     | Can be page-level, visual-level, or report-level | Always visual and interactive for users |
| Visibility| Hidden from dashboard viewers            | Visible and clickable                    |
| Use Case  | Control data behind the scenes           | Empower users to explore data            |
| Example   | Filter out null stations from map        | Slicer for Rider Type (Casual/Member)    |

✅ Use **filters** for cleanup and logic  
✅ Use **slicers** for exploration and storytelling

---

## 📌 Charts to Pin to Dashboard

Pin these from your report to the dashboard:

- ✅ Rider Type Distribution (Donut)
- ✅ Bike Type Usage by Rider Type (Stacked Bar)
- ✅ Avg Ride Duration (Bar)
- ✅ Rides by Day of Week (Bar)
- ✅ Rides by Hour of Day (Heatmap)
- ✅ Monthly Ride Trends (Line)
- ✅ Station Frequency (Stacked Bar)
- ✅ Map of Start/End Stations
- ✅ KPI Cards (Total Rides, % Casual, Avg Duration, Electric Bike Usage)

---

## 🚫 Do’s and Don’ts

### ✅ Do

- Use consistent colors (e.g., blue for casual, teal for members)
- Add tooltips for clarity
- Use slicers for Rider Type, Date Range, Station Name
- Keep layout modular (Executive Summary, Behavior, Time, Geo)
- Use bookmarks for storytelling views

### ❌ Don’t

- Overcrowd visuals—leave breathing space
- Use too many chart types—stick to familiar ones
- Mix color meanings (e.g., blue = casual throughout)
- Forget to label axes and titles clearly

---

## 🎨 Theme Selection Tips

- Use Cyclistic branding colors (blue, teal, gray)
- Choose a **light background** for readability
- Use **bold fonts** for KPI cards
- Apply a custom theme via Power BI Theme JSON or built-in templates

---

## 🗣️ Stakeholder Presentation & Storytelling

### 🔹 Structure Your Story

1. **ASK**: Cyclistic wants to convert casual riders into annual members
2. **PREPARE**: Cleaned and modeled ride data
3. **PROCESS**: Identified patterns in rider behavior
4. **ANALYZE**: Found key differences in time, bike type, station use
5. **ACT**: Proposed targeted campaigns and product tweaks

### 🔹 Presentation Tips

- Start with KPIs and business goal
- Use slicers live to show “what if” scenarios
- Highlight actionable insights (e.g., weekend promos, commute incentives)
- End with a summary of recommendations and expected impact

---

## 🧠 Final Notes

This README is my personal guide to:

- Build dashboards that are strategic, clean, and interactive
- Present findings with confidence and clarity
- Learn from each project and improve my analytics storytelling
