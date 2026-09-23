# 🏥 Healthcare Data Analytics Project

A complete end-to-end Python data analytics project analysing patient healthcare utilisation patterns using a real-world dataset of **5,190 patient records**.

---

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Dataset Description](#dataset-description)
- [Project Structure](#project-structure)
- [Setup & Installation](#setup--installation)
- [Running the Notebook](#running-the-notebook)
- [Project Phases](#project-phases)
- [Key Findings](#key-findings)
- [Technologies Used](#technologies-used)
- [License](#license)

---

## Project Overview

This project investigates the factors that influence the number of doctor visits made by patients. Using Python's data science stack, we explore demographic, socioeconomic, and health-related variables to uncover patterns and generate actionable business insights for healthcare providers and policymakers.

---

## Dataset Description

**File:** `Healthcare_Data_Sheet.csv`  
**Records:** 5,190 patients  

| Column | Type | Description |
|--------|------|-------------|
| `visits` | Integer | Number of doctor visits (target variable) |
| `gender` | Categorical | Gender of patient (male/female) |
| `age` | Float (0–1) | Age scaled (multiply by 100 for years) |
| `income` | Float (0–1) | Annual income (scaled) |
| `illness` | Integer | Number of illnesses in past 2 weeks |
| `reduced` | Integer | Days of reduced activity in past 2 weeks |
| `health` | Integer (0–12) | Self-assessed health score |
| `private` | Binary | Has private health insurance (yes/no) |
| `freepoor` | Binary | Has government low-income insurance (yes/no) |
| `freerepat` | Binary | Has repatriated government insurance (yes/no) |
| `nchronic` | Binary | Has non-limiting chronic condition (yes/no) |
| `lchronic` | Binary | Has limiting chronic condition (yes/no) |

---

## Project Structure

```
Healthcare Data Analytics Project/
│
├── Healthcare_Data_Sheet.csv      ← Raw dataset
├── Healthcare_Analysis.ipynb      ← Main Jupyter Notebook (all 8 phases)
├── Healthcare_Project_Report.docx ← Professional project report
├── requirements.txt               ← Python dependencies
├── README.md                      ← Project documentation (this file)
│
├── fig_visits_dist.png            ← Auto-generated charts (saved during notebook run)
├── fig_gender_dist.png
├── fig_age_dist.png
├── fig_income_dist.png
├── fig_illness_dist.png
├── fig_health_dist.png
├── fig_insurance_dist.png
├── fig_chronic_dist.png
├── fig_visits_gender.png
├── fig_visits_age.png
├── fig_visits_illness.png
├── fig_visits_health.png
├── fig_visits_insurance.png
├── fig_visits_chronic.png
├── fig_visits_reduced.png
├── fig_visits_income.png
├── fig_heatmap.png
├── fig_corr_visits.png
└── fig_insights_summary.png
```

---

## Setup & Installation

### Prerequisites
- Python 3.9 or higher
- pip (Python package manager)

### Step 1: Download the project

Download and unzip the project folder into a directory of your choice.

### Step 2: (Optional) Create a virtual environment

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python -m venv venv
source venv/bin/activate
```

### Step 3: Install dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Notebook

```bash
jupyter notebook Healthcare_Analysis.ipynb
```

Or with JupyterLab:

```bash
jupyter lab Healthcare_Analysis.ipynb
```

Then click **Kernel → Restart & Run All** to execute every cell in sequence.

> **Note:** All charts are automatically saved as `.png` files in the project directory during the run.

---

## Project Phases

| Phase | Title | Description |
|-------|-------|-------------|
| 1 | Import & Load | Import Python libraries and load the CSV dataset |
| 2 | Understand Data | Explore shape, columns, dtypes, describe, missing values |
| 3 | Clean Data | Remove duplicates, fix data types, encode categoricals |
| 4 | Univariate EDA | Individual distributions for every variable |
| 5 | Bivariate Analysis | Relationships between variables and doctor visits |
| 6 | Correlation Analysis | Heatmap + bar chart of feature correlations |
| 7 | Business Insights | 10 quantified, actionable insights |
| 8 | Conclusion | Summary, recommendations, and limitations |

---

## Key Findings

1. **Doctor visits are right-skewed** — most patients visit 0–2 times; a small group drives majority of demand.
2. **Illness count** is the strongest predictor of healthcare utilisation (r ≈ +0.30).
3. **Patients aged 65+** visit significantly more than younger cohorts.
4. **Females** visit more frequently than males on average.
5. **Limiting chronic conditions** add an average of ~1–2 extra visits per patient.
6. **Government low-income (freepoor) insured** patients have the highest visit frequency — reflecting greater health burden.
7. **Low self-assessed health scores** reliably identify high-utilisation patients.
8. **Days of reduced activity** is a strong proxy for healthcare severity and demand.
9. **Lower-income patients** exhibit higher visit rates, highlighting social health inequities.
10. **Compound risk patients** (chronic condition + poor self-rated health) visit nearly twice as often as healthy patients.

---

## Technologies Used

| Library | Version | Purpose |
|---------|---------|---------|
| Python | 3.9+ | Core programming language |
| Pandas | 2.2.2 | Data loading, cleaning, manipulation |
| NumPy | 1.26.4 | Numerical operations |
| Matplotlib | 3.9.0 | Base charting |
| Seaborn | 0.13.2 | Statistical visualisation |
| Jupyter Notebook | 7.2.0 | Interactive analysis environment |

---

## License

This project is released for educational and research purposes.  
Dataset adapted from publicly .

---

