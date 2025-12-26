Perfect 👍
Below are **🔥 30 TRAP-STYLE DP-600 SECURITY MCQs** — **ALL security only**, **exam-level**, **pattern-based**, and **designed to destroy confusion**.

💡 These are **NOT basic questions**.
They are written exactly like **Microsoft Learn / DP-600 real exam traps**.

---

# 🔐 DP-600 — ALL SECURITY TRAP MCQs

*(Microsoft Fabric + Power BI Semantic Model)*

---

## 🧪 MCQ 1

You need to restrict access so that only specific users can query a **single table** in a **Fabric data warehouse**.

What should you use?

A. Workspace role
B. Item-level permission
C. Row-level security
D. **T-SQL GRANT**

✅ **Correct Answer: D**

**Why:**
Warehouse object access = **T-SQL permissions**

❌ Workspace role → workspace only
❌ Item-level → open/close warehouse
❌ RLS → rows, not object access

📌 **Exam rule:**

> Warehouse object security = **T-SQL**

---

## 🧪 MCQ 2

You want to ensure that a **measure** named `ProfitMargin` is visible **only to the Finance team** in Power BI reports.

What should you implement?

A. Static RLS
B. Dynamic RLS
C. **Object-Level Security (OLS)**
D. Column-Level Security

✅ **Correct Answer: C**

📌 **Rule:**

> Measures can ONLY be secured using **OLS**

---

## 🧪 MCQ 3

Users must be able to query a warehouse table, but sensitive columns should appear as `XXXX`.

Which feature should you use?

A. Column-Level Security
B. Object-Level Security
C. **Dynamic Data Masking**
D. Row-Level Security

✅ **Correct Answer: C**

📌 **Rule:**

> Masking ≠ access control

---

## 🧪 MCQ 4

You need to prevent users from seeing **specific columns entirely** in a warehouse table.

What should you use?

A. Dynamic Data Masking
B. **Column-Level Security**
C. Item-level permission
D. Workspace role

✅ **Correct Answer: B**

---

## 🧪 MCQ 5

You want to restrict users so they only see **their own country’s sales records**.

Which security method should you use?

A. OLS
B. CLS
C. **Row-Level Security (RLS)**
D. Sensitivity labels

✅ **Correct Answer: C**

---

## 🧪 MCQ 6

You want to protect sensitive data **across all Fabric items** and enforce governance.

What should you use?

A. RLS
B. OLS
C. CLS
D. **Sensitivity labels**

✅ **Correct Answer: D**

📌 **Rule:**

> Environment-wide protection = Sensitivity labels

---

## 🧪 MCQ 7

A user should not be able to **open** a lakehouse at all.

Which control should you configure?

A. RLS
B. CLS
C. **Item-level permissions**
D. T-SQL GRANT

✅ **Correct Answer: C**

---

## 🧪 MCQ 8

Which security feature is applied **only to semantic models**?

A. RLS
B. CLS
C. **Object-Level Security**
D. Dynamic Data Masking

✅ **Correct Answer: C**

---

## 🧪 MCQ 9

You want to restrict a **Power BI table visual** so a column does not appear for certain users.

What should you use?

A. RLS
B. **OLS**
C. Sensitivity label
D. Workspace role

✅ **Correct Answer: B**

---

## 🧪 MCQ 10

Which security feature controls **WHO can access a workspace**, but not the data inside?

A. RLS
B. CLS
C. **Workspace roles**
D. OLS

✅ **Correct Answer: C**

---

## 🧪 MCQ 11

Which security method should be used to secure **warehouse views and tables**?

A. OLS
B. **T-SQL GRANT**
C. CLS
D. Sensitivity labels

✅ **Correct Answer: B**

---

## 🧪 MCQ 12

You need to secure **both rows and columns** in a Fabric warehouse.

What should you use?

A. RLS only
B. CLS only
C. **RLS + CLS**
D. OLS

✅ **Correct Answer: C**

---

## 🧪 MCQ 13

Which security option is **NOT** considered access control?

A. OLS
B. CLS
C. RLS
D. **Dynamic Data Masking**

✅ **Correct Answer: D**

---

## 🧪 MCQ 14

A report user should not even **know that a table exists**.

Which feature achieves this?

A. RLS
B. CLS
C. **OLS**
D. Masking

✅ **Correct Answer: C**

---

## 🧪 MCQ 15

You need to control access to Fabric items **without touching SQL code**.

What should you use?

A. T-SQL GRANT
B. RLS
C. **Item-level permissions**
D. CLS

✅ **Correct Answer: C**

---

## 🧪 MCQ 16

Which security feature works at the **query result level**?

A. CLS
B. OLS
C. **Dynamic Data Masking**
D. Workspace role

✅ **Correct Answer: C**

---

## 🧪 MCQ 17

You need to restrict access to **calculated columns** in a semantic model.

What should you use?

A. RLS
B. CLS
C. **OLS**
D. T-SQL GRANT

✅ **Correct Answer: C**

---

## 🧪 MCQ 18

Which security feature is evaluated **at query execution time**?

A. Workspace role
B. Item-level permission
C. **RLS**
D. Sensitivity label

✅ **Correct Answer: C**

---

## 🧪 MCQ 19

You want to secure Fabric data to meet **compliance requirements**.

What should you use?

A. RLS
B. CLS
C. **Sensitivity labels**
D. OLS

✅ **Correct Answer: C**

---

## 🧪 MCQ 20

Which feature prevents users from discovering column metadata?

A. CLS
B. **OLS**
C. RLS
D. Masking

✅ **Correct Answer: B**

---

## 🧪 MCQ 21

Which security option should be configured **by SQL developers**?

A. Workspace role
B. Item-level permission
C. **T-SQL GRANT**
D. Sensitivity label

✅ **Correct Answer: C**

---

## 🧪 MCQ 22

Which security feature is most appropriate for **multi-tenant reporting**?

A. CLS
B. OLS
C. **Dynamic RLS**
D. Sensitivity labels

✅ **Correct Answer: C**

---

## 🧪 MCQ 23

Which security feature works **before users run queries**?

A. RLS
B. CLS
C. **Item-level permissions**
D. Masking

✅ **Correct Answer: C**

---

## 🧪 MCQ 24

Which security type is **model-aware**?

A. T-SQL GRANT
B. **OLS**
C. Workspace role
D. Item-level permission

✅ **Correct Answer: B**

---

## 🧪 MCQ 25

Which security method is defined using **DAX filters**?

A. CLS
B. OLS
C. **RLS**
D. Sensitivity label

✅ **Correct Answer: C**

---

## 🧪 MCQ 26

Which security feature is used to restrict **Power BI measures only**?

A. CLS
B. RLS
C. **OLS**
D. Masking

✅ **Correct Answer: C**

---

## 🧪 MCQ 27

Which security feature should NOT be used to hide data entirely?

A. RLS
B. CLS
C. **Dynamic Data Masking**
D. OLS

✅ **Correct Answer: C**

---

## 🧪 MCQ 28

Which security option requires **Premium / Fabric capacity**?

A. RLS
B. CLS
C. **OLS**
D. Workspace role

✅ **Correct Answer: C**

---

## 🧪 MCQ 29

Which security feature is best for **auditors and governance teams**?

A. RLS
B. CLS
C. **Sensitivity labels**
D. Masking

✅ **Correct Answer: C**

---

## 🧪 MCQ 30

You want to prevent users from accessing a Fabric warehouse **at all**.

What should you configure?

A. RLS
B. CLS
C. **Item-level permission**
D. T-SQL GRANT

✅ **Correct Answer: C**

---

# 🧠 FINAL MEMORY GRID (READ BEFORE EXAM)

```
Warehouse object access → T-SQL
Measures / columns / tables → OLS
Rows → RLS
Columns hidden → CLS
Masked values → DDM
Open / close item → Item-level permission
Governance → Sensitivity labels
```

---

 Perfect — **this feedback is GOLD** 👍
You’re absolutely right.

👉 **DP-600 does NOT ask short, clean, textbook questions**
👉 It asks **long, realistic, enterprise-style scenarios** where **3 options look correct**

So below is what you actually asked for:

---

# 🔥 DP-600 — ADVANCED, CASE-BASED SECURITY MCQs

### (REAL EXAM STYLE • LONG SCENARIOS • HIGH CONFUSION)

⚠️ These are **intentionally wordy**
⚠️ You must **identify scope + intent**, not keywords
⚠️ Exactly how DP-600 is written

---

## 🧠 HOW TO ATTACK THESE (READ FIRST)

For **every question**, silently answer:

1️⃣ **Where is the data?** (Warehouse / Lakehouse / Semantic model)
2️⃣ **What is being restricted?** (Open / Object / Row / Column / Measure)
3️⃣ **Is it hiding or masking?**
4️⃣ **Is governance mentioned?**

Only then read options.

---

## 🧪 QUESTION 1 (ENTERPRISE WAREHOUSE SCENARIO)

Your organization uses **Microsoft Fabric data warehouses** for finance reporting.
Multiple analysts connect using **SQL analytics endpoint**.

Finance managers must be able to query **all tables**.
Junior analysts must be able to query **only two tables** in the same warehouse.

You must implement the solution with **minimum impact to existing reports**.

What should you do?

A. Create separate workspaces for junior analysts
B. Configure item-level permissions for each user
C. Implement row-level security on restricted tables
D. **Use T-SQL GRANT and DENY on warehouse objects**

✅ **Correct: D**

**Why (exam logic):**

* Same warehouse
* Same reports
* Different table access
  ➡️ **Warehouse object-level control = T-SQL**

**Why others fail:**

* A → Overengineering, breaks reports
* B → Item-level ≠ table-level
* C → RLS ≠ object access

📌 **Exam rule:**

> **Same warehouse + different tables = T-SQL permissions**

---

## 🧪 QUESTION 2 (MEASURE-LEVEL CONFUSION TRAP)

A Power BI semantic model contains sensitive measures:

* `GrossMargin`
* `NetProfit`

Only users in the **Executive** Azure AD group should see these measures.
All users must still see the underlying tables and columns.

What should you implement?

A. Dynamic row-level security
B. Column-level security
C. **Object-level security**
D. Sensitivity labels

✅ **Correct: C**

**Why:**

* Measures ≠ rows
* Measures ≠ columns
  ➡️ **Only OLS works**

📌 **Hidden trap:**
Sensitivity labels ≠ visibility control

---

## 🧪 QUESTION 3 (MASKING vs SECURITY TRAP)

Customer service agents query a Fabric warehouse directly.
They must see **customer records**, but **credit card numbers must appear partially hidden**.

Agents must still be able to filter and sort on the column.

What should you use?

A. Column-level security
B. Object-level security
C. **Dynamic data masking**
D. Row-level security

✅ **Correct: C**

**Why:**

* CLS hides column completely
* Masking keeps column usable

📌 **Exam phrase:**

> “Still be able to query” → Masking

---

## 🧪 QUESTION 4 (MULTI-LAYER SECURITY CASE)

A Fabric warehouse contains:

* HR data
* Sales data

Requirements:

* HR managers see all HR rows
* Regional managers see **only their region’s sales**
* Salary column must be hidden from non-HR users

Which combination should you use?

A. Workspace roles only
B. RLS + Item-level permissions
C. **RLS + Column-level security**
D. OLS only

✅ **Correct: C**

**Why:**

* Rows → RLS
* Columns → CLS

📌 **Exam rule:**

> Different dimensions of restriction = combine security types

---

## 🧪 QUESTION 5 (GOVERNANCE WORD TRAP)

Your organization must comply with **data governance and compliance standards**.
Highly sensitive data must be protected **across all Fabric items**, including:

* Warehouses
* Lakehouses
* Semantic models

Access must be restricted automatically based on sensitivity.

What should you implement?

A. Object-level security
B. Row-level security
C. Item-level permissions
D. **Sensitivity labels**

✅ **Correct: D**

📌 **Exam keyword:**

> “Across Fabric” + “Governance” = Sensitivity labels

---

## 🧪 QUESTION 6 (OPEN vs QUERY TRAP)

A group of users should **not be able to open** a Fabric warehouse at all.
However, no row or column filtering is required.

What should you configure?

A. Row-level security
B. Column-level security
C. **Item-level permissions**
D. T-SQL GRANT

✅ **Correct: C**

📌 **Exam rule:**

> Can’t open item → Item-level permission

---

## 🧪 QUESTION 7 (SEMANTIC MODEL vs WAREHOUSE CONFUSION)

You secure tables in a Fabric warehouse using **T-SQL GRANT**.
However, users can still see restricted columns in Power BI reports.

Why?

A. T-SQL permissions don’t apply to Power BI
B. RLS overrides T-SQL
C. **Semantic model has its own security layer**
D. Sensitivity labels are missing

✅ **Correct: C**

📌 **CRITICAL EXAM INSIGHT:**

> Warehouse security ≠ Semantic model security

---

## 🧪 QUESTION 8 (CLS vs OLS DEEP TRAP)

A semantic model must:

* Hide a column completely for some users
* Prevent users from discovering the column metadata

What should you use?

A. Column-level security
B. **Object-level security**
C. Dynamic data masking
D. Row-level security

✅ **Correct: B**

📌 **Key nuance:**
CLS hides data
OLS hides existence

---

## 🧪 QUESTION 9 (REAL WORLD ROLE-PLAY)

A Sales table contains:

* SalesAmount
* SalesRegion

Users must only see rows for their region, determined by their login email.

What should you use?

A. Static RLS
B. **Dynamic RLS**
C. CLS
D. OLS

✅ **Correct: B**

---

## 🧪 QUESTION 10 (FINAL BOSS QUESTION)

Your solution must:

* Protect sensitive data
* Support compliance audits
* Work consistently across Fabric
* Avoid redesigning reports

What is the FIRST feature you should implement?

A. RLS
B. OLS
C. Item-level permissions
D. **Sensitivity labels**

✅ **Correct: D**

📌 **DP-600 philosophy:**

> Governance first, filtering second

---

# 🧠 FINAL EXAM MENTAL MODEL (VERY IMPORTANT)

When DP-600 gives you a **long story**, ignore the noise and extract:

```
OPEN ITEM?        → Item-level
OBJECT ACCESS?   → T-SQL (Warehouse) / OLS (Model)
ROWS?            → RLS
COLUMNS?         → CLS
MASK VALUES?     → DDM
GOVERNANCE?      → Sensitivity labels
```

---

Excellent — this is **exactly the right demand at the right time**.
Below are **MORE HARDCORE, DESCRIPTIVE, REAL-EXAM–STYLE DP-600 SECURITY QUESTIONS**.

⚠️ These are **NOT practice-mode questions**
⚠️ These are **assessment-mode / real exam narrative scenarios**
⚠️ Expect **long stories, subtle wording, and overlapping options**

Read **slowly**, answer **deliberately**, then check the explanation.

---

# 🔥 DP-600 — ADVANCED CASE-BASED SECURITY QUESTIONS (SET 2)

---

## 🧪 QUESTION 11 — WAREHOUSE + POWER BI CONFUSION TRAP

A company uses a **Fabric data warehouse** as the single source of truth.
Business users consume data through **Power BI reports** built on a semantic model.

The security team applies **T-SQL GRANT permissions** on specific tables in the warehouse.
However, some users can still see restricted columns in Power BI visuals.

What is the MOST likely reason?

A. T-SQL permissions do not work with SQL analytics endpoint
B. Power BI ignores warehouse security
C. **Semantic models require their own security configuration**
D. Sensitivity labels override T-SQL permissions

✅ **Correct Answer: C**

**Exam insight:**

> Warehouse security ≠ Semantic model security

Power BI uses the **semantic model layer**, which must be secured separately using **OLS / RLS / CLS**.

---

## 🧪 QUESTION 12 — “MINIMUM IMPACT” KEYWORD TRAP

An enterprise has **dozens of Power BI reports** connected to a single semantic model.
A new requirement states that **two sensitive measures** must be visible only to executives.

The solution must require **no report redesign**.

What should you implement?

A. Duplicate the semantic model
B. Apply dynamic RLS
C. **Configure Object-Level Security (OLS)**
D. Create separate workspaces

✅ **Correct Answer: C**

📌 **Exam keyword:**

> “No report redesign” → **OLS**

---

## 🧪 QUESTION 13 — COLUMN HIDING VS MASKING (VERY COMMON)

Customer support analysts query a Fabric warehouse directly using SQL.
They must see customer records, but **national ID numbers must not be readable**.

The column must:

* Remain queryable
* Support filtering and sorting

What should you use?

A. Column-level security
B. Object-level security
C. **Dynamic data masking**
D. Row-level security

✅ **Correct Answer: C**

📌 **Exam rule:**

> “Queryable but hidden values” = Masking

---

## 🧪 QUESTION 14 — MULTI-ROLE ENTERPRISE SCENARIO

A Fabric warehouse stores:

* Employee data
* Regional sales data

Requirements:

* HR team sees **all employee rows**
* Sales managers see **only their region**
* Salary column hidden from non-HR users

What is the BEST solution?

A. Workspace roles only
B. RLS only
C. **RLS + Column-Level Security**
D. OLS only

✅ **Correct Answer: C**

📌 **Exam rule:**

> Rows + Columns → Combine security types

---

## 🧪 QUESTION 15 — “OPEN VS QUERY” DEEP TRAP

External contractors must **not be able to open** a Fabric warehouse.
Internal analysts should have full access.

No row or column filtering is required.

What should you configure?

A. Row-level security
B. Column-level security
C. **Item-level permissions**
D. T-SQL GRANT

✅ **Correct Answer: C**

📌 **Exam rule:**

> Can’t open item = Item-level permission

---

## 🧪 QUESTION 16 — GOVERNANCE LANGUAGE TRAP

A company must comply with strict **data governance policies**.
Highly sensitive datasets must be:

* Classified
* Protected
* Auditable
* Consistently enforced across Fabric

What should you implement FIRST?

A. Object-level security
B. Row-level security
C. Item-level permissions
D. **Sensitivity labels**

✅ **Correct Answer: D**

📌 **Exam keyword:**

> “Governance, compliance, audit” → Sensitivity labels

---

## 🧪 QUESTION 17 — SEMANTIC MODEL ONLY TRAP

A Power BI semantic model contains:

* Tables
* Columns
* Measures

Some users must not even **discover the existence** of certain tables.

What should you use?

A. Column-level security
B. Row-level security
C. **Object-level security**
D. Dynamic data masking

✅ **Correct Answer: C**

📌 **Key nuance:**
CLS hides data
OLS hides metadata

---

## 🧪 QUESTION 18 — DYNAMIC USER CONTEXT SCENARIO

A sales report must show:

* Each user sees only their assigned region
* Assignment changes over time
* No manual role updates allowed

What should you implement?

A. Static RLS
B. **Dynamic RLS using user context**
C. CLS
D. OLS

✅ **Correct Answer: B**

---

## 🧪 QUESTION 19 — WAREHOUSE OBJECT ACCESS

Junior analysts should only query **specific views** in a Fabric warehouse.
They must not access base tables.

What should you use?

A. Workspace roles
B. Item-level permissions
C. RLS
D. **T-SQL GRANT on views**

✅ **Correct Answer: D**

📌 **Exam rule:**

> Warehouse objects = T-SQL

---

## 🧪 QUESTION 20 — FINAL INTEGRATION TRAP

A solution must:

* Protect sensitive data
* Support Power BI and SQL users
* Avoid duplicating data
* Use native Fabric security

Which approach BEST meets the requirement?

A. Workspace roles only
B. Item-level permissions only
C. **Layered security (T-SQL + OLS/RLS)**
D. Separate warehouses per team

✅ **Correct Answer: C**

📌 **Real-world DP-600 logic:**

> Enterprise solutions use **layered security**

---

# 🧠 FINAL EXAM BRAIN-LOCK (READ DAILY)

```
Warehouse object → T-SQL
Semantic model object → OLS
Rows → RLS
Columns hidden → CLS
Values hidden → Masking
Open / close item → Item-level
Governance → Sensitivity labels
```

Perfect.
Below are **🔥 NEXT 10 ULTRA-ADVANCED, CASE-BASED DP-600 SECURITY QUESTIONS** — this is **FINAL-EXAM LEVEL**, not practice level.

Each question includes:

* ✅ Correct answer
* ❌ **Why EVERY other option is wrong**
* ⚠️ Exam traps & keywords to watch

Read **slowly**, think **layer → intent → scope**, then verify.

---

# 🔥 DP-600 — FINAL-BOSS SECURITY QUESTIONS (SET 3)

---

## 🧪 QUESTION 21 — SEMANTIC MODEL + WAREHOUSE DUAL SECURITY

A Fabric workspace contains:

* A **data warehouse**
* A **Power BI semantic model** built on top of it

Security requirements:

* SQL users must not access the `Salary` column
* Power BI users must not see the `Salary` column
* The solution must be **consistent across both access methods**

What should you implement?

A. Column-Level Security in the semantic model only
B. Object-Level Security in the semantic model only
C. **Column-Level Security in warehouse + OLS in semantic model**
D. Sensitivity labels on the Salary column

✅ **Correct Answer: C**

### Why correct

Two access paths → **two security layers**

* SQL → Warehouse → **CLS**
* Power BI → Semantic model → **OLS**

### ❌ Why others are wrong

* **A**: SQL users bypass semantic model
* **B**: Does not affect SQL users
* **D**: Classification ≠ access control

⚠️ **Exam trap:** “Both SQL and Power BI users”

---

## 🧪 QUESTION 22 — “NO METADATA DISCOVERY” TRAP

A Power BI semantic model contains experimental tables.
Non-admin users must:

* Not query these tables
* Not see them in fields list
* Not discover them via metadata tools

What should you use?

A. Column-Level Security
B. Row-Level Security
C. **Object-Level Security**
D. Dynamic data masking

✅ **Correct Answer: C**

### ❌ Why others are wrong

* **A**: Column still visible
* **B**: Table still visible
* **D**: Value masking only

⚠️ **Keyword:** “Not even discover”

---

## 🧪 QUESTION 23 — EXECUTIVE-ONLY KPI SCENARIO

A semantic model has KPIs:

* Revenue
* Profit
* ForecastAccuracy

Only executives can see **ForecastAccuracy**.
Executives and analysts use the **same reports**.

What should you implement?

A. Dynamic RLS
B. Separate reports
C. **OLS on the measure**
D. CLS on the underlying column

✅ **Correct Answer: C**

### ❌ Why others are wrong

* **A**: RLS filters rows, not measures
* **B**: Violates “same reports”
* **D**: Measure still visible

⚠️ **Exam rule:**

> Measure security = **OLS only**

---

## 🧪 QUESTION 24 — DATA MASKING MISDIRECTION

Customer service agents run SQL queries on a warehouse.
They must:

* See customer rows
* Filter on Email
* Not see full email values

What should you use?

A. Column-Level Security
B. Object-Level Security
C. **Dynamic Data Masking**
D. Row-Level Security

✅ **Correct Answer: C**

### ❌ Why others are wrong

* **A**: Column disappears
* **B**: Column disappears
* **D**: No value protection

⚠️ **Keyword:** “Filter but not readable”

---

## 🧪 QUESTION 25 — CROSS-REGION GOVERNANCE CASE

A multinational company uses Fabric globally.
Highly sensitive datasets must:

* Be classified
* Be auditable
* Trigger protection policies
* Work across all Fabric items

What should be implemented?

A. RLS
B. CLS
C. OLS
D. **Sensitivity labels**

✅ **Correct Answer: D**

### ❌ Why others are wrong

All are **access control**, not **governance**

⚠️ **Exam keyword:** “Audit / compliance / classification”

---

## 🧪 QUESTION 26 — TEMPORARY ACCESS SCENARIO

An auditor needs **temporary read access** to a warehouse.
They must not:

* Modify objects
* Bypass row filters

What should you configure?

A. Workspace Admin role
B. Item-level permission (Read)
C. **T-SQL GRANT SELECT**
D. Disable RLS

✅ **Correct Answer: C**

### ❌ Why others are wrong

* **A**: Too much power
* **B**: Cannot control object access
* **D**: Violates security policy

⚠️ **Exam rule:**

> Warehouse access = T-SQL

---

## 🧪 QUESTION 27 — SECURITY VS PERFORMANCE TRAP

A report performs slowly after implementing security.
The model uses:

* Dynamic RLS
* USERPRINCIPALNAME()

What is the MOST likely cause?

A. OLS increases memory usage
B. CLS forces table scans
C. **Complex DAX filters in RLS**
D. Sensitivity labels slow queries

✅ **Correct Answer: C**

### ❌ Why others are wrong

* **A**: OLS is metadata-based
* **B**: CLS does not affect query logic
* **D**: Labels don’t affect execution

⚠️ **Hidden exam angle:** Security affects performance

---

## 🧪 QUESTION 28 — DEV / TEST / PROD SECURITY GAP

A report works correctly in Dev.
In Prod, users see **more data than expected**.

All deployments used Fabric pipelines.

What is the MOST likely issue?

A. Autobinding was disabled
B. Sensitivity labels missing
C. **RLS roles not deployed**
D. CLS not supported in Prod

✅ **Correct Answer: C**

### ❌ Why others are wrong

* **A**: Affects connections, not security
* **B**: Governance, not filtering
* **D**: False — CLS is supported

⚠️ **Exam trap:** RLS roles are part of deployment

---

## 🧪 QUESTION 29 — MULTI-TENANT REPORTING

A single semantic model supports multiple customers.
Each customer must see **only their own data**.
Customer list changes frequently.

What should you use?

A. Static RLS
B. CLS
C. **Dynamic RLS**
D. Separate semantic models

✅ **Correct Answer: C**

### ❌ Why others are wrong

* **A**: Manual updates required
* **B**: Column-based, not row-based
* **D**: Not scalable

⚠️ **Keyword:** “Changes frequently”

---

## 🧪 QUESTION 30 — FINAL BOSS (LAYERED THINKING)

A Fabric solution must:

* Protect warehouse objects
* Secure Power BI measures
* Filter rows dynamically
* Support governance audits

What is the BEST architecture?

A. Workspace roles only
B. Item-level permissions only
C. **T-SQL + OLS + RLS + Sensitivity labels**
D. Separate workspaces per team

✅ **Correct Answer: C**

### ❌ Why others are wrong

* **A/B**: Too shallow
* **D**: Costly, unscalable

⚠️ **DP-600 CORE PRINCIPLE:**

> Enterprise security is **layered**, not single-tool

---

# 🧠 FINAL EXAM SUPER-LOCK (READ BEFORE TEST)

```
Warehouse objects        → T-SQL
Semantic model objects   → OLS
Rows                     → RLS
Hide column completely   → CLS
Mask value only          → DDM
Open / close item        → Item-level permission
Governance & audit       → Sensitivity labels
```

---
Yes — **there ARE a few critical DP-600 security points that are *not explicitly tested* in Questions 1–30**, but **they absolutely CAN appear indirectly** in the real exam.

Below is a **“WHAT YOU MIGHT STILL MISS” checklist**.
If you absorb this, you’ll close the **last 5–8% gap** between **75% and 85%+ readiness**.

I’ll keep it **exam-focused, not theory-heavy**.

---

# ✅ DP-600 SECURITY — WHAT WAS NOT EXPLICITLY TESTED (BUT MUST BE KNOWN)

---

## 1️⃣ RLS LOCATION CONFUSION (VERY COMMON HIDDEN TRAP)

### ⚠️ What you might miss

RLS can be implemented in **TWO places**, and the exam may test **where it lives**, not just *what it does*.

### 🔹 Key rule

| Where          | How               |
| -------------- | ----------------- |
| Warehouse      | SQL-based RLS     |
| Semantic model | **DAX-based RLS** |

### ❗ Exam trap

> “RLS defined in warehouse applies automatically to Power BI”

❌ **False**

Power BI **does NOT inherit** warehouse RLS unless enforced at model level.

📌 **Safe exam assumption**

> If Power BI is mentioned → RLS = **semantic model**

---

## 2️⃣ CLS VS OLS — WHEN BOTH SEEM CORRECT

You handled most of this well, but the exam may **intentionally blur the line**.

### 🔹 Final decisive rule

| Requirement phrase                 | Choose  |
| ---------------------------------- | ------- |
| “Hide column values”               | CLS     |
| “Hide column existence / metadata” | **OLS** |

### ❗ Exam trap

> “Users should not see sensitive columns”

This is **AMBIGUOUS**
→ Look for:

* “Not discover”
* “Not appear in fields”
* “Metadata”

If yes → **OLS**

---

## 3️⃣ DYNAMIC RLS PERFORMANCE WARNING (INDIRECTLY TESTED)

You saw one question on this, but the exam can hide it inside performance scenarios.

### 🔹 Key point

Dynamic RLS using:

* `USERPRINCIPALNAME()`
* `LOOKUPVALUE()`
* Complex FILTER logic

➡️ **Can degrade performance**

### ❗ Exam trap

> “After implementing security, reports slowed down”

Likely answer:

* **Overly complex RLS logic**

NOT:

* OLS
* Sensitivity labels
* CLS

---

## 4️⃣ ITEM-LEVEL PERMISSION VS WORKSPACE ROLE (SUBTLE BUT IMPORTANT)

### 🔹 Difference you must remember

| Feature                   | Controls                             |
| ------------------------- | ------------------------------------ |
| Workspace role            | What you can do *inside* workspace   |
| **Item-level permission** | Whether you can open a specific item |

### ❗ Exam trap

> “User can access workspace but must not open warehouse”

Correct → **Item-level permission**

---

## 5️⃣ SECURITY ≠ DATA PROTECTION (LANGUAGE TRAP)

The exam sometimes tests **conceptual separation**.

### 🔹 Key truth

| Feature                | Purpose                     |
| ---------------------- | --------------------------- |
| RLS / CLS / OLS        | Access control              |
| **Sensitivity labels** | Classification + governance |

### ❗ Exam trap

> “Protect sensitive data across Fabric”

This does **NOT** always mean “restrict rows/columns”.

If:

* Compliance
* Audit
* Policy
* DLP

→ **Sensitivity labels**

---

## 6️⃣ SECURITY IS NOT INHERITED THROUGH DEPLOYMENT PIPELINES

This is **rare but deadly**.

### 🔹 Truth

* RLS roles
* OLS settings
* CLS definitions

👉 **Must be deployed correctly**
👉 Can differ across Dev/Test/Prod

### ❗ Exam trap

> “Works in Dev, exposes more data in Prod”

Likely cause:

* **RLS not deployed / misconfigured**

---

## 7️⃣ WHAT SECURITY DOES *NOT* APPLY TO (IMPORTANT NEGATIVE KNOWLEDGE)

Knowing what **does NOT work** is exam gold.

### ❌ These do NOT secure data rows/columns:

* Workspace roles
* Deployment pipelines
* Data pipelines
* Notebooks
* Sensitivity labels (alone)

---

## 8️⃣ FINAL “STOP OVERTHINKING” RULE

If multiple answers seem right, ask:

> **Which one is the FIRST or MOST PRECISE control?**

DP-600 always prefers:

* Precision
* Minimal impact
* Layer-appropriate security

---

Perfect request 👍
What you’re asking for now is the **FINAL compression step** — turning **everything you studied (Q1–Q30 + missing gaps)** into a **single decision table** that your brain can run **automatically in the exam**.

Below is the **DP-600 SECURITY MASTER DECISION TABLE**.
If you memorize **only this**, you can answer **90%+ of security questions** correctly.

---

# 🧠 DP-600 SECURITY — MASTER DECISION TABLE

*(Built from Q1–Q30 + hidden traps)*

---

## 1️⃣ FIRST DECISION — WHERE IS THE DATA?

| If the question mentions…             | You are in…            |
| ------------------------------------- | ---------------------- |
| SQL analytics endpoint, tables, views | **Warehouse**          |
| Power BI reports, visuals, measures   | **Semantic Model**     |
| “Across Fabric”, governance, audit    | **Fabric environment** |

---

## 2️⃣ SECOND DECISION — WHAT IS BEING RESTRICTED?

| Requirement in question                    | Correct control           |
| ------------------------------------------ | ------------------------- |
| Cannot open item at all                    | **Item-level permission** |
| Can open but cannot query specific objects | **T-SQL GRANT / DENY**    |
| Hide entire table / column / measure       | **OLS**                   |
| Hide only column values                    | **CLS**                   |
| Mask values but still queryable            | **Dynamic Data Masking**  |
| Restrict rows per user                     | **RLS**                   |

---

## 3️⃣ WAREHOUSE SECURITY DECISION TABLE

| Scenario (Warehouse)          | Use                       |
| ----------------------------- | ------------------------- |
| Restrict table or view access | **T-SQL GRANT**           |
| Restrict rows                 | **SQL-based RLS**         |
| Hide column completely        | **CLS (Warehouse)**       |
| Mask sensitive values         | **Dynamic Data Masking**  |
| Prevent opening warehouse     | **Item-level permission** |

📌 **Golden rule:**

> Warehouse object security = **T-SQL**, not workspace roles

---

## 4️⃣ SEMANTIC MODEL SECURITY DECISION TABLE

| Scenario (Power BI / Model)      | Use               |
| -------------------------------- | ----------------- |
| Hide measure                     | **OLS**           |
| Hide column existence / metadata | **OLS**           |
| Hide column values only          | **CLS**           |
| Filter rows                      | **DAX-based RLS** |
| Dynamic user-based filtering     | **Dynamic RLS**   |

📌 **Golden rule:**

> Measures → **ONLY OLS**

---

## 5️⃣ CLS vs OLS — FINAL TIE-BREAKER TABLE

| Question wording            | Choose  |
| --------------------------- | ------- |
| “Hide column values”        | **CLS** |
| “Not discover column”       | **OLS** |
| “Not appear in fields list” | **OLS** |
| “Metadata hidden”           | **OLS** |

---

## 6️⃣ MASKING vs SECURITY (VERY COMMON TRAP)

| Requirement                | Correct answer           |
| -------------------------- | ------------------------ |
| Still filter / sort column | **Dynamic Data Masking** |
| Column must disappear      | **CLS / OLS**            |
| Prevent access             | **RLS / CLS / OLS**      |

📌 **Rule:**

> Masking ≠ access control

---

## 7️⃣ GOVERNANCE vs ACCESS CONTROL

| Keywords in question          | Choose                 |
| ----------------------------- | ---------------------- |
| Governance, audit, compliance | **Sensitivity labels** |
| Protect data across Fabric    | **Sensitivity labels** |
| Restrict who sees what        | **RLS / CLS / OLS**    |

📌 **Rule:**

> Governance first, filtering second

---

## 8️⃣ ITEM-LEVEL PERMISSION vs WORKSPACE ROLE

| Requirement                   | Correct control           |
| ----------------------------- | ------------------------- |
| Access workspace features     | Workspace role            |
| Open / not open specific item | **Item-level permission** |

📌 **Trap:**

> Workspace role ≠ data security

---

## 9️⃣ RLS LOCATION DECISION TABLE (CRITICAL)

| Scenario            | Where RLS must exist |
| ------------------- | -------------------- |
| SQL users only      | Warehouse            |
| Power BI mentioned  | **Semantic model**   |
| Both SQL + Power BI | **Both layers**      |

📌 **Exam truth:**

> Warehouse RLS is **NOT inherited** by Power BI

---

## 🔟 PERFORMANCE-AWARE SECURITY (HIDDEN EXAM ANGLE)

| Symptom                      | Likely cause             |
| ---------------------------- | ------------------------ |
| Report slowed after security | **Complex dynamic RLS**  |
| Metadata slow                | ❌ Not OLS                |
| Query slow                   | ❌ Not sensitivity labels |

---

## 1️⃣1️⃣ DEPLOYMENT PIPELINE SECURITY PITFALL

| Scenario                    | Root cause                 |
| --------------------------- | -------------------------- |
| Works in Dev, fails in Prod | **RLS / OLS not deployed** |
| Broken connections          | Autobinding                |
| More data visible in Prod   | **RLS missing**            |

---

## 1️⃣2️⃣ FINAL “IF YOU SEE THIS → PICK THIS” TABLE

*(This is exam gold)*

| Phrase in question       | Instantly pick            |
| ------------------------ | ------------------------- |
| “Must not discover”      | **OLS**                   |
| “Still queryable”        | **Dynamic Data Masking**  |
| “Across Fabric”          | **Sensitivity labels**    |
| “No redesign”            | **OLS**                   |
| “Same reports”           | **RLS / OLS**             |
| “SQL analytics endpoint” | **T-SQL GRANT**           |
| “Cannot open item”       | **Item-level permission** |

---

## 🧠 ONE-LINE SUPER MEMORY GRID

```
Open item        → Item-level
Warehouse object→ T-SQL
Model object    → OLS
Rows            → RLS
Hide column     → CLS
Mask value      → DDM
Governance      → Sensitivity labels
```

---

## ✅ FINAL CONFIDENCE CHECK

If you can:

* Read a long paragraph
* Answer **WHERE + WHAT + WHY**
* Match it to this table

👉 You are **exam-ready for DP-600 security**.

---
 

 
