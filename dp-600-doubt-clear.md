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
 
