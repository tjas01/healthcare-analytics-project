# Healthcare ED Analytics (Canada, Apr 2024–Mar 2025)

A Power BI analytics project demonstrating healthcare data analysis, responsible use of public health-data principles (OCAP-aligned handling of aggregate datasets), and Fraser Health–style executive reporting.  
Built using publicly available Emergency Department (ED) summary data for Apr 2024–Mar 2025.

The project converts raw ED summaries into actionable, visually consistent insights aligned with health authority reporting standards (CAADSI, CIHI, PHSA).

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `healthcare-ed-analytics-apr2024-mar2025.pbix` | Main Power BI report (Pages 1 & 2 complete) |
| `emergency-department-visits-apr-2024-mar-2025-data-tables-en.xlsx` | Source dataset |
| `color-palette.json` | Custom clinical theme |
| `README.md` | Documentation |
| `/Screenshots/` | Dashboard screenshots |

---

## 📸 Dashboard Screenshots

### **Page 1 — ED Overview & Performance**
![Page 1](./Screenshots/page1.png)

---

### **Page 2 — Top Clinical Conditions & Drivers**
![Page 2](./Screenshots/page2.png)

---

## 🧠 Skills Demonstrated  
*(Aligned with Fraser Health Data Analyst expectations)*

### Health Data Literacy
- Understanding ED concepts: **CTAS categories**, **Admitted vs Discharged**, **LOS P50/P90**, **age-group classifications**, **monthly volume structures**
- Ability to interpret health-system KPIs and their operational meaning
- Working with **public, aggregate health data** in an OCAP-aligned manner (no identifiers, no re-identification risk, respectful use of summary data)

### Healthcare BI & Analytics
- Advanced Power BI modeling and DAX in a clinical context  
- IBCS-aligned design for clarity and consistency  
- Visuals designed for ED operations and executive review  
- Interpretation of ED drivers, throughput, and clinical demand patterns  

### Data Modeling
- Multi-table integration across annual & monthly ED summaries  
- Dimensional modeling via `DimDate` and `DimProvince`  
- Clean relationship behavior for time, geography, and ED cohorts  

### KPI Design & Interpretation
- Median LOS (P50) and 90th percentile LOS (P90) throughput analytics  
- Acuity Mix: **Admitted vs CTAS I–III vs CTAS IV–V**  
- ED volumes split by province, age group, sex, and disposition  
- Clinical problem–level analysis using Top 10 ED problems  

### UI/UX & Theme Development
- Custom JSON theme matching a clinical reporting palette  
- Clean, IBCS-style minimal-ink design  
- Consistent layout, spacing, font hierarchy, and grouping  

### Version Control & Documentation
- Well-structured repository for recruiters and hiring managers  
- Self-contained PBIX + theme + dataset  
- Clear README with model view, screenshots, and explanation  

---

## 🧩 Dataset Overview

### `ed_province_annual_summary`
Annual ED metrics per province:
- ED volumes (Total, Admitted, CTAS I–III, CTAS IV–V)  
- Median LOS (hours)  
- LOS P90 (hours)  
- Province/Territory  

### `fact_ed_visits_monthly`
Monthly visit distributions:
- Age groups (0–4, 5–19, 20–64, 65+, All)  
- Month  
- Province/Territory  
- Sex  

### `ed_top10_problems`
- Main problem  
- Number of ED visits  
- Admitted (%) / Non-admitted (%)  
- ED LOS P90  

### Dimensions
- `DimDate` — Calendar metadata  
- `DimProvince` — Province metadata  

---

## 🗺️ Data Model View

```mermaid
flowchart LR
  DimDate --> fact_ed_visits_monthly
  DimProvince --> fact_ed_visits_monthly
  DimProvince --> ed_province_annual_summary

  subgraph ClinicalProblems
    ed_top10_problems
  end
ed_top10_problems intentionally remains disconnected (summary-level table) and is used only for Page 2’s clinical insights.

## 📊 Report Pages

---

# **Page 1 — ED Overview & Performance (Completed)**

A high-level operational view of ED demand, throughput, acuity, and patient mix.

### **Key KPIs**
- Total ED Visits  
- Total Admitted  
- Total Discharged (CTAS I–III)  
- Median LOS (CTAS I–III)  
- LOS P90 (CTAS I–III)  
- Acuity Mix  

### **Main Visuals**
- Monthly ED Visits (line)  
- Admitted visits by province (clustered bar)  
- CTAS I–III discharged by province (clustered bar)  
- Age distribution by province (stacked bar)  
- Acuity Mix composition bar  
- Province + Month slicers  

---

# **Page 2 — Top Clinical Conditions & Drivers (Completed)**

A clinical drill-down into the top 10 ED problems driving patient flow and throughput.

### **Key KPIs**
- Total ED Visits (Top 10 Problems)  
- Overall Admission Rate  
- Overall Non-Admission Rate  

### **Main Visuals**
- **Admission vs Discharge Breakdown** (100% stacked bar)  
- **Admission Patterns Across Top Problems** (scatter plot: admitted% vs non-admitted%)  
- **Length of Stay (P90) by Problem** (horizontal bar)  
- **Top 10 Problems Table** (problem + visit counts)  
- Shared Province + Month slicers  

This page highlights clinical drivers behind ED utilization, identifies conditions associated with higher admission burden, and surfaces problem-level throughput patterns.

---

## 🎨 Theme & Color Palette

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
| Card Background | `#F7F9FC` |
| Page Background | `#E9EDF5` |
| Divider Grey | `#D3D9E3` |

### Text Colors
| Purpose | Hex |
|--------|-----|
| Dark Text | `#2F3145` |
| Medium Grey Text | `#6B7180` |

The palette is designed to be clean, clinical, and accessible, following IBCS clarity principles and healthcare reporting standards.

---

## ✅ Summary

This project demonstrates capability in:
- Healthcare data analysis and clinical KPI interpretation  
- OCAP-aligned use of public health datasets  
- ED performance and throughput analytics  
- IBCS-disciplined dashboard design  
- Visualizing clinical drivers behind ED utilization  
- Building polished, recruiter-ready BI portfolio artifacts  

This transforms complex ED data into an executive-quality analytics solution suitable for real healthcare organizations.
