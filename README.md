# 📊 Loan Portfolio Dashboard — Microfinance Credit Analytics (Excel)

**By Benard Musyoka Mwinzi** | [benadata.github.io](https://benadata.github.io) | Nairobi, Kenya

---

## 📌 Business Problem

Microfinance institutions (MFIs) in Kenya disburse thousands of loans annually to smallholder farmers, traders, and micro-entrepreneurs. Despite strong disbursement volumes, many MFIs lack real-time visibility into portfolio health — resulting in reactive rather than proactive credit risk management.

Without a structured monitoring system, credit managers cannot:
- Identify which loan officers or counties are generating disproportionate NPLs
- Track Portfolio-at-Risk (PAR) aging before it breaches provisioning thresholds
- Assess sector concentration risk across the loan book
- Evaluate loan officer performance objectively
- Produce regulatory-ready portfolio reports for the Central Bank of Kenya (CBK)

This dashboard addresses all five gaps using Excel — no BI tools required.

---

## 🗂️ Project Structure

The Excel workbook contains **6 colour-coded sheets**:

| Sheet | Description |
|---|---|
| 📋 Business Problem | Structured problem statement — context, objective, approach, expected outcome |
| 📁 Loan Book | 50 synthetic loan records across 8 Kenyan counties, 8 sectors, 8 loan officers |
| 📝 Executive Summary | 12 live KPI cards + written portfolio health commentary and recommendations |
| 📊 Portfolio Summary | 5 formula-driven tables: by sector, county, risk grade, PAR aging, KPI scorecard |
| 👤 Officer Performance | PAR rate and performance rating (Excellent/Good/Needs Improvement/Critical) per officer |
| 📈 Charts & Visuals | 4 charts for board/credit committee presentation |

---

## 🔢 Key Metrics Tracked

| Metric | Formula Logic | CBK Benchmark |
|---|---|---|
| PAR > 30 Days | Outstanding DPD>30 / Total Outstanding | < 5% |
| PAR > 90 Days | Outstanding DPD>90 / Total Outstanding | < 2% |
| NPL / Write-Off Rate | Written Off Loans / Total Loans | < 2% |
| Delinquency Rate | Delinquent Loans / Total Loans | < 10% |
| Portfolio Yield | Weighted Avg. Interest Rate by Loan Amount | ≥ 18% |
| Repayment Rate | Closed Loans / Total Loans | > 80% |

---

## ⚙️ How the Formulas Work

All KPIs and summary tables are powered by **171 live Excel formulas** — no hardcoded values. Key functions used:

- `COUNTIF` / `COUNTIFS` — loan counts by status, officer, risk grade, DPD bucket
- `SUMIF` / `SUMIFS` — outstanding balances by sector, county, officer
- `SUMPRODUCT` — PAR calculations across multiple conditions (e.g. DPD > 30 AND officer = X)
- `IFERROR` — prevents division-by-zero errors on empty slices
- `IF` nesting — performance rating logic (Excellent → Good → Needs Improvement → Critical)

Changing any value in the **Loan Book** sheet automatically updates every KPI, chart, and table throughout the workbook.

---

## 📂 Dataset

The loan book contains **50 synthetic records** designed to reflect a realistic Kenyan MFI portfolio:

- **Counties:** Nairobi, Mombasa, Kisumu, Nakuru, Eldoret, Machakos, Nyeri, Meru
- **Sectors:** Agriculture, Trade & Commerce, Manufacturing, Education, Health, Real Estate, Transport, Personal
- **Products:** Business Loan, Emergency Loan, Asset Finance, Group Loan, Agricultural Loan
- **Loan Sizes:** KES 50,000 – KES 1,000,000
- **Tenor:** 6 – 36 months
- **Interest Rates:** 14% – 24% per annum
- **Statuses:** Active (22), Delinquent (14), Closed (10), Written Off (4)
- **Risk Grades:** A (low risk) through E (loss)
- **Collateral Types:** Land Title, Logbook, Shares, Salary Undertaking, Group Guarantee, Machinery, None

> ⚠️ All data is synthetic and generated for demonstration purposes only. No real borrower information is used.

---

## 📈 Charts Included

1. **Loans by Status** — Pie chart showing Active / Closed / Delinquent / Written Off split
2. **Outstanding Balance by Sector** — Column chart for sector concentration analysis
3. **PAR Aging Buckets** — Column chart showing outstanding balances across DPD buckets (Current / 1–30 / 31–60 / 61–90 / >90)
4. **PAR Rate by Loan Officer** — Horizontal bar chart for officer-level risk comparison

---

## 🛠️ Tools Used

- **Microsoft Excel** — Dashboard, formulas, charts
- **Python + openpyxl** — Workbook generation and formula injection
- **LibreOffice** — Formula recalculation and validation

---

## 💡 Key Insights (from the dashboard)

- PAR > 30 rate is tracked against the CBK benchmark of < 5% — delinquency is concentrated in D and E risk-grade accounts
- Trade & Commerce and Agriculture represent the highest outstanding balances, creating sector concentration risk
- Loan officers with PAR rates > 20% are flagged as **Critical** — indicating client appraisal process gaps
- Loans with **no collateral** show a disproportionate share of write-offs
- Nairobi and Mombasa dominate disbursements; Eldoret and Nyeri represent untapped market opportunity

---

## 👤 About the Author

**Benard Musyoka Mwinzi**
Freelance Data Analyst | Nairobi, Kenya

- 🎓 BA Economics & Mathematics — Machakos University
- 📜 Google Data Analytics Professional Certificate
- 💼 Experience: Knoetic Inc. (People Analytics), TIFA Research, Blossom Academy Ghana
- 🌐 Portfolio: [benadata.github.io](https://benadata.github.io)
- 💼 Available on [Upwork](https://www.upwork.com)

---

*This project was built to demonstrate applied credit analysis skills in a Kenyan microfinance context — including portfolio segmentation, PAR aging analysis, risk grading, and loan officer performance evaluation.*
