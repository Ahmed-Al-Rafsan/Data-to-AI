<div align="center">

# 🚀 Data-to-AI

**My journey from Data Analyst to AI Engineer — built in public, one project at a time.**

![Stage](https://img.shields.io/badge/current%20stage-Data%20Engineering%20Foundations-8A6A2F)
![Projects](https://img.shields.io/badge/projects-2-2E7D32)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/status-actively%20building-2E7D32)

[Portfolio](https://ahmed-al-rafsan.github.io/) · [LinkedIn](https://www.linkedin.com/in/ahmed-al-rafsan-/) · [YouTube](https://www.youtube.com/@AhmedAlRafsan)

</div>

---

## 🧭 The path

```
Data Analyst  ──►  Analytics Engineer  ──►  Data Engineer  ──►  AI Engineer
   ▲ you are here
```

This repo is the practice ground. Every time I learn something new — a library, a tool, a technique — I build a small, honest project with it and push it here. Each project gets its own numbered folder and its own README, so the commit history shows how I actually learn, not just the polished end result.

---

## 📚 Projects

| # | Project | Stage | Skills practised | Status |
|--:|---|---|---|---|
| 01 | [**Auto Sales — Data Cleaning & Validation**](./01-auto-sales-data-cleaning) | Data Analyst | pandas · deduplication · type validation · quarantine tables · lookup joins · Matplotlib | ✅ Complete |
| 02 | [**Retail Sales ETL & Data Quality Pipeline**](./02-retail-sales-etl-data-quality) | Data Engineering fundamentals | Python · pandas · CSV/JSON · data-quality checks · logging · exception handling | ✅ Complete |

*New rows are added as I build. Newest project goes at the bottom.*

### Build 01 · Auto Sales

A messy sales export of 2,723 order lines, cleaned with a pipeline where **no row is silently deleted**: invalid rows are quarantined and the totals reconcile to the cent. It answers three questions on shipped sales — top product line, top country and peak month.

➡ [Read the full README](./01-auto-sales-data-cleaning/README.md)

---

### Latest build — 02 · Retail Sales ETL & Data Quality

A deliberately small synthetic retail input (58 rows) becomes two traceable outputs: 53 accepted orders and 3 quarantined orders, after 2 exact duplicates are removed. Practised Python/pandas transformations, CSV/JSON exports, logging, and documenting data-quality decisions without inventing missing quantities or prices.

➡ [Explore the notebook, architecture and validation notes](./02-retail-sales-etl-data-quality/README.md)

---

## 🗺 What's planned

These are the next steps on the path, not finished work. Each will get its own numbered folder when it is built.

| Stage | Planned practice |
|---|---|
| **Data Analyst** | Outlier checks; more cleaning and EDA builds |
| **Analytics Engineer** | Rebuild project 01 in SQL, then as dbt models with tests (`unique`, `not_null`, `relationships`) |
| **Data Engineer** | Turn pipeline steps into tested functions (`pytest`) that can run on a schedule |
| **AI Engineer** | Machine-learning and LLM builds on top of clean, documented data |

---

## 🗂 Repository structure

```
Data-to-AI/
├── README.md                          # this journey map
├── 01-auto-sales-data-cleaning/       # Data Analyst stage
│   ├── README.md
│   ├── data/
│   ├── images/
│   ├── output/
│   ├── Mini_Project_1.ipynb
│   └── requirements.txt
└── 02-retail-sales-etl-data-quality/  # Python ETL fundamentals
```

Each project folder is self-contained: its own README, data, code and `requirements.txt`.

---

## 🔗 More of my work

Larger portfolio projects — employee attrition, RFM customer segmentation, fashion retail intelligence, and the school-targeting capstone — are on my [portfolio website](https://ahmed-al-rafsan.github.io/).

---

<div align="center">

**Ahmed Al Rafsan** · Melbourne, Australia
*Engineering roots. People experience. A passion for finding the story in data.*

</div>
