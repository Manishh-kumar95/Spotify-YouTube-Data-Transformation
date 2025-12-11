# 🎵 Spotify + YouTube Music: Data Cleaning & Transformation

![Power Query](https://img.shields.io/badge/Tool-Power_Query-green?style=for-the-badge&logo=powerquery)
![Data Analysis](https://img.shields.io/badge/Focus-Data_Cleaning-blue?style=for-the-badge)
![Power BI](https://img.shields.io/badge/Status-Analysis_Ready-yellow?style=for-the-badge&logo=powerbi)

## 🎯 Project Overview
This project focuses on the detailed cleaning and transformation of the Spotify-YouTube dataset. The main goal was to take raw, messy data and turn it into a clean, structured format that is ready for analysis in Power BI.

## 🛠️ Tools Used
* **Power Query:** Used for all data cleaning and transformation steps.
* **Power BI:** The final destination for the cleaned data.

---

## 🧹 Key Cleaning Steps
I followed a step-by-step process to fix the data:

### 1. Handling Missing Values
* **Problem:** Key columns like `Views` and `Likes` had missing numbers (Null values).
* **Solution:** I replaced these missing values with **0**.
* **Reason:** This ensures we don't lose data rows and allows for accurate calculations (since null usually means zero engagement).

### 2. Fixing Merged Columns
* **Problem:** Columns like `Spotify_Info` and `Youtube_Info` had multiple pieces of data combined in one cell.
* **Solution:** I used the **Split Column** feature to separate them into distinct fields.
* **Reason:** This restores important details like IDs and links so they can be used properly.

### 3. Correcting Data Types
* **Problem:** Numbers (like `Views`, `Tempo`, `Energy`) were stored as "Text" because they contained symbols or letters.
* **Solution:** I removed the text characters and changed the type to **Decimal Number** or **Whole Number**.
* **Reason:** You cannot perform math (Sum/Average) on text; this step made analysis possible.

### 4. Standardizing Text
* **Problem:** Column names and Artist names had messy formatting (inconsistent capital letters).
* **Solution:** I converted all column names to **lowercase with underscores** and made Artist names **Capitalized Each Word**.
* **Reason:** This makes the dataset look professional and prevents errors in Power BI formulas.

### 5. Removing Duplicates
* **Problem:** Some tracks appeared more than once, which would double-count the views.
* **Solution:** I removed duplicate rows based on the unique `Track ID`.
* **Reason:** This ensures the final numbers are 100% accurate.

---

## ✅ Final Result
The data is now:
* **Clean:** No missing values or errors.
* **Structured:** Columns are split and organized logically.
* **Ready:** Fully optimized for Power BI dashboards.

---
