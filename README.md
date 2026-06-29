# 🏙️ Pune Real Estate Market Trends — Project 4

> **Google Sheets analysis of 1,932 RERA-registered projects and 340 property transactions in Pune, using real Maharashtra government open data.**

---

## 📌 Overview

This is the fourth project in an ongoing data analysis series built entirely in **Google Sheets**. It marks the step up from clean teaching datasets to **real, unmodified government open data** — with all the messiness, inconsistencies, and domain knowledge that entails.

The dataset comes from the **Maharashtra Real Estate Regulatory Authority (RERA)** open data portal, covering registered residential real estate projects across Pune district and property transaction records from the Erandwane locality.

---

## 📂 Datasets

| Dataset | Source | Records | Scope |
|---|---|---|---|
| RERA Project Registry | Maharashtra RERA Open Data Portal | 1,932 projects | Pune district |
| Property Transactions | RERA Transaction Data | 340 transactions | Erandwane locality |

---

## 📊 Key Statistics

### Project Registry

| Status | Count | Share |
|---|---|---|
| 🟢 Active | 800 | 41.4% |
| ✅ Completed | 721 | 37.3% |
| 🔴 Lapsed | 401 | 20.8% |
| ⚫ De-registered | 9 | 0.5% |

**Peak registration year:** 2017 — 412 projects registered as developers rushed to comply with the newly enacted RERA law.

### Top Localities by Project Count

| Rank | Locality | Projects |
|---|---|---|
| 1 | Kothrud | 166 |
| 2 | Punawale | 116 |
| 3 | Kharadi | 100 |
| 4 | Erandwane | 80 |

### Property Transactions (Erandwane)

- **Most common deal type:** Agreement to Sell — 61 transactions
- **Average deal value:** ₹66.5 Lakhs
- **Median deal value:** ₹41.3 Lakhs
- **Most active price band:** ₹25L – ₹1Cr

> The gap between mean and median signals a right-skewed distribution — a small number of high-value luxury deals pull the average up while most transactions cluster in the mid-market range.

---

## 📈 Charts Created

| # | Chart | Type | Skill Introduced |
|---|---|---|---|
| 1 | Project Status Distribution | Donut Chart | Donut chart + percentage data labels |
| 2 | Year-on-Year Registration Trend | Stacked Column Chart | Stacked series, trend annotation |
| 3 | Top Localities Comparison | Grouped Bar Chart | Side-by-side multi-series bars |
| 4 | Transaction Types Breakdown | Horizontal Bar Chart | Sorting by frequency, bar labels |
| 5 | Market Value Segments | Column Chart | IF-based segmentation, segment colouring |
| 6 | Floor-wise Transaction Distribution | Column Chart | Text parsing to extract floor numbers |

---

## 🛠️ Skills Practised

### Google Sheets — Charting
- Donut chart with percentage data labels
- Stacked column chart
- Grouped bar chart
- Data labels on charts (position, formatting)
- Alternating row colours on data tables

### Data Analysis
- Value segmentation using nested `IF()` / `IFS()`
- `COUNTIF` across derived segments
- Mean vs median analysis for skewed distributions
- Interpreting regulatory events in time-series data (the 2017 spike ≠ a market boom)

### Data Cleaning
- Trimming whitespace in locality names causing duplicate `COUNTIF` groups
- Standardising mixed-case transaction type labels
- Handling blank cells without breaking formulas
- Extracting floor numbers from free-text fields using `LEFT`, `MID`, `FIND`

### Domain Knowledge
- Understanding RERA compliance timelines and what "lapsed" status means for buyers
- Distinguishing Agreement to Sell from Sale Deed in property transactions
- Reading government open data with incomplete or inconsistent records

---

## 💡 Key Findings

1. **1 in 5 projects has lapsed** — the 20.8% lapse rate is significant and reflects either developer delays, financial stress, or regulatory non-compliance. Not the same as project failure, but a buyer risk signal.

2. **2017 spike is regulatory, not a market boom** — 412 registrations in a single year happened because RERA was new and all existing projects had to register. Treating it as organic demand would be misleading.

3. **Erandwane buyers are primarily pre-possession purchasers** — Agreement to Sell dominating the transaction type means most buyers are locking in under-construction properties, not buying completed homes.

4. **Median is a better market signal than mean** — at ₹41.3L vs ₹66.5L, the median tells the more honest story of what a typical Erandwane buyer actually pays.

5. **Growth is geographically concentrated** — the top 4 localities alone account for a disproportionate share of all projects, reflecting Pune's radial expansion from the city core westward (Kothrud, Punawale) and eastward (Kharadi).

---

## 🧰 Tools Used

- **Google Sheets** — all analysis, formulas, and charts
- **Maharashtra RERA Open Data Portal** — primary data source

---

## 🗂️ Project Series

This is **Project 4** of an ongoing Google Sheets data analysis series:

| Project | Topic |
|---|---|
| Project 1 | *(earlier project)* |
| Project 2 | *(earlier project)* |
| Project 3 | *(earlier project)* |
| **Project 4** | **Pune Real Estate Market Trends ← you are here** |

---

## 📜 Data Source

**Maharashtra Real Estate Regulatory Authority (RERA)**
Established under the Real Estate (Regulation and Development) Act, 2016. RERA mandates registration of all residential projects above a specified threshold, making its open data portal one of the most comprehensive public records of India's real estate market activity.

> Data used as-is from the government portal. No data was modified or synthesised.
