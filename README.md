# Startup Funding Analysis (2024–2025)

An end-to-end data analysis portfolio project covering ETL, data cleaning, exploratory data analysis (EDA), and interactive data visualization using a Crunchbase startup dataset.

## 📊 Interactive Dashboard

**[View Tableau Dashboard →](https://public.tableau.com/app/profile/shengmin.hung/viz/StartupFundingAnalysis_17771540311390/StartupFundingAnalysis20242025)**

![Dashboard Preview](https://public.tableau.com/static/images/St/StartupFundingAnalysis_17771540311390/StartupFundingAnalysis20242025/1.png)

---

## Project Overview

**Dataset:** Crunchbase startup data — 1,576 companies, 32 columns  
**Scope:** Funding activity in 2024 and 2025 only  
**Goal:** Identify trends in startup funding across industries, geographies, and time periods

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python / pandas | ETL, data cleaning, EDA |
| Google Colab | Development environment |
| Tableau Public | Interactive dashboard |
| GitHub | Version control & hosting |

---

## Project Structure

```
startup_funding_analysis/
├── startup_funding_analysis.ipynb   # Main notebook (ETL + EDA)
├── Startup_Data__Startup.csv        # Raw dataset
├── startup_funding_cleaned.csv      # Cleaned dataset
└── README.md
```

---

## Key Findings

### Industry Funding
- **AI & Data dominates** with 676 startups and $17.2B total funding, but median deal size is only $4.7M — a few mega-deals drive the average
- **CleanTech & Energy** has the highest median deal size at $19.9M despite only 41 companies — most capital-efficient sector
- **E-Commerce & Retail** is the weakest performer with a $1.1M median deal size

### Geography
- **West Coast** leads with 530 startups and $17.5B total funding
- **Silicon Valley** alone accounts for 175 startups and $8.2B — a dense high-value cluster
- **New England** has the highest median deal size ($10M) driven by Boston biotech

### 2024 → 2025 Trends
| Metric | 2024 | 2025 | Change |
|---|---|---|---|
| Deal Count | 822 | 1,005 | +22% |
| Total Funding | $17.2B | $30.8B | +79% |
| Median Deal Size | $2.5M | $6.0M | +139% |

- Deal sizes are growing **much faster** than deal volume — 2025 is a year of larger, more concentrated bets
- **AI & Data** median nearly doubled: $3.25M → $6.3M
- **CleanTech** median nearly tripled: $12.25M → $34.65M
- **Media & Marketing** collapsed: $1.19B → $83M total funding

---

## Data Cleaning Highlights

- Converted date columns from `object` to `datetime64`
- Converted funding amount columns from `object` to `float64`
- Extracted `Founded_Year` and `Last_Funding_Year` from date columns
- Split `Headquarters_Regions` into `Region_Local`, `Region_Mid`, `Region_Broad`
- Extracted `State` from `Headquarters_Location` for geographic mapping
- Created `Industry_Category` column with 9 standardized categories
- Filtered out records with missing funding amounts (251 records)

---

## Dashboard Features

1. **Industry Funding Overview** — Total funding by industry (log scale bar chart)
2. **Geographic Map** — Startup concentration and funding by US state (filled map)
3. **2024 vs 2025 Comparison** — Median deal size growth by industry (side-by-side bar chart)
4. **Funding Distribution** — Spread and outliers by industry (box plot)
