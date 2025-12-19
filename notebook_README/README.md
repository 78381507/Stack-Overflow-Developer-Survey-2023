# Global Developer Trends Analysis  
Stack Overflow Developer Survey 2023

**Author:** François Tilkin  
**Role:** Data Analyst  
**Context:** IBM Data Analyst Professional Certificate (Coursera)  
**Deliverables:**  
- Executive slide deck (PDF – 19 slides)  
- Interactive dashboards (Looker Studio)  
- Reproducible Python analysis  

---

## 1. Project overview

This project analyzes global developer trends using the Stack Overflow Developer Survey 2023.
The objective is to transform large-scale survey data into **decision-oriented insights**
relevant for business stakeholders.

The analysis focuses on:
- Compensation distribution and benchmarking
- Remote vs hybrid vs on-site work preferences
- Relationship between professional experience and job satisfaction
- Current technology adoption vs future demand (languages, databases, platforms)

The project is designed as a **portfolio-grade case study**, emphasizing clarity,
reproducibility and business relevance rather than purely academic exploration.

---

## 2. Business framing

### Business context

Technology-driven organizations face multiple challenges:
- Hiring in a competitive and fast-evolving talent market
- Anticipating future skill demand beyond current stacks
- Benchmarking compensation in highly skewed salary distributions
- Retaining talent in a remote-first environment

This project answers concrete business questions using survey data at scale,
with the goal of supporting **strategic decision-making**.

---

### Business questions & analytical translation

| Business question | Analytical approach | Key metrics | Business value |
|------------------|--------------------|------------|----------------|
| Which technologies are most relevant **today**? | Adoption analysis | Top-N “Have worked with” | Align hiring with market reality |
| Which skills should be **anticipated**? | Preference analysis | Top-N “Want to work with” | Future-proof recruitment & training |
| Are average salaries misleading? | Distribution analysis | Median, percentiles, skewness | Reliable compensation benchmarks |
| Does experience impact job satisfaction? | Group comparison | Mean & variability by experience band | Retention and career path design |
| Is remote work still a differentiator? | Frequency analysis | Remote / Hybrid / On-site split | Employer branding & policy |

---

### Stakeholders

- **HR & Talent Acquisition:** compensation, skills prioritization  
- **CTO / Tech leadership:** technology roadmap, learning strategy  
- **Management:** workforce planning and long-term capability building  

---

### Success criteria

The project is considered successful if it:
- Uses **robust statistics** (median, percentiles over raw averages)
- Clearly separates **current reality** from **future intent**
- Is fully **reproducible**
- Can be consumed by non-technical stakeholders (slides, dashboards)

---

## 3. Dataset

- **Source:** Stack Overflow Developer Survey 2023  
- **File:** `data/survey_data_updated.csv`  
- **Size:** 18,845 rows × 114 columns  

### Key variables used
- Compensation: `ConvertedCompYearly`, `CompTotal`
- Experience: `YearsCodePro`
- Satisfaction: `JobSat` (0–10)
- Work mode: `RemoteWork`
- Tech stack (multi-select):
  - `LanguageHaveWorkedWith`, `LanguageWantToWorkWith`
  - `DatabaseHaveWorkedWith`, `DatabaseWantToWorkWith`
  - `PlatformHaveWorkedWith`, `PlatformWantToWorkWith`
- Demographics: `Age`, `EdLevel`, `Country`

---

## 4. Methodology

1. Data loading and profiling  
2. Data cleaning:
   - Type conversion
   - Missing value assessment
   - Outlier awareness (heavy-tailed compensation)
3. Feature engineering:
   - Parsing multi-select columns
   - Binning experience levels
4. Exploratory data analysis:
   - Distributions and rankings
   - Group comparisons
5. Visualization and delivery:
   - Executive slide deck
   - Interactive dashboards (Looker Studio)

The workflow follows a **business-first EDA approach**:
questions → metrics → interpretation → action.

---

## 5. Key findings

### Compensation distribution
- Compensation is strongly right-skewed.
- Median income (~65k) is significantly lower than the mean (~85k),
  highlighting the importance of robust statistics.
- Extreme outliers confirm that averages are unreliable for benchmarking.

**Business implication:**  
Median and percentile-based benchmarks should be preferred in compensation discussions.

---

### Remote work preferences
- Remote and hybrid work dominate.
- Fully on-site roles represent a minority.

**Business implication:**  
Remote flexibility is no longer a perk but a baseline expectation.

---

### Experience & job satisfaction
- Job satisfaction slightly increases and stabilizes with experience.
- Senior profiles show lower variability in satisfaction scores.

**Business implication:**  
Experience contributes to expectation alignment and retention stability.

---

### Technology trends
- Current usage is concentrated around mature technologies
  (JavaScript, SQL, Python, TypeScript).
- Future preferences show growing interest in modern, scalable tools
  (Go, Rust, cloud-native databases).

**Business implication:**  
Hiring only on past stacks risks misalignment with future talent expectations.

---

## 6. Deliverables

- **Executive slides:** `reports/IBM_TRAVAIL_FINAL_C9.pdf`
- **Dataset:** `data/survey_data_updated.csv`
- **Dashboards (Looker Studio):**
  - Current technology usage – *link to add*
  - Future technology trends – *link to add*
  - Demographic overview – *link to add*

---

## 7. Repository structure

├─ data/
│ └─ survey_data_updated.csv
├─ notebooks/
│ ├─ 01_data_quality_checks.ipynb
│ ├─ 02_eda_tech_trends.ipynb
│ ├─ 03_compensation_experience_jobsat.ipynb
│ └─ 04_exports_for_looker.ipynb
├─ reports/
│ └─ IBM_TRAVAIL_FINAL_C9.pdf
├─ outputs/
│ └─ looker_exports/
├─ README.md
└─ requirements.txt

---

## 8. Reproducibility

1. Create a virtual environment  
2. Install dependencies from `requirements.txt`  
3. Run notebooks in numerical order  

All transformations and exports are documented and reproducible.

---

## 9. Limitations

- Survey data is self-reported and subject to bias.
- Compensation contains extreme outliers.
- Multi-select fields measure mentions, not depth of expertise.
- Cross-sectional data: no causal inference.

---

## 10. Next steps

- Segment analysis by geography and role
- Multi-year trend comparison
- Predictive modeling for compensation drivers
- Executive “decision memo” summarizing actions in one page



























