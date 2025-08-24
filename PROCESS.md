# 🧼 Cyclistic Case Study Roadmap: PROCESS Phase

## 🧭 Guiding Questions

### 🛠️ What tools are you choosing and why?

**→** _Microsoft Excel with Power Query_  
Initially, Excel was chosen for its accessibility and robust data manipulation
capabilities. Power Query, in particular, enables efficient data import,
transformation, and loading — ideal for cleaning large datasets without writing
code.
Exploratory Data Analysis and preliminary data checks were conducted in
Microsoft Excel before adopting Power BI which is discussed below.

**→** _Power BI Desktop_
Due to the fast build up of data volume from the selection of 12 months worth
of dataset for this exercise, Power BI was adopted for its  efficiency in
handling large dataset volumes. Further transformations were conducted
after importing data from Excel, calculated columns and measures were created
in preparation for analysis.

### ✅ Have you ensured your data’s integrity?

Yes. Data integrity was maintained by:

- Importing all quarterly datasets consistently
- Verifying schema alignment across files
- Checking for duplicate entries and timestamp anomalies

### 🧹 What steps have you taken to ensure that your data is clean?

- Replaced rows with null values with 'Unknown' in critical fields (station names)
- Standardized column formats (e.g., datetime, text)
- Aggregated 'ride_lengths' in seconds to avoid zero-duration rides
- Ensured consistent naming conventions across station fields
- Removed dupliated data across rows

### 🔍 How can you verify that your data is clean and ready to analyze?

- Performed exploratory checks using filters and pivot tables
- Validated ride durations and station usage distributions
- Ensured no missing values in key columns
- Confirmed consistent data types across merged datasets

### 📝 Have you documented your cleaning process so you can review and share those results?

Yes. Each step of the cleaning process was documented in a separate markdown
file and annotated within Excel’s Power Query editor. This ensures transparency
and reproducibility for future reference or stakeholder review.

---

## 📌 Key Tasks

### ✅ Check the data for errors

- Identified and removed nulls, duplicates, and outliers
- Flagged inconsistent station names and corrected them

### ✅ Choose your tools

- Microsoft Excel with Power Query for transformation
- Power BI with Power Query for efficiently handling the large volumes of
aggregated data

### ✅ Transform the data so you can work with it effectively

- Merged quarterly datasets into a single master file
- Created new calculated columns (e.g., ride duration, day of week)
- Filtered out invalid entries and standardized formats

### ✅ Document the cleaning process

- Markdown notes created for each phase
- Power Query steps annotated for traceability
- Screenshots and logs saved for audit trail

---

## 📄 Deliverable

### Data Cleaning Documentation

For efficiency of workflow, all relevant data was aggregated at the start
using Power Query.

### Data Cleaning Steps in Excel with Power Query

- Filtered hidden files - auto step performed on obtaining data
- Invoked custom function in M to replace nulls
- Renamed columns for consistency
- Changed column data types to appropriate formats: text, date, integer.
- Cleaned and trimmed text
- Removed duplicates based on 'rider_id' column

### Data Transformation and Processing Steps in Power BI

- Navigation - 'auto' step upon connecting to files from Excel
- Promoted Headers
- Added custom columns: 'ride_length' and 'day_of_week'
- Created an Hour column (_inserted Hour_)

### Finally

Loaded data for analysis.

---
