# 🏦 Project 4 — AI-Assisted Financial Data Transformation & Reconciliation

**Dataset 1:** 1,000 GL Journal Entry records · MS SQL Server → Oracle GL Interface  
**Dataset 2:** 1,000 Employee Timesheet records · Timesheet-to-Purchase Order Matching  
**Tool used:** Claude (Anthropic) — AI-assisted data validation, transformation & reconciliation

---

## 🧩 Business Context

This project is grounded in real enterprise work — the kind that runs quietly in the background of every finance department.

Every period-end, financial data flows from source systems (Microsoft SQL Server) into Oracle's GL interface tables. If that data arrives with errors — missing cost centres, invalid accounts, currency mismatches, unmatched purchase orders — the posting fails, finance teams scramble, and reporting is delayed.

**The traditional approach:** manual validation scripts, DBA involvement, hours of reconciliation.  
**The AI-assisted approach:** prompt-driven analysis that flags errors, explains root causes, and recommends fixes — in minutes.

---

## 📁 Datasets

### Dataset 1 — GL_Transactions_Source.csv
Simulates financial journal entries extracted from MS SQL Server, staged for load into Oracle GL interface tables.

| Field | Description |
|---|---|
| TRANSACTION_ID | Unique journal entry reference |
| TRANSACTION_DATE | Date of financial transaction |
| COMPANY_CODE | Legal entity (CORP-UK, CORP-US, CORP-NG, CORP-ZA) |
| DEPARTMENT | Business unit |
| COST_CENTRE | Oracle cost centre code |
| GL_ACCOUNT | Target Oracle GL account |
| DESCRIPTION | Journal narrative |
| DEBIT_AMOUNT | Debit value |
| CREDIT_AMOUNT | Credit value |
| CURRENCY | Transaction currency |
| SOURCE_SYSTEM | MS-SQL-SERVER |
| TARGET_SYSTEM | ORACLE-GL |
| STATUS | VALID / ERROR / PENDING |
| ERROR_TYPE | Root cause of failure if ERROR |
| PERIOD | Accounting period |

**Record summary:**
- ✅ VALID: 668 records — ready for Oracle GL load
- ❌ ERROR: 150 records — blocked, require remediation
- ⏳ PENDING: 182 records — awaiting validation

### Dataset 2 — Timesheet_PO_Matching.csv
Simulates weekly employee timesheet data matched against approved Purchase Orders before Oracle GL processing.

| Field | Description |
|---|---|
| TIMESHEET_ID | Unique timesheet reference |
| EMPLOYEE_ID | Employee identifier |
| JOB_TITLE | Role classification |
| WEEK_STARTING | Week commencing date |
| HOURS_WORKED | Actual hours submitted |
| HOURLY_RATE_GBP | Contracted rate |
| TOTAL_AMOUNT_GBP | Timesheet value |
| PO_NUMBER | Linked Purchase Order |
| PO_APPROVED_HOURS | Hours authorised on PO |
| PO_BUDGET_GBP | PO budget value |
| MATCH_STATUS | MATCHED / UNMATCHED / PARTIAL / OVER_CLAIMED |
| VARIANCE_HOURS | Difference between worked and approved hours |
| COST_CENTRE | Oracle cost centre for posting |
| PERIOD | Accounting period |

**Record summary:**
- ✅ MATCHED: 494 records — ready for Oracle GL posting
- ❌ UNMATCHED: 156 records — no valid PO found
- ⚠️ PARTIAL: 162 records — hours partially within PO tolerance
- 🚨 OVER_CLAIMED: 188 records — hours exceed PO approval

---

## 🧪 Prompt Evolution — The Core Skill

---

### GL Transaction Validation

**Attempt 1 — Score: 7/10**
```
Analyse this financial dataset and tell me what errors exist.
```
*Issues: No context, no priority, no output format, no actionable framing.*

---

**Attempt 2 — Score: 8.5/10**
```
You are a data analyst. I have a dataset of 1,000 GL journal entries being transferred
from MS SQL Server to Oracle GL interface tables. Analyse the dataset and:
- Identify all ERROR records and classify by error type
- Flag PENDING records that may block period-end close
- Calculate the total financial value at risk
- Present findings in a clear summary table
```
*Improvements: Role defined, context given, specific outputs requested.*

---

**Attempt 3 — Score: 9.5/10**
```
You are a financial data analyst supporting a period-end close for a multinational company.
I have 1,000 GL journal entries staged for load into Oracle GL interface tables, extracted
from MS SQL Server. Analyse the dataset and produce a reconciliation report for the
Finance Controller. Prioritise in this order:
1) ERROR records — classify by type, show count and total £ value at risk
2) PENDING records — flag any that will block Oracle GL posting
3) VALID records — confirm posting-ready count and value
4) Recommend exactly 3 actions the finance team should take before period close
Use a summary table for each category. Keep language audit-ready — no jargon.
```
*Improvements: Audience defined (Finance Controller), priority order set, financial value quantified, audit-ready language specified, actionable recommendations requested.*

---

### Timesheet-to-PO Matching

**Attempt 1 — Score: 7/10**
```
Review this timesheet data and check if it matches the purchase orders.
```

---

**Attempt 2 — Score: 8.5/10**
```
You are a data analyst. I have 1,000 employee timesheet records that need to be matched
against Purchase Orders before Oracle GL posting. Identify all UNMATCHED and OVER_CLAIMED
records, calculate the total financial exposure, and summarise by department.
```

---

**Attempt 3 — Score: 9.5/10**
```
You are a payroll data analyst preparing a reconciliation report for the Finance and
Procurement teams. I have 1,000 weekly timesheet records staged for Oracle GL posting.
Each timesheet must match an approved Purchase Order within tolerance.
Analyse and report in this order:
1) OVER_CLAIMED — hours exceed PO approval: count, total £ exposure, top 5 employees
2) UNMATCHED — no valid PO found: count and total £ value, flag by department
3) PARTIAL — within tolerance but needs sign-off: count and recommended action
4) MATCHED — confirm posting-ready count and total value
Recommend exactly 3 actions Procurement should take before approving Oracle GL posting.
Format as an executive summary — clear, concise, audit-ready.
```

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

*Part of the [Prompt Engineering Portfolio](https://github.com/iamabeke/prompt-engineering-portfolio) by Femi Adesanya*
