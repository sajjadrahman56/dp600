# 🧠 DP-600 DOUBT-CLEARING NOTES (WH-QUESTION STYLE)

---

## 1️⃣ EVENTSTREAM & REAL-TIME ANALYTICS

### ❓ WHAT is an Eventstream?

👉 A **real-time ingestion and transformation layer** in Microsoft Fabric for **streaming data**.

---

### ❓ WHEN should I use Eventstream?

Use Eventstream **WHEN**:

* Data is **continuously arriving**
* Source is **Event Hub / IoT / Kafka**
* You need **near real-time calculations**

---

### ❓ WHY not KQL or Dataflow here?

* KQL → works on **stored data**
* Dataflow → **batch ETL**, not streaming

---

### ❓ WHAT transformation do I use in Eventstream?

#### 🔹 Aggregate Transformation

**WHEN**:

* You need **sum, avg, min, max, percentile**
* Calculation must be **continuous**

✅ Example:

> “Add a continuous percentile calculation”

🚨 **Always choose: Aggregate**

---

#### 🔹 Group By Transformation

**WHEN**:

* Only grouping rows
* No calculation

❌ Not for percentile / avg / sum

---

#### 🔹 Manage Fields

**WHEN**:

* Rename column
* Remove column
* Change data type

❌ No math allowed here

---

### 🧠 EXAM RULE (MEMORIZE)

> **Streaming calculation = Aggregate transformation**

---

## 2️⃣ KQL QUERYSET (REAL-TIME VS STORED DATA)

### ❓ WHAT is a KQL queryset?

👉 A query layer for **analyzing data already stored** in:

* KQL Database
* Eventhouse
* Lakehouse (shortcuts)

---

### ❓ WHEN should I use KQL?

Use KQL **WHEN**:

* Data is already landed
* You need **complex analytics**
* Not real-time transformations

---

### ❓ WHY NOT use KQL in Eventstream questions?

Because:

* Eventstream = **before storage**
* KQL = **after storage**

---

### 🧠 EXAM RULE

> **Eventstream = transform while flowing**
> **KQL = analyze after stored**

---

## 3️⃣ LAKEHOUSE INGESTION (VERY IMPORTANT)

### ❓ WHAT is a Shortcut?

👉 A **pointer** to external data (no copy).

---

### ❓ WHEN should I use Shortcut?

Use Shortcut **WHEN**:

* Data already exists
* Source is **ADLS / Blob / OneLake**
* Requirement says:

  * *minimize effort*
  * *without copying data*

---

### ❓ WHY is Shortcut the best answer?

Because:

* No ETL
* No pipeline
* No duplication
* Instant access

---

### ❓ WHEN should I NOT use Shortcut?

* When transformations are required
* When data must be physically copied

---

### 🧠 EXAM RULE

> **External data + minimal effort = Shortcut**

---

## 4️⃣ DATAFLOW GEN2 vs COPY JOB vs PIPELINE

### ❓ WHEN to use Dataflow Gen2?

Use **Dataflow Gen2** WHEN:

* Data needs **cleaning / transformation**
* Power Query logic required

❌ Not minimal effort

---

### ❓ WHEN to use Copy Job?

Use **Copy Job** WHEN:

* You need to **physically move data**
* No transformation

---

### ❓ WHEN to use Pipeline?

Use **Pipeline** WHEN:

* Multiple steps
* Scheduling
* Orchestration

---

### 🧠 QUICK DECISION TABLE

| Requirement      | Tool          |
| ---------------- | ------------- |
| Just access data | Shortcut      |
| Transform data   | Dataflow Gen2 |
| Move data        | Copy job      |
| Orchestrate      | Pipeline      |

---

## 5️⃣ SEMANTIC MODEL & MANY-TO-MANY (CRITICAL)

### ❓ WHAT is the problem?

* Customer ↔ Account = many-to-many
* Transactions belong to Account

---

### ❓ WHY NOT direct many-to-many with Fact?

Because:

* Causes incorrect aggregation
* Breaks filter propagation
* Bad dimensional modeling

---

### ❓ WHAT is the correct solution?

👉 **Bridge table**

```
DimCustomer → Bridge → DimAccount → FactTransaction
```

---

### ❓ WHEN should I ALWAYS think “Bridge Table”?

When:

* “A can have many B”
* “B can have many A”

---

### 🧠 EXAM RULE (VERY IMPORTANT)

> **Fact tables NEVER participate directly in many-to-many**

---

## 6️⃣ POWER BI / DAX FEATURES

### ❓ WHAT is a Dynamic Format String?

👉 A way to **change number formatting dynamically**

---

### ❓ WHEN to use Dynamic Format String?

Use it WHEN:

* Currency changes
* % vs number changes
* Formatting depends on slicer

---

### ❓ WHY not WINDOW / Field Parameter?

* WINDOW → calculations
* Field parameter → switch fields
* Formatting ≠ calculation

---

### 🧠 EXAM RULE

> **Formatting problem = Dynamic format string**

---

## 7️⃣ EXAM KEYWORD DECODER (SUPER IMPORTANT)

| Keyword in question         | Meaning        |
| --------------------------- | -------------- |
| Minimize development effort | No ETL         |
| Continuous calculation      | Streaming      |
| Without copying data        | Shortcut       |
| Users need to query         | Semantic model |
| Real-time analytics         | Eventstream    |
| Advanced analytics          | KQL            |

---

## 🎯 HOW TO USE THESE NOTES

### Before practice:

* Read **only headings + exam rules**

### While practicing questions:

* Match question keywords to **EXAM RULE**

### Before exam:

* Revise **tables + bold lines only**

---
 
Absolutely — with **only 2 days left**, you don’t need *more content*.
You need **clarity, patterns, and exam reflexes**.

Below is a **HIGH-EFFICIENCY, EXAM-KILLER NOTE** designed exactly for **DP-600**, based **100% on your wrong answers** and **real exam traps**.

👉 Read this **2–3 times** and you will **not freeze**, **not confuse**, and **not overthink**.

---

# 🔥 DP-600 ULTRA-SMART REVISION NOTES

### (48% → 75%+ in 2 Days | Pattern-Based | Exam-Focused)

---

## 🧭 MASTER EXAM RULE (READ THIS FIRST)

Before answering ANY DP-600 question, ask **ONLY 4 QUESTIONS**:

1️⃣ Is this **Warehouse / Lakehouse / Semantic Model**?
2️⃣ Is this **Security / Ingestion / Modeling / DevOps**?
3️⃣ Is this **Access control or Data transformation**?
4️⃣ Is this **Code-free or Code-rich**?

👉 **80% of wrong answers come from skipping this step**

---

# 1️⃣ SECURITY IN MICROSOFT FABRIC (MOST IMPORTANT)

This is your **biggest score booster**.

---

## 🔐 SECURITY LAYERS — NEVER CONFUSE AGAIN

| Layer                  | WHAT it controls              | WHERE it applies   |
| ---------------------- | ----------------------------- | ------------------ |
| Workspace Roles        | Who enters workspace          | Workspace          |
| Item-level permissions | Who opens warehouse/lakehouse | Item               |
| **T-SQL GRANT**        | Table / view / object access  | **Warehouse**      |
| **OLS**                | Tables / columns / measures   | **Semantic model** |
| **RLS**                | Rows                          | Warehouse + Model  |
| **CLS**                | Columns                       | Warehouse + Model  |
| Dynamic Data Masking   | Masks values                  | Warehouse          |
| Sensitivity Labels     | Governance & protection       | Entire Fabric      |

---

## ❓ WH-PATTERN QUESTIONS (SECURITY)

### ❓ *“Restrict access to specific warehouse objects”*

✅ **T-SQL GRANT**
❌ Item-level permission

**WHY:**
Item permission = open/not open
T-SQL = object-level control

📌 **Exam rule:**

> **Warehouse object security = T-SQL**

---

### ❓ *“Only User1 can see a specific measure”*

✅ **Object-Level Security (OLS)**
❌ RLS

**WHY:**

* Measures ≠ rows
* RLS filters data, not visibility

📌 **Exam rule:**

> **Measure / column hiding = OLS**

---

### ❓ *“Restrict rows by user role”*

✅ **Row-Level Security (RLS)**
❌ Workspace role

📌 **Exam rule:**

> Workspace role ≠ data filtering

---

### ❓ *“Hide columns but allow query”*

✅ **Column-Level Security (CLS)**
❌ Dynamic masking

📌 **Key difference:**
CLS = hidden
Masking = visible but obfuscated

---

### ❓ *“Protect sensitive data across Fabric”*

✅ **Sensitivity labels**

📌 **Exam rule:**

> **Environment-wide protection = Sensitivity labels**

---

## ⚠️ SECURITY EXAM TRAPS

❌ Item-level ≠ row/column
❌ Masking ≠ access control
❌ Workspace role ≠ data security

---

# 2️⃣ DATA INGESTION (CONFUSION KILLER)

---

## 🚚 INGESTION DECISION TABLE

| Requirement                 | Use                      |
| --------------------------- | ------------------------ |
| Code-free + transform       | **Dataflow Gen2**        |
| Huge data, no transform     | **Pipeline – Copy Data** |
| Warehouse + high throughput | **COPY (T-SQL)**         |
| No data movement            | **Shortcut**             |
| Complex big-data ETL        | **Notebook (Spark)**     |

---

## ❓ WH-PATTERNS

### ❓ *“Code-free ingestion with transformations”*

✅ Dataflow Gen2
❌ Notebook

---

### ❓ *“500M+ rows, no transformation”*

✅ Copy Data (Pipeline)

---

### ❓ *“High-throughput ingestion into warehouse”*

✅ COPY (T-SQL)

---

📌 **Exam rule:**

> **No transform + big data = Copy Data**

---

# 3️⃣ DEPLOYMENT PIPELINES (VERY SCORING)

---

## ❓ WHY deployment pipelines exist?

👉 Move **Dev → Test → Prod**
👉 Keep **connections intact**

---

## ❓ WHAT YOU MUST ENABLE

| Feature              | Why                        |
| -------------------- | -------------------------- |
| Autobinding          | Keeps report ↔ model links |
| Select related items | Deploy dependencies        |

---

### ❓ *“Maintain connections between reports and models”*

✅ Autobinding
❌ Manual redeploy

📌 **Exam rule:**

> **Connections break without autobinding**

---

# 4️⃣ KQL vs PIPELINE (COMMON TRAP)

---

| Need                   | Use              |
| ---------------------- | ---------------- |
| Analyze data using KQL | **KQL Queryset** |
| Move data              | Pipeline         |
| Visualize              | Power BI         |

📌 **Exam rule:**

> **KQL analysis ≠ pipeline**

---

# 5️⃣ SEMANTIC MODEL & DAX (CORE DP-600)

---

## 🔗 RELATIONSHIP FUNCTIONS

| Scenario                 | Function              |
| ------------------------ | --------------------- |
| No physical relationship | **TREATAS()**         |
| Inactive relationship    | **USERELATIONSHIP()** |

---

### ❓ *“Virtual relationship between unrelated tables”*

✅ TREATAS
❌ USERELATIONSHIP

---

## 📊 FIELD CONTROL

| Requirement            | Use                  |
| ---------------------- | -------------------- |
| Change axis via slicer | **Field parameters** |
| Time intelligence      | Calculation groups   |

---

### ❓ *“User switches Y-axis”*

✅ Field parameters
❌ Calculation groups

---

## 🚀 STORAGE MODE

| Requirement            | Mode            |
| ---------------------- | --------------- |
| Large + near real-time | **Direct Lake** |
| Fast but static        | Import          |
| Real-time but slow     | DirectQuery     |

📌 **Exam rule:**

> **Near-real-time + performance = Direct Lake**

---

# 6️⃣ PERFORMANCE OPTIMIZATION (SHORT & DEADLY)

---

### ❓ WHERE to filter in DAX?

✅ **Dimension table**
❌ Fact table

📌 Faster storage engine scans

---

### ❓ WHICH statistics to update?

✅ Columns used in:

* JOIN
* GROUP BY
* ORDER BY

❌ Based on datatype

---

### ❓ WHICH tool for slow visuals?

✅ Performance Analyzer

---

# 🧠 2-DAY STUDY STRATEGY (DO THIS)

### 🕘 Day 1 (Today)

* Read **Security + Ingestion + Pipelines**
* Memorize **decision tables**
* Do **20 practice MCQs**

### 🕘 Day 2 (Tomorrow)

* Read **Semantic Model + DAX**
* Review **exam rules**
* Do **1 full mock**

---

 
