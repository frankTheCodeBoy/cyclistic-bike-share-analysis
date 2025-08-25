# 🧠 Purpose

Create a set of dynamic title measures that reflect slicer selections like:

- `rideable_type`
- `day_of_week`
- `StartHour`
- `member_casual`

These measures can be reused in **Card visuals** to act as dynamic titles for each chart.

---

## 📁 Suggested Setup: `_MetaMeasures` Table

Create a dedicated table to store all your metadata and title measures:

```DAX
_MetaMeasures = DATATABLE("Label", STRING, { {"Placeholder"} })
```

> This creates a dummy table to hold your DAX measures. You won’t use the column — just the table name.

---

## 🧩 Reusable DAX Template: `DynamicChartTitle`

```DAX
DynamicChartTitle = 
"Ride Analysis for " & 
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
) & 
" during " & 
IF(
    ISFILTERED('rides'[StartHour]),
    SELECTEDVALUE('rides'[StartHour]),
    "All Hours"
) & 
" by " & 
IF(
    ISFILTERED('rides'[member_casual]),
    SELECTEDVALUE('rides'[member_casual]),
    "All Rider Types"
)
```

> 🔍 Example Output:  
> `"Ride Analysis for electric_bike on Saturday during 14 by casual"`

---

## 🧠 Optional Variants

### 🔹 `Title_RideVolume`

```DAX
Title_RideVolume = 
"Ride Volume by Member Type for " & 
IF(
    ISFILTERED('rides'[rideable_type]),
    SELECTEDVALUE('rides'[rideable_type]),
    "All Types"
)
```

### 🔹 `Title_AvgDuration`

```DAX
Title_AvgDuration = 
"Average Ride Duration for " & 
IF(
    ISFILTERED('rides'[member_casual]),
    SELECTEDVALUE('rides'[member_casual]),
    "All Riders"
) & 
" on " & 
IF(
    ISFILTERED('rides'[day_of_week]),
    SELECTEDVALUE('rides'[day_of_week]),
    "All Days"
)
```

---

## 🧩 How to Use in Power BI

1. Create the `_MetaMeasures` table.
2. Add these DAX measures to that table.
3. Insert a **Card visual**.
4. Drag the relevant title measure into the card.
5. Format and position the card above your chart.

---

## 📦 Suggested Naming Convention

| Purpose              | Measure Name             |
|----------------------|--------------------------|
| General title        | `DynamicChartTitle`       |
| Ride volume chart    | `Title_RideVolume`        |
| Avg duration chart   | `Title_AvgDuration`       |
| Hourly chart         | `Title_HourlyPattern`     |

---
