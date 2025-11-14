# Healthcare ED Analytics (Canada, Apr 2024–Mar 2025)

A Power BI analytics project demonstrating expertise in healthcare data analysis, IBCS-compliant dashboard design, KPI construction, and executive reporting.  
Built using publicly available Emergency Department (ED) summary data for Apr 2024–Mar 2025.

This project converts raw provincial ED aggregates into actionable, visually consistent insights aligned with health authority reporting standards.

---

## Skills Demonstrated

### Data Analytics & BI
- Enterprise-grade dashboard development using Power BI Desktop  
- IBCS-based layout, labeling, and visual hierarchy  
- KPI card design, slicer logic, and interactive visuals  
- Executive storytelling with trend, distribution, and composition views

### Data Modeling
- Multi-table integration across annual and monthly ED summary datasets  
- Dimensional modeling using `DimDate` and `DimProvince`  
- Correct relationship configuration for time-series and provincial analysis  
- Ensuring clean aggregation behaviors across provinces and months

### KPI Design & Interpretation
- Median LOS (P50) and LOS P90 (worst-case throughput)  
- Acuity Mix (Admitted vs CTAS I–III vs CTAS IV–V)  
- ED volumes by province, age, sex, and discharge category  
- Clear, concise, IBCS-aligned KPI wording and unit presentation

### UI/UX & Theme Development
- Custom JSON Power BI theme (`color-palette.json`)  
- Consistent color hierarchy and contrast for healthcare reporting  
- Minimal-ink IBCS formatting: short labels, clean spacing, and clear grouping  
- Modern, clinical-style dashboard design

### Version Control & Documentation
- Structured repository layout  
- Clean, recruiter-friendly README  
- PBIX + theme + dataset maintained together for reproducibility

---

## Repository Contents

| File | Description |
|------|-------------|
| `healthcare-ed-analytics-apr2024-mar2025.pbix` | Main Power BI report (Page 1 complete; Pages 2–3 WIP) |
| `emergency-department-visits-apr-2024-mar-2025-data-tables-en.xlsx` | Source dataset |
| `color-palette.json` | Custom Power BI theme |
| `LICENSE` | License file |
| `README.md` | Documentation |

---

## Dataset Overview

### `ed_province_annual_summary`
Annual provincial ED metrics:
- ED volumes (Total, Admitted, CTAS I–III, CTAS IV–V)  
- Median LOS (hours) per category  
- 90th percentile LOS (hours) per category  
- Province/Territory

### `fact_ed_visits_monthly`
Monthly ED distributions:
- Visits by age groups (0–4, 5–19, 20–64, 65+, All)  
- Month  
- Province/Territory  
- Sex

### `ed_top10_problems`
- Main problem  
- Number of ED visits  
- Admitted (%) and Non-admitted (%)  
- ED LOS (90% spent less)

### Dimensions
- `DimDate` for calendar filtering  
- `DimProvince` for regional filtering

---

## Report Pages

### Page 1 — ED Overview & Performance (Completed)

High-level view of ED demand, throughput, and patient mix across Canada.

#### Key KPIs (IBCS-compliant)
- Total ED Visits  
- Total Admitted  
- Total Discharged (CTAS I–III)  
- Median LOS (CTAS I–III)  
- LOS P90 (CTAS I–III)  
- Acuity Mix (Admitted vs CTAS I–III vs CTAS IV–V)

#### Main Visuals
- Monthly ED Visits trend  
- Admitted visits by province and sex  
- CTAS I–III discharged by province and sex  
- Province-level age distribution (0–4, 5–19, 20–64, 65+)  
- Acuity Mix composition bar  
- Month and Province slicers

---

### Page 2 — Wait Times & Flow (Under Construction)

Planned:
- LOS comparisons across categories and provinces  
- LOS vs volume (bottleneck analysis)  
- P50/P90 throughput analysis for system strain  
- Interpretation of performance across ED patient groups

---

### Page 3 — Patient Profile & Equity Lens (Under Construction)

Planned:
- Age/sex distribution across provinces  
- Demographic trends across ED visits  
- Pediatric vs older adult burden  
- Equity-lens interpretation where supported by data

---

## Theme & Color Palette

The report uses a custom healthcare theme with the following hex codes:

### Primary Accent Colors
| Purpose | Hex |
|--------|-----|
| Accent Blue (main) | `#6A8BF7` |
| Deep Blue (secondary) | `#3E4A75` |

### Supporting Visualization Colors
| Purpose | Hex |
|--------|-----|
| Light Ice Blue | `#AFC9FF` |
| Blue-Grey | `#8FA4C8` |
| Steel Blue | `#5D6C9E` |

### Backgrounds & Cards
| Purpose | Hex |
|--------|-----|
| Soft White (cards) | `#F7F9FC` |
| Ultra-Light Grey (background) | `#E9EDF5` |
| Medium Divider Grey | `#D3D9E3` |

### Text Colors
| Purpose | Hex |
|--------|-----|
| Dark Text | `#2F3145` |
| Medium Grey Text | `#6B7180` |

The palette is designed to be clean, clinical, and accessible, following IBCS clarity principles.

---

## Summary

This project demonstrates the ability to:

- Understand and model healthcare summary datasets  
- Generate meaningful ED performance KPIs without patient-level data  
- Build clean, executive-ready dashboards with IBCS discipline  
- Apply a cohesive visual identity through a custom theme  
- Present a polished, recruiter-oriented analytics project

It transforms a complex ED dataset into a high-quality, professional BI artifact suitable for real-world healthcare analytics roles.
