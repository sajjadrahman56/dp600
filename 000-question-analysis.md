Practice Assessment for Exam DP-600: Implementing Analytics Solutions Using Microsoft Fabric
Question 1 of 50

You have a Microsoft Power BI report that contains a table visual. The visual contains three DAX measures named Sales, Units, and Customers.

You need to apply logic-based DAX formatting to the Sales measure. The solution must minimize administrative effort and prevent the modification of the other two measures.

How should you apply the logic?

Select only one answer.

Use calculation group measure formatting.

This answer is incorrect.

Use conditional formatting.


Use dynamic measure formatting.

This answer is correct.

Use the fields parameter.

Dynamic measure formatting is the simplest and most effective way to add logic-based formatting to a single measure. Calculation groups can add logic-based formatting, but these are applied at the visual, page, or report level, and cannot be easily added to single measures.

Create dynamic format strings for measures in Power BI Desktop - Power BI | Microsoft Learn
## 🔹 Version 1 (তোমার original question)

### ❓ Question

> Apply logic-based DAX formatting to the **Sales measure**
> Minimize administrative effort
> Prevent modification of other measures

### ✅ Correct Answer

**Dynamic measure formatting**

### 🧠 Why

* Specific measure (Sales)
* Other measures safe রাখতে হবে
* Least effort

---

## 🔹 Version 2 (এখানে Calculation Group correct হবে)

### ❓ Question

> Apply the **same logic-based formatting to ALL measures**
> Formatting logic may be reused across visuals
> Centralized management is required

### ✅ Correct Answer

**Calculation group measure formatting**

### 🧠 Why

* ALL measures
* Reusable logic
* Central control

📌 **Keyword:** ALL / reusable / centralized

---

## 🔹 Version 3 (এখানে Conditional Formatting correct হবে)

### ❓ Question

> Apply logic-based formatting **only in a single table visual**
> No changes to the underlying DAX measures are allowed

### ✅ Correct Answer

**Conditional formatting**

### 🧠 Why

* Only visual-level
* Measure touch করা যাবে না
* One-time setup

📌 **Keyword:** single visual / no DAX change

---

## 🔹 Version 4 (এখানে Field Parameter correct হবে)

### ❓ Question

> Allow users to **switch between Sales, Units, and Customers**
> Formatting should change based on selected field

### ✅ Correct Answer

**Use the fields parameter**

### 🧠 Why

* User interaction
* Dynamic field switching

📌 **Keyword:** switch / select / toggle

---

## 🔥 ONE-GLANCE DECISION CHART (Exam Gold)

| Question says…          | Answer                 |
| ----------------------- | ---------------------- |
| One specific measure    | Dynamic formatting     |
| All measures / reusable | Calculation group      |
| Only one visual         | Conditional formatting |
| User switches fields    | Field parameter        |

---

## 🧠 Super Shortcut (Bangla Memory Hack)

> **Measure-এর নাম থাকলে → Dynamic**
> **ALL measure বললে → Calculation Group**
> **Visual বললে → Conditional**
> **User switch বললে → Field Parameter**

---

## 🔥 Mini Practice (Try yourself)

### Q:

> Apply logic-based formatting to Sales and Units only, without duplicating DAX logic.

👉 Answer কী হবে?
**Calculation Group** (partial reuse logic)

 
 

Question 2 of 50

You are developing a large semantic model.

You have a fact table that contains 500 million rows. Most analytic queries will target aggregated data, but some users must still be able to view data on a detailed level.

You plan to create a composite model and implement user-defined aggregations.

Which three storage modes should you use for each type of table? Each correct answer presents part of the solution.

Select all answers that apply.

Aggregated tables should use Dual mode.


Aggregated tables should use Import mode.

This answer is correct.

The detailed fact table should use DirectQuery mode.

This answer is correct.

The detailed fact table should use Import mode.

This answer is incorrect.

Dimension tables should use DirectQuery mode.

This answer is incorrect.

Dimension tables should use Dual mode.

This answer is correct.
When using ser-defined aggregations, the detailed fact table must be in DirectQuery mode. It is recommended to set the storage mode to Import for aggregated tables because of the performance, while dimension tables should be set to Dual mode to avoid the limitations of limited relationships

User-defined aggregations - Power BI | Microsoft Learn



# 🧠 PART-1: ORIGINAL QUESTION টা ভালো করে বুঝি

## ❓ Question (সহজ ভাষায়)

তুমি একটা **বড় semantic model** বানাচ্ছো।

* Fact table = **500 million rows** 😮 (খুব বড়)
* **Most queries** → aggregated data (SUM, COUNT, GROUP BY)
* **কিছু user** → detailed row-level data দেখতে চায়
* তুমি ব্যবহার করছ:

  * **Composite model**
  * **User-defined aggregations**

এখন প্রশ্ন:

> কোন type table-এ **কোন storage mode** ব্যবহার করবে?

---

## 🔑 এখানে 3টা গুরুত্বপূর্ণ clue আছে (এগুলো ধরতে পারলেই answer easy)

### 🔹 Clue 1: *500 million rows*

👉 এত বড় table **Import করলে problem** হবে
👉 Detailed data → **DirectQuery দরকার**

---

### 🔹 Clue 2: *Most queries will target aggregated data*

👉 Aggregated table:

* ছোট
* summary data
* fast performance দরকার

📌 Best choice → **Import mode**

---

### 🔹 Clue 3: *User-defined aggregations*

এটা খুব important 🔥

📌 Microsoft rule:

> **User-defined aggregation কাজ করতে হলে**
> 👉 **Detailed fact table MUST be DirectQuery**

এটা মুখস্থ রাখতে হবে 💯

---

## 🧩 এখন table-wise decision নেই

---

### 🟦 1️⃣ Aggregated Tables

👉 Role:

* SUM, COUNT, GROUP BY
* Most queries hit here

👉 Best storage:

* **Import mode** (fastest)

❌ Dual?

* দরকার নাই
* extra complexity

✅ **Correct answer**
✔️ Aggregated tables should use **Import mode**

---

### 🟥 2️⃣ Detailed Fact Table (500M rows)

👉 Role:

* Row-level detail
* Drill-through
* Rarely queried but must exist

👉 Rule (exam killer line):

> User-defined aggregations ⇒ **Detailed fact = DirectQuery**

❌ Import?

* 500M rows → memory issue
* aggregation routing কাজ করবে না

✅ **Correct answer**
✔️ The detailed fact table should use **DirectQuery mode**

---

### 🟩 3️⃣ Dimension Tables

👉 Role:

* Join/filter
* Used by both aggregated + detailed queries

👉 Problem:

* Import + DirectQuery mix করলে relationship limitation হয়

👉 Solution:

* **Dual mode**

📌 Dual মানে:

* Aggregated query → behaves like Import
* Detail query → behaves like DirectQuery

✅ **Correct answer**
✔️ Dimension tables should use **Dual mode**

---

## ✅ FINAL CORRECT ANSWERS (Original Question)

✔️ Aggregated tables → **Import**
✔️ Detailed fact table → **DirectQuery**
✔️ Dimension tables → **Dual**

---

# 🧠 PART-2: এখন question বদলাই → answer বদলাবে

এটাই তোমার main request 🔥

---

## 🔁 Version-1: Aggregation নাই

### ❓ Changed Question

> You are not using user-defined aggregations.
> All data should be cached for maximum performance.

### ✅ Correct Answers

* Fact table → **Import**
* Dimension tables → **Import**

📌 কারণ:

* Aggregation না থাকলে DirectQuery দরকার নাই

---

## 🔁 Version-2: Real-time reporting required

### ❓ Changed Question

> Data must always reflect real-time source values.

### ✅ Correct Answers

* Fact table → **DirectQuery**
* Dimension tables → **DirectQuery**

📌 কারণ:

* Import = cached data
* Real-time = DirectQuery

---

## 🔁 Version-3: Small dataset

### ❓ Changed Question

> The fact table contains only 5 million rows.

### ✅ Correct Answers

* Fact table → **Import**
* Dimension tables → **Import**

📌 কারণ:

* 5M rows manageable
* Simpler model

---

## 🔁 Version-4: Aggregations + but dimensions not reused

### ❓ Changed Question

> Dimension tables are not shared with detailed queries.

### ✅ Correct Answers

* Aggregated table → **Import**
* Detail fact → **DirectQuery**
* Dimension tables → **Import**

📌 Dual দরকার নাই এখানে

---

## 🧠 ONE-LOOK MEMORY TABLE (Exam GOLD)

| Question says…            | Choose                    |
| ------------------------- | ------------------------- |
| User-defined aggregations | Detail fact = DirectQuery |
| Most queries aggregated   | Aggregation = Import      |
| Mix Import + DirectQuery  | Dimension = Dual          |
| Real-time data            | DirectQuery               |
| Small dataset             | Import                    |

---

Question 5 of 50

You have a Microsoft Power BI report page that takes longer than expected to display all its visuals.

You need to identify which report element consumes most of the rendering time. The solution must minimize administrative effort and how long it takes to capture the rendering information of each element on the report page.

What should you use?

Select only one answer.

DAX Studio


Performance analyzer

This answer is correct.

SQL Server Profiler


Tabular Editor

Performance analyzer is a built-in feature in Power BI Desktop that captures the performance information of each element on the report page. DAX Studio can be used to analyze DAX queries, whereas Tabular Editor does not capture the rendering time at all.

Use Performance Analyzer to examine report element performance in Power BI Desktop - Power BI | Microsoft Learn

ঠিক আছে 👍
এই প্রশ্নটা **exam-এর খুব common trap**, তাই আমি ঠিক তোমার চাওয়া অনুযায়ী করবো:

👉 **প্রথমে প্রশ্নটা ভালো করে খুলে বুঝাবো**
👉 **তারপর question বদলালে কোন option correct হবে—সেটা দেখাবো**

সব **easy Bangla** 👇

---

# 🧠 PART-1: প্রশ্নটা ঠিকমতো বুঝি (Line-by-Line)

## ❓ Question (সহজ ভাষায়)

তোমার একটা **Power BI report page** আছে
➡️ Page টা **slow load হচ্ছে** (visual গুলো আসতে সময় লাগছে)

তুমি জানতে চাও:

> **কোন report element / visual সবচেয়ে বেশি সময় নিচ্ছে**

### Extra condition (সবচেয়ে গুরুত্বপূর্ণ clue 🔥)

> The solution must
>
> * **minimize administrative effort**
> * **minimize time to capture rendering info of each element**

মানে:

* extra tool install করা যাবে না
* query trace, long setup চলবে না
* **fast + easy solution**

---

## 🔑 এখন clue থেকে option eliminate করি

---

### ❌ DAX Studio কেন ভুল?

DAX Studio:

* DAX query analyze করে
* query-level performance দেখায়
* ❌ visual rendering time দেখায় না
* ❌ setup লাগে (external tool)

📌 তাই:

> “Rendering time of each report element” → ❌

---

### ❌ SQL Server Profiler কেন ভুল?

SQL Profiler:

* backend query trace করে
* heavy tool
* model-level / engine-level

📌 Problem:

* ❌ rendering time দেখায় না
* ❌ admin effort বেশি
* ❌ slow setup

---

### ❌ Tabular Editor কেন ভুল?

Tabular Editor:

* model edit করার tool
* calculation group, measures manage করে
* ❌ performance tracking নেই

---

### ✅ Performance Analyzer কেন ঠিক?

Performance Analyzer:

* **Built-in** Power BI Desktop feature
* **One click** → Start recording
* Visual-by-visual:

  * DAX query time
  * Visual display time
  * Total rendering time

📌 Exactly matches:
✔️ Identify slow visual
✔️ Minimum effort
✔️ Fast capture

---

## ✅ FINAL CORRECT ANSWER

✔️ **Performance Analyzer**

---

# 🧠 PART-2: Question change করলে answer কিভাবে বদলাবে

এখন তোমার আসল চাওয়া অংশ 👇

---

## 🔁 Version-1: DAX query optimize করতে হবে

### ❓ Changed Question

> You need to analyze and optimize the DAX queries executed by a slow visual.

### ✅ Correct Answer

**DAX Studio**

📌 কারণ:

* query plan
* server timings
* storage engine vs formula engine

---

## 🔁 Version-2: Data source-level issue

### ❓ Changed Question

> You need to trace queries sent from Power BI to SQL Server.

### ✅ Correct Answer

**SQL Server Profiler**

📌 কারণ:

* SQL query capture
* source-level diagnostics

---

## 🔁 Version-3: Model refactor করতে হবে

### ❓ Changed Question

> You need to manage measures, calculation groups, and metadata efficiently.

### ✅ Correct Answer

**Tabular Editor**

📌 কারণ:

* modeling tool
* not performance tracing

---

## 🔥 ONE-LOOK MEMORY TABLE (Exam Gold)

| Question says…         | Use                  |
| ---------------------- | -------------------- |
| Which visual is slow   | Performance Analyzer |
| DAX query optimization | DAX Studio           |
| Trace SQL queries      | SQL Profiler         |
| Edit model metadata    | Tabular Editor       |

---

## 🧠 Super Exam Shortcut (Bangla)

> **Visual slow? → Performance Analyzer**
> **Query slow? → DAX Studio**
> **Database slow? → SQL Profiler**
> **Model change? → Tabular Editor**

---

## ✨ One-line summary

> **Rendering time of report elements** জানতে চাইলে
> 👉 **Performance Analyzer ছাড়া অন্য কিছু ভাববে না**

---
 

