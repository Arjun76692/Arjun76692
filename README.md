<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Merriweather&size=48&duration=2500&pause=9999&color=7AE2CF&center=true&vCenter=true&width=1000&height=80&lines=Shivarjun+Reddy+Palla" alt="Shivarjun Reddy Palla" />
</p>
<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Jetbrains+Mono&size=22&duration=2500&pause=250&color=077A7D&center=true&vCenter=true&width=1000&height=50&lines=Business+Analyst;Data+Analyst" alt="Role" />
</p>

# Hey! I'm Shivarjun 👋

**Data & Business Analytics | Python · SQL · Power BI | Hyderabad**

I'm a recent MCA post-graduate who learns by building real things. Not toy datasets — actual pipelines, real app data, financial instruments with real complexity. I care about finding the insight behind the numbers, not just running the code.

---

## Featured Projects

---

### 🔍 [CRED App — Play Store Review Analysis](https://github.com/Arjun76692/CRED-Product-Analytics-150K-Reviews)
> *What does a 4.20 star rating hide? Turns out, a lot.*

I scraped 1,50,000 CRED Play Store reviews (Oct 2022 – Feb 2026) after noticing my coins couldn't buy anything cheaper than Amazon. What I found was a 1.72 star gap sitting underneath a healthy headline rating.

**The core finding:**
- Overall app rating: **4.20 ★**
- Reviews mentioning rewards: **2.48 ★** — including positive ones
- Gap: **1.72 stars**
- 59.8% of all rewards-related reviews are 1 or 2 star
- "Cashback" mentioned **3,215 times** — a single removed feature, still appearing years later
- Every complaint theme classified as **structural** — spread across 110 versions, 3+ years. No release fixed it.

**Pain index ranking** (normalised complaint volume + community validation):

| Theme | Score |
|---|---|
| Rewards devaluation | 1.000 |
| Customer support | 0.556 |
| Payment issues | 0.477 |
| App performance | 0.194 |

**Stack:** Python, google-play-scraper, pandas, matplotlib, Power BI

📄 [Read the full analysis on Medium](https://medium.com/@arjunreddy.inc/i-analysed-1-50-000-cred-reviews-because-i-got-curious-about-my-own-coins-which-i-got-as-rewards-8ab54d11e6ac) · 📓 [Notebook](https://github.com/Arjun76692/CRED-Product-Analytics-150K-Reviews/Analysis.ipynb)

---

### 📊 [Mutual Fund Investment Framework](https://github.com/Arjun76692/Mutual-Fund-Risk-Adjusted-Performance-Analyzer-)
> *Only 6% of 340+ equity funds pass a basic risk-adjusted quality bar.*

I wanted to understand how to evaluate mutual funds beyond just returns — so I built a framework from scratch using real fund data, conducted 21 structured interviews to understand how retail investors actually make decisions, and found the gap between what investors look at and what the data says matters.

**The core finding:**
- Analysed 342 equity mutual funds on risk-adjusted metrics
- Only **6% cleared all three quality filters** — Sharpe ratio, max drawdown, and volatility threshold
- Most funds marketed on 1-year returns had significantly worse 3-year risk profiles
- Built a scoring model that weights downside protection over raw return

**What I built:**
- Python-MySQL ETL pipeline to fetch, store, and refresh fund data
- Calculated Sharpe ratio, max drawdown, volatility per fund
- 21 structured investor interviews to validate the framework
- PowerPoint deck with findings and recommendations

**Stack:** Python, MySQL, PowerPoint

📄 [Published on Medium](https://medium.com/@arjunreddy.inc/i-asked-21-people-how-they-pick-mutual-funds-their-answers-shocked-me-5bd6295fd675)

---

### 📦 [E-Commerce Vendor Analytics Pipeline](https://github.com/Arjun76692/E-Commerce-Vendor-Analytics-Pipeline)
End-to-end ETL pipeline for vendor profitability analysis across 2.7M+ transactions.

- Automated ingest → clean → transform pipeline with error handling and logging
- Built star schema with KPIs: profit margin, inventory turnover, vendor concentration
- Found top 24% of vendors generate 65% of profit — classic concentration risk
- Power BI dashboard with drill-down by vendor, category, and time period

**Stack:** Python, SQL, Power BI

---

### 🤖 [AI Resume Screening Automation](https://github.com/Arjun76692/n8n_resume_screening_automation)
Automated resume-to-JD matching using n8n and LLM's Api.

- Monitors Google Drive for new resumes, scores them against a JD automatically
- Outputs skills match %, gaps, and recommendation to Google Sheets
- JSON validation ensures consistent scoring across runs

**Stack:** n8n, Groq LLM, Google Drive API, Google Sheets

---

## What I Work With

**Languages & Tools**
- **Python** — pandas, NumPy, matplotlib, SQLAlchemy, google-play-scraper
- **SQL** — MySQL, CTEs, window functions, query optimisation
- **BI Tools** — Power BI (DAX, star schema), Tableau
- **Automation** — n8n workflows, API integrations
- **Other** — Excel, Git

---

## Certifications

- 🏆 **Google Data Analytics Professional Certificate** (Coursera)
- 🥇 **HackerRank SQL Gold Badge** — Top 15%
- 💻 **LeetCode SQL** — 95+ problems, Top 15%

---

## Get in Touch

📧 arjunreddy.inc@gmail.com
💼 [LinkedIn](https://www.linkedin.com/in/shivarjun-reddy-palla-31a001223/)
📍 Hyderabad, India

---

*All projects have runnable code, documented notebooks, and real outputs. If it's here, it works.*
