# University Online Enrollment Analysis

## Project Objective
This project analyzes the online enrollment process of a large public university. The main goal is to understand the student application funnel — from application submission to enrollment — and identify key conversion metrics and bottlenecks. Insights generated are presented to university leadership to support data-driven decision-making for improving enrollment strategies.

## Python Analysis Overview
The data processing and analysis were performed using Python (Jupyter Notebook). Key steps include:

1. **Data Loading**  
   - Imported the enrollment dataset from Excel.  
   - Explored the dataset structure, column types, and sample rows.

2. **Data Cleaning & Type Correction**  
   - Converted date columns to proper datetime format.  
   - Ensured funnel flag columns (`Applied`, `Completed`, `Admitted`, `Matric`, `Enrolled`) were numeric.  

3. **Data Quality Checks**  
   - Checked for duplicate `Application Number`s.  
   - Counted missing values per column.  
   - Verified date consistency (e.g., completion date not earlier than application creation date).

4. **Feature Engineering**  
   - Calculated `days_to_complete` (application completion time).  
   - Calculated `days_to_action` (time to admission decision).  
   - Extracted application month (`app_month`) to analyze temporal patterns.  

5. **Exploratory Funnel Analysis**  
   - Summarized overall counts at each funnel stage.  
   - Calculated conversion rates by **College** and **Admit Type**.  
   - Generated clean datasets (`Parquet`, `CSV`, `Excel`) for further analysis and visualization.  

6. **Output for Dashboarding**  
   - Generated three main summary files for Tableau:  
     - `overall_funnel_summary.xlsx`  
     - `college_funnel_summary.xlsx`  
     - `admit_funnel_summary.xlsx`  

## Tableau Dashboard
To visualize the enrollment funnel and conversion metrics, a **Tableau dashboard** was created. The dashboard includes:

- **Overall Funnel**: Shows the number of students at each stage from Applied → Completed → Admitted → Matric → Enrolled.  
- **Conversion Rates by College**: Highlights which colleges have the highest conversion from application to enrollment.  
- **Conversion Rates by Admit Type**: Shows how admit type (e.g., Regular, Transfer, International) affects enrollment rates.  

<img width="1212" height="803" alt="Screenshot 2026-01-28 at 8 30 29 PM" src="https://github.com/user-attachments/assets/02866a02-2607-410d-b68e-ea42d4a6f267" />

This dashboard allows leadership to quickly identify bottlenecks in the enrollment funnel, compare performance across colleges, and make informed operational decisions.

### Tableau Public Link
[View the Dashboard on Tableau Public]([YOUR_TABLEAU_PUBLIC_LINK_HERE](https://public.tableau.com/views/EnrollmentFunnelAnalysisArizona/EnrollmentFunnelAnalysis?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link))

---

*Project by Saurabh Srivastava*
