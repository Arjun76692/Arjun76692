# Shivarjun Reddy Palla

**Data Analyst · Business Analyst · Product Analyst**  
Python · SQL · Power BI · PRDs · BRDs · Hyderabad

I'm a recent MCA graduate who gets curious about real problems — why investors ignore risk when picking mutual funds, where Zomato's refund process actually breaks down, why CRED users are unhappy despite a 4.2 rating. Most of my projects start from a question like that and end with something structured: a PRD, a BRD, a dashboard, or a process spec that someone could actually act on.

I've also done freelance analytical work on a real FlixBus India pricing dataset and transport routing data for a school — both with actual teams and stakeholders, not just personal projects.

---

## Projects

### [Mutual Fund Risk Discovery — Competitive Analysis & PRD](https://github.com/Arjun76692/Mutual-Fund-Risk-Adjusted-Performance-Analyzer-)

Started by asking 21 people how they pick mutual funds. 76% had never looked at a risk metric. Then I checked whether the platforms they used — Zerodha Coin and Angel One — even showed those metrics. They don't.

- Surveyed 21 investors; confirmed the behaviour gap firsthand. Zerodha and Angel One were the two most-used platforms (6 respondents each)
- Conducted a 12-point screenshot comparison of both platforms on the same fund (ICICI Prudential Large Cap) — neither shows Sharpe ratio, volatility, or max drawdown at discovery
- Fetched live NAV data for 14,221 funds via mftool API, computed Sharpe ratio, volatility, max drawdown, and upmarket/downmarket capture from scratch in Python — stored in MySQL via SQLAlchemy
- Filtered 342 large-cap funds through 4 downside-protection criteria and narrowed to 20 qualifying funds (6%)
- Compared return-only vs multi-metric selection: return-only gave higher CAGR (18.6% vs 16.0%) but significantly higher volatility — confirming multi-metric filtering is better for stable long-term decisions
- Wrote a PRD for a Risk Score Card feature: MoSCoW-prioritised requirements, 4 investor persona user stories, 3-phase roadmap, risk register with mitigations, and 4 success metrics with baselines and targets

**Stack:** Python, MySQL, mftool API, SQLAlchemy, Jupyter Notebook  
**Links:** [Repo](https://github.com/Arjun76692/Mutual-Fund-Risk-Adjusted-Performance-Analyzer-) · [Medium write-up](https://medium.com/@arjunreddy.inc/i-asked-21-people-how-they-pick-mutual-funds-their-answers-shocked-me-5bd6295fd675)

---

### [Zomato — Complaint & Refund Resolution Analysis](https://github.com/Arjun76692/Zomato-Complaint_and_Refund_Resolution_Analysis_and_CaseStudy)

Wanted to understand where Zomato's post-order experience actually breaks down — not from assumptions, but from what users wrote.

- Scraped 30K Zomato Play Store reviews and filtered to 3,462 complaint reviews (score ≤3, length >15 chars)
- Classified them into 10 complaint themes using DeBERTa NLP (zero-shot, multi-label, threshold 0.70, TOP_K=2) — stored in MySQL via SQLAlchemy for structured analysis
- Mapped complaints to 4 process stages: delivery execution (53%), support & resolution (20%), financial (12%), technical (1.4%)
- Found via co-occurrence analysis that support failure and refund delays almost always appear in the same review — they're not separate issues, they share a root cause
- Simultaneous multi-category spikes on Mar 8–9 and Mar 17–18 pointed to systemic operational breakdowns — a finding only visible from a cross-category view, not single-theme analysis
- Translated everything into a BRD with 9 Must Have requirements, 5 stakeholder-mapped user stories (customer, support agent, delivery rider, ops manager), and 4 success metrics with current baselines and targets

**Stack:** Python, DeBERTa NLP, MySQL, SQLAlchemy, SQL

---

### [JoshTalks — Product Design, Data Quality & AI Evaluation](https://github.com/Arjun76692/JoshTalks_Product_Design-Data_Quality_Analysis_AI-Evaluation_System-)

Three separate deliverables for JoshTalks across product design, contributor quality, and AI evaluation — all connected to the same goal of building reliable training data.

- Wrote a full PRD for a mobile-first image collection platform targeting contributors across India — defined a 7-step contributor workflow, offline draft-saving logic, GPS override handling, blur detection, 200-character description minimum, and an admin dashboard with district-level coverage tracking. Included MoSCoW-prioritised requirements, 6 success metrics, and 7 edge cases with handling logic
- Analysed 51,783 transcription tasks to identify low-quality contributors using three behavioural signals: speed ratio below 1.0 (submitted before audio finished), no-edit submissions on clips over 5 seconds, and repeated placeholder text (10 users submitted the same text up to 64 times). Designed a 3-tier response system — task rejection, flag for human review, account suspension — with explicit thresholds and human review gates
- Designed a Voice AI evaluation framework with 4 measurable criteria (task completion, comprehension accuracy, naturalness, error recovery), a calibration protocol, and an AI-assisted triage system to limit full human review to 250–350 of every 1,000 conversations

**Stack:** Python, Pandas, Excel, PRD writing, data quality analysis

---

### [Large-Scale EDA / ETL Pipeline](https://github.com/Arjun76692/EDA-ETL-Pipeline)

Wanted to build something closer to how data pipelines work in practice — not a single notebook, but a proper multi-step pipeline with error handling and logging.

- Built a 3-script ETL pipeline (ingest, clean, summarise) using CTEs across 5 tables including a 12.7M-row sales file — loaded into MySQL via SQLAlchemy with 5-minute timeouts and dual logging (file + stdout) for production-style reliability
- Applied analysis on $14.1M in sales data: found 8 of 12 months in 2024 declined vs 2023, 3 loss-making SKUs, and a 13.5% pricing gap across markets
- Delivered findings in Power BI with evidence-backed recommendations for product-mix and pricing decisions

**Stack:** Python, Pandas, SQLAlchemy, MySQL, Power BI

---

### [AI Resume Screening Automation](https://github.com/Arjun76692/n8n_resume_screening_automation)

Mapped a 3–4 hour manual screening process and redesigned it as an automated pipeline.

- Built an 11-node n8n pipeline: Google Drive trigger → PDF extraction → JD fetch → merge → Groq Llama 3.1 (temp 0.1) → JavaScript parser → Google Sheets — processes a resume within 1 minute of upload
- Engineered the AI prompt with a custom scoring algorithm (skills match, experience, domain fit, missing requirements) and a structured JSON output schema (name, email, score, reasoning, matched skills, missing skills)
- Set temperature to 0.1 for scoring consistency — same resume gets near-identical scores on repeated runs

**Stack:** n8n, Groq LLM (Llama 3.1), Google Drive API, Google Sheets, JavaScript

---

### [CRED App — 150K+ Review Analysis](https://github.com/Arjun76692/CRED-Product-Analytics-150K-Reviews)

I noticed CRED had a 4.2 rating but my own coins felt increasingly worthless — so I scraped 150K reviews to check if other users felt the same.

- Scraped and cleaned 134,552 valid reviews from the Play Store
- Built a weighted Pain Index (40% review volume, 60% upvotes) to rank complaint themes by real user impact — not just mention count
- Rewards devaluation ranked #1 with a pain score of 1.00 and 22,618 upvotes, while the rewards theme averaged just 2.48 stars vs the app's 4.20 overall
- Ran version concentration analysis: no complaint theme exceeded 60% concentration in any two app versions — meaning the problems are structural, not tied to a bad release
- Built a Power BI dashboard to track complaint trends from Sep 2022 to Feb 2026

**Stack:** Python, Pandas, Google Play Scraper, Power BI  
**Links:** [Repo](https://github.com/Arjun76692/CRED-Product-Analytics-150K-Reviews) · [Medium write-up](https://medium.com/@arjunreddy.inc/i-analysed-1-50-000-cred-reviews-because-i-got-curious-about-my-own-coins-which-i-got-as-rewards-8ab54d11e6ac)

---

## Freelance Work

### Pricing Analytics — FlixBus India *(Jan – Mar 2026)*
Selected via open application · Team of 3

Worked on a real FlixBus India pricing dataset alongside a 3-member team.

- Built competitor-matching logic across 26,170 routes — defining grouping criteria on bus type, AC/sleeper/seater classification, bus score (±0.5 buffer), and a 90-minute departure window
- Designed a weighted average pricing model and load factor metric (seats filled / total seats) to quantify demand pressure per route
- Jointly flagged 15,163 underpriced and 3,991 overpriced combinations into a 5-bucket action framework (Maintain / Increase / Reduce / Slight Reduce / Investigate) with Medium/High severity tiers

### Transport Routing Analytics — Johnson Grammar School *(Sep – Nov 2025)*
Freelance engagement · Team of 5 · Reporting to school leadership

- Analysed student transport data across 27 bus routes, computing a weighted route efficiency score (utilisation 40%, detour ratio 30%, students-per-stop 30%) and daily cost per route using fuel and driver cost assumptions
- Identified consolidation opportunities that reduced 27 routes to 24 by merging low-utilisation routes within shared geographic zones
- Flagged high-detour routes (ratio >1.4) and low-density stops (<4 students per stop) for operational review — presented findings directly to school leadership

---

## What I Work With

**Data & Programming:** Python (Pandas, NumPy, SciPy), SQL (MySQL, CTEs, window functions), DeBERTa NLP, SQLAlchemy, mftool API, Google Play Scraper, Jupyter Notebook, Git

**Reporting & Analysis:** Power BI (DAX, dashboards), Excel (Pivot Tables, VLOOKUP), KPI design, complaint analysis, cohort analysis, survey design, competitive analysis, ETL pipelines

**Product & BA:** PRD/BRD writing, MoSCoW prioritisation, user stories, acceptance criteria, stakeholder mapping, process flow mapping, edge case identification, roadmap definition

**Automation:** n8n, Groq LLM, Google Drive API, workflow design

---

## Certifications

- Google Data Analytics Professional Certificate (Coursera, Mar 2025)
- Accenture Tech Consulting Simulation — Forage (Agile, user stories, backlog)
- HackerRank SQL Gold Badge
- LeetCode SQL — Top 15% Globally

---

## Contact

- **Email:** shivarjunreddypalla@gmail.com
- **LinkedIn:** [linkedin.com/in/shivarjun-reddy-palla](https://www.linkedin.com/in/shivarjun-reddy-palla/)
- **GitHub:** [github.com/Arjun76692](https://github.com/Arjun76692)
- **Location:** Hyderabad, India (open to relocation across metro cities)
