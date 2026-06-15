# Hospital Data Cleaning and Analytics Project

This project focuses on preprocessing, cleaning, and performing initial analytical calculations on a raw hospital dataset using Python and Pandas. The final structured data has been exported as a clean CSV file ready for downstream analysis or visualization.

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Key Features & Workflow](#key-features--workflow)
- [Installation & Setup](#installation--setup)
- [Data Cleaning Steps](#data-cleaning-steps)
- [Calculations & Feature Engineering](#calculations--feature-engineering)
- [Output File](#output-file)

## 🔍 Project Overview
Raw medical and hospital datasets often contain missing entries, duplicate records, and inconsistent formatting. This project implements a rigorous data-cleaning pipeline to ensure data integrity, handle healthcare terminology accurately, and engineer useful metrics for operational insights.

## 🚀 Key Features & Workflow
- **Deduplication:** Identified and removed redundant patient or clinical records.
- **Imputation:** Filled null values using context-aware strategies (e.g., median values for continuous metrics, "Unknown" for missing categorical metadata).
- **Type Casts:** Formatted date columns, numeric metrics, and categorical flags into their appropriate data types.
- **Domain Alignment:** Researched healthcare terminology to validate, map, or correct column names and codes (e.g., ICD codes, department names).
- **Feature Engineering:** Performed mathematical and time-based calculations to derive new insights.


## 🧹 Data Cleaning Steps
The automated pipeline applies the following transformations:
1. **Removing Duplicates:** Dropped exact duplicates and conflicting rows using `df.drop_duplicates()`.
2. **Handling Missing Values:** 
   - Used median values for skewed hospital metrics (e.g., Length of Stay).
   - Applied forward-filling or placeholder strings for missing demographic data.
3. **Data Type Formatting:** 
   - Converted admission and discharge strings to standard `datetime64` objects.
   - Handled categorical columns securely to optimize memory usage.

## 🧮 Calculations & Feature Engineering
The script calculates the following operational healthcare metrics:
* **Length of Stay (LOS):** Calculated directly from admission and discharge timestamps.
* **Financial Calculations:** Aggregated total billing, applied insurance discounts, and computed net costs.
* **Patient Segmentation:** Grouped clinical outcomes and age brackets for simplified reporting.

## 💾 Output File
The final, clean dataset is exported in the root directory:
* **Filename:** `hospital_data_cleaned.csv`
* **Format:** Comma-Separated Values (CSV), UTF-8 encoded, index omitted.

