# 📊 Cyclistic Case Study Roadmap: ANALYZE Phase

## 🧠 Guiding Questions & Insights

### 🔹 How should you organize your data to perform analysis on it?

- Data was aggregated from 12 monthly CSVs using Power Query and loaded into Power BI.
- Structured into a star schema with key dimensions:
  - `member_casual` (rider type)
  - `ride_length` (duration in seconds)
  - `day_of_week` (weekday name)
  - `start_hour` (hour of day)
  - `rideable_type` (bike category)
- This structure enables dynamic filtering and trend analysis across rider behaviors.

### 🔹 Has your data been properly formatted?

- ✅ Date and time fields standardized
- ✅ Calculated columns created:
  - `ride_length` (in seconds, then converted to minutes)
  - `day_of_week` (derived from `started_at`)
  - `start_hour` (hour extracted from `started_at`)
- ✅ Nulls replaced with “Unknown” where necessary
- ✅ Duplicates removed
- ✅ Consistent data types across merged datasets

---

## 📈 Key Findings with Numerical Insights

### 1. 🚴‍♂️ **Ride Volume by Rider Type**

- **Members**: 615,770 rides (≈58.72%)
- **Casual Riders**: 432,810 rides (≈41.28%)
- **Insight**: Members dominate usage, but casual riders represent a sizable opportunity for conversion.

### 2. 📅 **Ride Frequency by Day of Week**

| Day        | Casual Peak | Member Peak |
|------------|-------------|-------------|
| Saturday   | ~100K       | ~60K        |
| Sunday     | ~90K        | ~55K        |
| Monday–Friday | ~40K–60K | ~60K–80K    |

- **Insight**: Casual riders peak on weekends; members ride consistently on weekdays, especially Monday to Friday.

### 3. ⏱️ **Average Ride Duration**

- **Casual Riders**: ~1,200–1,500 seconds (20–25 minutes)
- **Members**: ~500–700 seconds (8–12 minutes)
- **Insight**: Casual riders take longer trips, indicating leisure or exploratory behavior. Members ride shorter, likely commute-based trips.

### 4. 🚲 **Bike Type Preference**

| Rideable Type     | Casual Count | Member Count |
|-------------------|--------------|--------------|
| Classic Bike      | ~400K        | ~500K        |
| Electric Bike     | ~250K        | ~350K        |
| Electric Scooter  | Minimal      | Minimal      |

- **Insight**: Members show higher adoption of electric bikes, suggesting preference for speed and efficiency.

### 5. 🕒 **Ride Start Hour Distribution**

| Hour Range | Casual Peak | Member Peak |
|------------|-------------|-------------|
| 0–6        | Low         | Moderate    |
| 7–9        | Moderate    | High        |
| 10–16      | High        | Moderate    |
| 17–19      | Moderate    | High        |
| 20–23      | Low         | Low         |

- **Insight**: Members peak during commute hours (7–9 AM, 5–7 PM); casual riders peak midday (10 AM–4 PM).

---

## 🎯 Business Task Alignment

> **Business Task:**  
> _Analyze how annual members and casual riders use Cyclistic bikes differently._

### ✅ Behavioral Differences Identified

- **Ride Frequency**: Members ride more often, especially on weekdays.
- **Ride Duration**: Casual riders take longer trips.
- **Time of Day**: Members ride during commute hours; casual riders prefer midday.
- **Bike Type**: Members favor electric bikes; casual riders stick with classic bikes.

### ✅ Strategic Implications

- **Target casual riders with weekday commute incentives** (e.g., discounted morning rides).
- **Promote electric bike upgrades to casual users** via app banners or email nudges.
- **Geo-target marketing near tourist hotspots and leisure parks** where casual usage is high.
- **Introduce loyalty programs or gamified challenges** to encourage repeat rides from casual users.

---

## 🛠️ Key Tasks Completed

- ✅ Aggregated and cleaned 12 months of trip data
- ✅ Created calculated columns for analysis
- ✅ Built interactive dashboards in Power BI
- ✅ Identified behavioral differences between rider types
- ✅ Quantified trends with actionable metrics

---

## 📌 Deliverable: Summary of Analysis

This analysis reveals clear behavioral distinctions between casual riders and annual members. Casual riders favor longer, weekend rides and leisure routes, while members ride more frequently, with shorter durations, and on weekdays. These insights form the foundation for a targeted marketing strategy aimed at converting casual riders into loyal members—supporting Cyclistic’s goal of increasing annual memberships and maximizing revenue.

---
