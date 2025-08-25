# 🎛️ Adding Slicers and Filters to the Cyclistic Power BI Report

This guide outlines how to enhance each visual in the Cyclistic dashboard with strategic slicers and filters. It’s designed to improve interactivity, uncover deeper insights, and support stakeholder exploration.

---

## 📄 Page 1: Ride Distribution Overview

### 🔹 Visual: Donut Chart — Count of `ride_id` by `member_casual`

**Summary**: Shows overall ride volume split between casual and member riders.

**Recommended Slicers**:

- `rideable_type` (Dropdown)
- `day_of_week` (Dropdown)

**Insights Unlocked**:

- “How do ride volumes shift by rider type across different bike/scooter types?”
- “Which rider type dominates on weekends?”

**How to Add**:

1. Insert slicer visual.
2. Drag `rideable_type` into one slicer, `day_of_week` into another.
3. Click slicer > top-right corner > select **Dropdown**.
4. Resize and position above or beside the donut chart.

**Slicer Titles**:

- “Filter by Rideable Type”
- “Filter by Day of Week”

**Comments**:

- Consider adding a **Card visual** showing total filtered ride count.
- Use tooltips to show exact ride counts and percentages.

---

## 📄 Page 2: Weekly Ride Patterns

### 🔹 Visual: Clustered Column Chart — Count of `ride_id` by `day_of_week` and `member_casual`

**Summary**: Displays ride volume across weekdays split by rider type.

**Recommended Slicers**:

- `rideable_type` (Dropdown)
- `StartHour` (Horizontal buttons)

**Insights Unlocked**:

- “Do casual riders prefer electric bikes on weekends?”
- “What are peak hours for members on weekdays?”

**How to Add**:

1. Insert slicers for `rideable_type` and `StartHour`.
2. Format `rideable_type` as dropdown, `StartHour` as horizontal buttons.
3. Use **Edit Interactions** to ensure both slicers affect the chart.

**Slicer Titles**:

- “Filter by Rideable Type”
- “Filter by Start Hour”

**Comments**:

- Add dynamic chart title reflecting active filters.
- Consider syncing slicers across pages for consistent filtering.

---

## 📄 Page 3: Ride Duration Analysis

### 🔹 Visual: Bar Chart — AvgRide Duration by `member_casual`

**Summary**: Compares average ride duration between rider types.

**Recommended Slicers**:

- `rideable_type` (Dropdown)
- `day_of_week` (Dropdown)
- `StartHour` (Optional)

**Insights Unlocked**:

- “Do casual riders take longer rides on weekends?”
- “Which vehicle type leads to longer average rides?”

**How to Add**:

1. Add slicers for `rideable_type` and `day_of_week`.
2. Format both as dropdowns.
3. Use **Single Select** for focused analysis or **Multi-select** for broader view.

**Slicer Titles**:

- “Filter by Rideable Type”
- “Filter by Day of Week”

**Comments**:

- Add tooltip to show exact average duration.
- Consider using a line chart for trend comparison if needed.

---

## 📄 Page 4: Rideable Type Usage

### 🔹 Visual: Column Chart — Count of `ride_id` by `rideable_type` and `member_casual`

**Summary**: Shows ride volume by vehicle type split by rider type.

**Recommended Slicers**:

- `day_of_week` (Dropdown)
- `StartHour` (Dropdown or buttons)

**Insights Unlocked**:

- “Which rideable type is most popular among casual riders on Fridays?”
- “Do members prefer classic bikes during morning hours?”

**How to Add**:

1. Insert slicers for `day_of_week` and `StartHour`.
2. Format `day_of_week` as dropdown, `StartHour` as horizontal buttons.
3. Use **Edit Interactions** to link slicers to the chart.

**Slicer Titles**:

- “Filter by Day of Week”
- “Filter by Start Hour”

**Comments**:

- Add a stacked version of this chart for visual comparison.
- Use color coding to highlight rider type differences.

---

## 📄 Page 5: Hourly Ride Patterns

### 🔹 Visual: Column Chart — Count of `ride_id` by `StartHour` and `member_casual`

**Summary**: Displays ride volume across hours of the day split by rider type.

**Recommended Slicers**:

- `rideable_type` (Dropdown)
- `day_of_week` (Dropdown)

**Insights Unlocked**:

- “Do members ride more during morning rush hours?”
- “Are casual riders more active in the evenings?”

**How to Add**:

1. Add slicers for `rideable_type` and `day_of_week`.
2. Format both as dropdowns.
3. Position above or beside the chart for easy access.

**Slicer Titles**:

- “Filter by Rideable Type”
- “Filter by Day of Week”

**Comments**:

- Add a line chart overlay to show hourly trends.
- Consider grouping hours into time blocks (e.g., Morning, Afternoon, Evening).

---

## 📦 Should This Document Be Included in Your Project Repo?

**Absolutely yes.**  
This markdown file serves as:

- A **technical guide** for dashboard interactivity
- A **stakeholder reference** for exploring insights
- A **portfolio asset** showcasing your strategic thinking

📁 **Suggested filename**: `slicers-and-filters-guide.md`  
📂 **Suggested location**: Root of your Cyclistic project repo or inside `/docs/` folder

---
