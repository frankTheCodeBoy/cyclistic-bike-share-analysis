# 🛠️ How to Add a Dynamic Chart Titles in Power BI

## ✅ Step-by-Step Guide

### 1. **Create a Measure for the Title**

Use DAX to create a measure that reflects the slicer selections.

### Example: Dynamic Title Based on `rideable_type` and `day_of_week`

```DAX
ChartTitle = 
"Ride Count by Member Type for " & 
IF(
    ISFILTERED('rides'[rideable_type]),
    SELECTEDVALUE('rides'[rideable_type]),
    "All Rideable Types"
) & 
" on " & 
IF(
    ISFILTERED('rides'[day_of_week]),
    SELECTEDVALUE('rides'[day_of_week]),
    "All Days"
)
```

> 🔍 This measure returns a string like:  
> `"Ride Count by Member Type for electric_bike on Saturday"`

---

### 2. **Add a Card Visual for the Title**

- Insert a **Card visual** from the Visualizations pane.
- Drag the `ChartTitle` measure into the card.
- Resize and position the card **above your chart** to act as the title.

---

### 3. **Format the Card**

- Remove background and border for a clean look.
- Use bold font and increase size (e.g., 16–20pt).
- Align center or left depending on your layout.

---

## 🧠 Bonus Tips

| Feature              | Recommendation                            |
|----------------------|--------------------------------------------|
| **Fallback Text**     | Always include default text for unfiltered state |
| **Multiple Filters**  | Use `CONCATENATEX` if multiple values may be selected |
| **Title Placement**   | Position consistently across visuals       |
| **Sync with Slicers** | Ensure slicers affect the measure context |

---

## 🧩 Example Use Case in the Cyclistic Report

For the **donut chart** on report (pg 1):

- Dynamic title could say:  
  > “Ride Distribution by Member Type for classic_bike on Friday”

For the **hourly chart** on report (pg 5):

- Dynamic title could say:  
  > “Hourly Ride Volume by Member Type for electric_scooter on Sunday”

---
