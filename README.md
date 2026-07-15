# 🤖 Prompt Engineering Portfolio
**by Oluwafemi (Femi) Adesanya** · Data Analyst · Oracle Data Specialist · AI Workflow Consultant

---

## About This Portfolio

I am a **Data Analyst and Oracle Developer** (20+ years) transitioning into AI-assisted analysis and prompt engineering. This portfolio documents real business problems solved using **Claude (Anthropic)** — with measurable before/after improvements tracked per project.

My background in financial data transformation, ETL pipelines, and Oracle GL interfaces gives me a rare edge: I don't just engineer prompts — I engineer them for **data-heavy, high-stakes business contexts**.

> **Core belief:** The quality of your prompt determines the quality of your output. This portfolio proves it — with scored iterations on every project.

---

## 📁 Projects

---

### Project 1 — AI Impact on Jobs by 2030
**Dataset:** 3,000 employee records · 10 industries · 10 countries

**Business problem:** HR leadership teams need to understand which roles face automation risk by 2030 — and act on it now.

**What I built:** An interactive dark-themed dashboard for non-technical HR audiences, using prompt engineering to drive analysis and visualisation from raw CSV data.

**Live Dashboard:** [View HR Leadership Dashboard](https://iamabeke.github.io/prompt-engineering-portfolio/ai_jobs_2030_hr_leadership_dashboard.html)

---

#### 🧪 Prompt Evolution — The Core Skill

This project demonstrates how refining a prompt produces dramatically better outputs from the same dataset.

---

**Attempt 1 — Score: 7/10**
```
act as a data analyst, review and analyse this data set. the context is AI Impact on
jobs market in 2030. produce outcome in the form of graphs or dashboard for easy
understanding and overview.
```
*Issues: No audience defined, no priority order, no output depth, no theme.*

---

**Attempt 2 — Score: 8.5/10**
```
You are a data analyst. I've uploaded a dataset on AI Impact in future on jobs market
in 2030 (3,000 employee_id). Build an interactive dashboard focusing on:
'Job roles most affected by AI automation',
'New careers emerging due to AI technologies',
'Industry-wise impact analysis',
'Skill demand changes by 2030',
'Regional and global employment trends'
as the primary metrics. Prioritise visual clarity — the audience is non-technical.
Use a dark theme. Flag the 2–3 most important insights.
```
*Improvements: Role assigned, context given, output format and theme specified, insights requested.*

---

**Attempt 3 — Score: 9.5/10**
```
You are a data analyst presenting to a non-technical HR leadership team. I've uploaded
a dataset on AI's impact on jobs by 2030 (3,000 records). Build an interactive dark-themed
dashboard. Prioritise in this order:
1) Jobs most at risk
2) Skills to develop urgently
3) Industry-wise impact
4) Emerging roles
5) Regional trends
Use bar charts for comparisons, line charts for trends. Keep labels simple — no jargon.
Flag exactly 3 insights a business leader would act on today.
```
*Improvements: Audience specified, priority order defined, chart types assigned, actionable framing added.*

---

#### 📊 Key Business Insights

| # | Insight | Recommended Action |
|---|---|---|
| 1 | 1 in 2 employees faces meaningful automation risk (avg 51%) | Audit high-risk roles immediately |
| 2 | Cloud Computing & Leadership are the #1 skills gap | Launch reskilling programme now |
| 3 | Job market splitting — 34% growing roles, 33% declining | Revise hiring strategy for 2026 |

#### 📈 Prompt Score Progression

| Attempt | Score | Key Improvement |
|---|---|---|
| 1 | 7.0 / 10 | Baseline |
| 2 | 8.5 / 10 | Added role, theme, format, insights |
| 3 | 9.5 / 10 | Added audience, priority order, actionable framing |

---

### Project 2 — World Bank & UN HDI Global Development Analysis
**Dataset:** World Bank indicators + UN Human Development Index

**Business problem:** Development organisations and policy teams need a fast way to compare country-level progress across economic and social indicators.

**What I built:** Two interactive dashboards (v1 and v2 refined) using AI-assisted analysis to surface regional patterns and HDI correlations.

**Live Dashboards:**
- [IDA Dashboard v1](https://iamabeke.github.io/prompt-engineering-portfolio/IDA_world_bank_HDI_dashboard.html)
- [IDA Dashboard v2 (Refined)](https://iamabeke.github.io/prompt-engineering-portfolio/IDA_dashboard_v2_refined.html)

---

### Project 3 — Social Media Impact on Teen Mental Health
**Dataset:** 1,200 teens · ages 13–19

**Business problem:** School leadership and child welfare teams need evidence-based insights on how social media affects student wellbeing — presented accessibly.

**What I built:** An interactive dark-themed dashboard translating raw survey data into actionable findings for non-technical decision makers.

**Live Dashboard:** [View Teen Mental Health Dashboard](https://iamabeke.github.io/prompt-engineering-portfolio/teen_mental_health_dark_dashboard.html)

**Key findings:**
- Average sleep (6.1 hrs) is nearly 2 hrs below recommended minimum
- Teens using 6–8 hrs of social media daily score higher on stress and anxiety
- Pre-sleep screen time of 2–3 hrs reduces sleep by 0.5 hrs vs under 1 hr
- Stress and anxiety peak at ages 16–17

---

## 🛠️ Skills Demonstrated

- Prompt Engineering (iterative, scored, measurably improved)
- AI-assisted Data Analysis using Claude (Anthropic)
- Dashboard design for non-technical business audiences
- Financial data transformation & ETL (Oracle, GL interfaces)
- Data storytelling and actionable insight generation

---

# 🏦 Project 4 — AI-Assisted Financial Data Transformation & Reconciliation

**Dataset 1:** 1,000 GL Journal Entry records · MS SQL Server → Oracle GL Interface  
https://github.com/iamabeke/prompt-engineering-portfolio/blob/main/GL_Transactions_Source.csv 
**Dataset 2:** 1,000 Employee Timesheet records · Timesheet-to-Purchase Order Matching  
https://github.com/iamabeke/prompt-engineering-portfolio/blob/main/Timesheet_PO_Matching.csv
**Tool used:** Claude (Anthropic) — AI-assisted data validation, transformation & reconciliation

---
## 🧩 Business Context

This project is grounded in real enterprise work — the kind that runs quietly in the background of every finance department.

Every period-end, financial data flows from source systems (Microsoft SQL Server) into Oracle's GL interface tables. If that data arrives with errors — missing cost centres, invalid accounts, currency mismatches, unmatched purchase orders — the posting fails, finance teams scramble, and reporting is delayed.

**The traditional approach:** manual validation scripts, DBA involvement, hours of reconciliation.  
**The AI-assisted approach:** prompt-driven analysis that flags errors, explains root causes, and recommends fixes — in minutes.

---
## 📊 Key Business Insights

### GL Transactions
| # | Insight | Action |
|---|---|---|
| 1 | 150 ERROR records block Oracle GL load — 15% of total volume | Remediate before period close |
| 2 | MISSING_COST_CENTRE is the #1 error type | Update source system validation rules |
| 3 | 182 PENDING records risk delaying financial reporting | Prioritise review within 24hrs |

### Timesheet / PO Matching
| # | Insight | Action |
|---|---|---|
| 1 | 188 OVER_CLAIMED records represent unauthorised spend | Procurement to review and re-approve or reject |
| 2 | 156 UNMATCHED timesheets cannot post to Oracle GL | Employees to resubmit with valid PO reference |
| 3 | 506 records (51%) require intervention before posting | Finance Controller to escalate to department heads |

---

## 📈 Prompt Score Progression

| Dataset | Attempt | Score | Key Improvement |
|---|---|---|---|
| GL Transactions | 1 | 7.0 / 10 | Baseline |
| GL Transactions | 2 | 8.5 / 10 | Role, context, structured outputs |
| GL Transactions | 3 | 9.5 / 10 | Audience, priority order, audit-ready framing |
| Timesheet / PO | 1 | 7.0 / 10 | Baseline |
| Timesheet / PO | 2 | 8.5 / 10 | Context, financial exposure quantified |
| Timesheet / PO | 3 | 9.5 / 10 | Executive summary, procurement actions, audit framing |

---

## 🛠️ Skills Demonstrated

- Prompt Engineering (iterative, scored, measurably improved)
- Financial data transformation — MS SQL Server → Oracle GL
- ETL validation and error classification
- Timesheet-to-Purchase Order reconciliation
- Audit-ready reporting for Finance Controllers
- AI-assisted analysis using Claude (Anthropic)

---
## 📬 Contact

- **Email:** mrs.adesanya22@gmail.com
- **LinkedIn:** [Femi Adesanya](https://www.linkedin.com/in/femi-adesanya-26a96915)
- **GitHub:** [github.com/iamabeke](https://github.com/iamabeke)
- **Open to:** Data Analyst · AI Analyst · Prompt Engineer · Oracle Data Specialist · Freelance/Contract

---

*This portfolio is actively updated. New projects added regularly.*
