Healthcare ED Analytics (Canada, Apr 2024–Mar 2025)

A Power BI analytics project demonstrating health‑systems data analysis, correct use of healthcare terminology, OCAP‑aligned handling of Indigenous‑related insight boundaries (no individual‑level data, no identifiers, respecting data sovereignty principles), and Fraser Health–style executive reporting.  
Built using publicly available Emergency Department (ED) summary data for Apr 2024–Mar 2025.

This project illustrates the ability to analyze health‑sector datasets, interpret LOS metrics, acuity groupings, CTAS levels, provincial ED trends, and communicate findings in a manner aligned with health‑authority expectations and responsible data principles.

---

SKILLS DEMONSTRATED  
(Aligned with Fraser Health CAADSI expectations)

Health Data Literacy
- Understanding of ED terminology: CTAS levels, LOS P50/P90, admitted vs discharged pathways  
- Correct interpretation of age‑grouped and sex‑segmented ED datasets  
- Ability to translate raw provincial aggregates into operational insights  
- Awareness of OCAP fundamentals: no re‑identification risk, respecting data stewardship, using only public, aggregate data appropriately

Healthcare BI & Analytics
- Advanced Power BI modelling and DAX for health‑system KPIs  
- IBCS‑aligned KPI construction and clinical throughput visualization  
- Clear, accessible communication of ED performance drivers  
- Executive‑ready dashboards used for operational decisions

Data Modeling
- Multi‑table integration of annual + monthly ED summaries  
- Dimensional modelling with DimDate and DimProvince  
- Clean aggregation behavior across provinces, months, and age groups  

KPI Design & Interpretation
- Median LOS and LOS P90 throughput analytics  
- Acuity Mix (Admitted vs CTAS I–III vs CTAS IV–V)  
- ED volume trends by province, age, sex, and discharge group  

UI/UX & Theming
- Custom JSON theme for clinical reporting  
- Structured, consistent, minimal‑ink IBCS layouts  
- Modern, clinical visual hierarchy  

Version Control & Documentation
- Clear repo structuring  
- Recruiter‑friendly README  
- PBIX + theme + dataset organized for reproducibility  

---

REPOSITORY CONTENTS
healthcare-ed-analytics-apr2024-mar2025.pbix – Main report (Pages 1 and 2 complete)
emergency-department-visits-apr-2024-mar-2025-data-tables-en.xlsx – Source dataset
color-palette.json – Custom theme
README.md – Documentation
LICENSE – License file

---

DATASET OVERVIEW

ed_province_annual_summary
- ED volumes (Total, Admitted, CTAS I–III, CTAS IV–V)
- Median LOS (hours)
- LOS P90 (hours)
- Province/Territory

fact_ed_visits_monthly
- Age‑grouped visit volumes (0–4, 5–19, 20–64, 65+, All)
- Month
- Province/Territory
- Sex

ed_top10_problems
- Main problem
- Number of ED visits
- Admitted (%) and Non‑admitted (%)  
- ED LOS (90% spent less)

Dimensions
- DimDate for month‑level filtering
- DimProvince for regional filtering

---

DATA MODEL VIEW
(Diagram represented in README via Mermaid)

DimDate → fact_ed_visits_monthly  
DimProvince → fact_ed_visits_monthly  
DimProvince → ed_province_annual_summary  
ed_top10_problems (stand‑alone clinical summary table)

---

REPORT PAGES

PAGE 1 — ED Overview & Performance
Operational ED view across provinces.

Key KPIs
- Total ED Visits  
- Total Admitted  
- Total Discharged (CTAS I–III)  
- Median LOS (CTAS I–III)  
- LOS P90 (CTAS I–III)  
- Acuity Mix (Admitted vs CTAS I–III vs CTAS IV–V)

Main Visuals
- Monthly ED Visits (line, sex split)
- Admitted visits by province and sex
- CTAS I–III discharged by province and sex
- Province‑level age distribution
- Acuity Mix bar
- Month + Province slicers

PAGE 2 — Top Clinical Conditions & Drivers
Clinical problem‑level insight page.

Key KPIs
- Total ED Visits (Top 10 Problems)
- Overall Admission Rate
- Overall Non‑Admission Rate

Main Visuals
- Admission vs Discharge Breakdown (100% stacked bar)
- Admission Patterns Across Top Problems (scatter: admitted% vs non‑admitted%)
- Length of Stay (P90) by Problem (horizontal bar)
- Top 10 Problems table
- Shared Month + Province slicers

All visuals follow OCAP‑aligned principles:  
No individual‑level data, no identifiable attributes, all metrics aggregated, and all insights derived only from publicly released summary data.

---

THEME & COLOR PALETTE

Primary Accent Colors
- #6A8BF7 – Accent Blue
- #3E4A75 – Deep Blue

Supporting Colors
- #AFC9FF – Light Ice Blue
- #8FA4C8 – Blue‑Grey
- #5D6C9E – Steel Blue

Backgrounds
- #F7F9FC – Card background
- #E9EDF5 – Page background
- #D3D9E3 – Divider

Text
- #2F3145 – Dark
- #6B7180 – Medium Grey

---

SUMMARY

This project demonstrates capability in:
- Healthcare data modelling and ED performance analysis  
- OCAP‑aligned handling of public health datasets  
- Building clean, clinical, IBCS‑compliant dashboards  
- Communicating ED flow, acuity, LOS, and problem‑level drivers  
- Designing a polished, professional healthcare analytics portfolio piece  
