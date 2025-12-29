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
 
Practice Assessment for Exam DP-600: Implementing Analytics Solutions Using Microsoft Fabric
Question 6 of 50

You publish a very large Microsoft Power BI semantic model to a Power BI workspace.

The model refresh will take two hours.

In Power BI Desktop, you limit the data you work with by using parameters.

You need to update the definition of a measure.

What can you use to update the measure definition without having to refresh the model in the Power BI service?

Select only one answer.

ALM Toolkit

This answer is correct.

DAX Studio

This answer is incorrect.

Microsoft Excel


Power BI Desktop

The ALM Toolkit is a schema diff tool for Power BI models and can be used to perform the deployment of metadata only. Deploying from Power BI Desktop will overwrite the model’s data in the service and will require a refresh by the Power BI service to load the data. DAX Studio does not update metadata. You can connect to Power BI semantic models by using Excel in read-only mode.

Advanced incremental refresh and real-time data with the XMLA endpoint in Power BI - Power BI | Microsoft Learn

 
 ঠিক আছে 👍
এই প্রশ্নটাও আমি **একদম তোমার আগের pattern**-এ বুঝাবো:

👉 **প্রথমে original questionটা line-by-line খুলে বুঝাবো**
👉 **তারপর question একটু বদলালে কোন option correct হবে—সেটা দেখাবো**

সব **easy Bangla**, exam-focus 👇

---

# 🧠 PART-1: Original Question টা ভালো করে বুঝি

## ❓ Question (সহজ ভাষায়)

* তুমি একটা **খুব বড় Power BI semantic model** publish করছো
* **Refresh time = 2 hours** ⏳ (খুব slow)
* Desktop-এ তুমি **parameter দিয়ে ছোট data** নিয়ে কাজ করছো
* এখন তুমি শুধু **একটা measure-এর definition update** করতে চাও

### সবচেয়ে গুরুত্বপূর্ণ condition 🔥

> **Without having to refresh the model in the Power BI service**

মানে:

* ❌ Full model overwrite করা যাবে না
* ❌ 2 ঘণ্টার refresh trigger করা যাবে না
* ✅ শুধু metadata (measure definition) change করতে হবে

---

## 🔑 Exam clue গুলো ধরো

### 🔹 Clue 1: *Very large model + 2 hour refresh*

👉 Data touch করলে বিপদ
👉 **Metadata-only update দরকার**

---

### 🔹 Clue 2: *Update the definition of a measure*

👉 Measure = **model metadata**
👉 Data reload দরকার নেই

---

### 🔹 Clue 3: *Without refresh in service*

👉 Desktop publish = ❌
👉 Metadata deployment tool = ✅

---

## 🧩 এখন option গুলো এক এক করে দেখি

---

### ❌ DAX Studio কেন ভুল?

DAX Studio:

* Query run করে
* Performance analyze করে
* ❌ Measure CREATE / UPDATE করতে পারে না
* ❌ Metadata deploy করে না

📌 তাই:

> “update measure definition” → ❌

---

### ❌ Power BI Desktop কেন ভুল?

Power BI Desktop থেকে publish করলে:

* Entire model overwrite হয়
* Service আবার data load করে
* ❌ 2 ঘণ্টার refresh trigger হবে

📌 Question explicitly বলছে:

> without refresh ❌

---

### ❌ Microsoft Excel কেন ভুল?

Excel:

* Power BI semantic model-এ **read-only connection**
* Measure edit করা যায় না

---

### ✅ ALM Toolkit কেন ঠিক?

ALM Toolkit:

* **Schema diff & deployment tool**
* Metadata only deploy করে
* Data touch করে না
* Refresh trigger করে না

📌 Exactly matches:
✔️ Measure definition update
✔️ No data reload
✔️ No service refresh

---

## ✅ FINAL CORRECT ANSWER

✔️ **ALM Toolkit**

---

# 🧠 PART-2: Question বদলালে answer কিভাবে বদলাবে

এখন আসল শেখার জায়গা 👇

---

## 🔁 Version-1: Model ছোট, refresh fast

### ❓ Changed Question

> The model is small and refresh takes only a few minutes.

### ✅ Correct Answer

**Power BI Desktop**

📌 কারণ:

* Overwrite acceptable
* Simpler workflow

---

## 🔁 Version-2: Measure performance analyze করতে হবে

### ❓ Changed Question

> You need to analyze and optimize the DAX logic of a measure.

### ✅ Correct Answer

**DAX Studio**

📌 কারণ:

* Server timings
* Query plan analysis

---

## 🔁 Version-3: User needs to view model data

### ❓ Changed Question

> Users need to analyze the semantic model using a familiar tool.

### ✅ Correct Answer

**Microsoft Excel**

📌 কারণ:

* Live connection
* PivotTable analysis

---

## 🔁 Version-4: Multiple environments deploy

### ❓ Changed Question

> You need to deploy measure changes from DEV to PROD without refreshing data.

### ✅ Correct Answer

**ALM Toolkit**

📌 কারণ:

* Metadata-only deployment
* Environment compare

---

## 🔥 ONE-LOOK EXAM CHEAT TABLE

| Question says…       | Use              |
| -------------------- | ---------------- |
| Update metadata only | ALM Toolkit      |
| Analyze DAX          | DAX Studio       |
| Edit model + publish | Power BI Desktop |
| Read-only analysis   | Excel            |

---

## 🧠 Super Shortcut (Bangla)

> **Refresh avoid করতে চাইলে → ALM Toolkit**
> **Query optimize → DAX Studio**
> **Small model edit → Desktop**
> **Just analyze data → Excel**

---

## ✨ One-line summary

> **বড় model + refresh slow + measure update**
> 👉 **ALM Toolkit ছাড়া কিছু ভাববে না**

---

Question 7 of 50

You have a Microsoft Power BI semantic model assigned to you for ownership and maintenance.

You need to perform an audit on the model to identify and resolve potential performance or design issues.

Which Tabular Editor tool should you use?

Select only one answer.

Best Practices Analyzer

This answer is correct.

Perspective Editor

This answer is incorrect.

TOM Explorer


Vertipaq Analyzer

Only Best Practices Analyzer lets you specify a ruleset to review the model and multiple options for quick fixes by using C# scripts.

External tools in Power BI Desktop - Power BI | Microsoft Learn

Best Practice Analyzer | Tabular Editor Documentation

ঠিক আছে 👍
এই প্রশ্নটাও আমি **একই স্টাইলে** বুঝাবো:

👉 **প্রথমে প্রশ্নটা ভালো করে খুলে বুঝাবো**
👉 **তারপর question বদলালে কোন option correct হবে—সেটা দেখাবো**

সব **সহজ Bangla**, exam-focused 👇

---

# 🧠 PART-1: Original Question টা ভালো করে বুঝি

## ❓ Question (সহজ ভাষায়)

* তোমার কাছে একটা **Power BI semantic model** আছে
* তুমি এখন এর **owner & maintainer**
* তুমি চাও:

  * model-এর **performance issue**
  * **design issue**
  * ভুল relationship, bad practice, heavy measure ইত্যাদি **identify + fix** করতে

অর্থাৎ 👉
🕵️‍♂️ **Model audit করতে হবে**

---

## 🔑 এখানে সবচেয়ে গুরুত্বপূর্ণ keyword

### 👉 **“audit the model to identify and resolve issues”**

Audit মানে:

* নিয়ম অনুযায়ী check করা
* কোথায় problem আছে বলা
* fix করার suggestion দেওয়া

---

## 🧩 এখন option গুলো এক এক করে দেখি

---

### ✅ Best Practices Analyzer — কেন ঠিক

Best Practices Analyzer (BPA):

* Model-এর উপর **ruleset চালায়**
* Performance + design issue detect করে
* Example:

  * Unused columns
  * Missing relationships
  * Bad cardinality
  * Heavy calculated columns
* **Quick Fix** দেয় (C# script দিয়ে)

📌 এক কথায়:

> **Full model audit tool**

✅ তাই **Correct Answer**

---

### ❌ Perspective Editor — কেন ভুল

Perspective Editor:

* User-এর জন্য model-এর **view limit** করতে ব্যবহার হয়
* কোন table / measure user দেখবে সেটাই control করে

📌 Audit করে না
📌 Performance check করে না

❌ Wrong

---

### ❌ TOM Explorer — কেন ভুল

TOM Explorer:

* Model metadata দেখায় (tree view)
* Table, column, measure structure explore করা যায়

📌 Problem:

* ❌ Issue detect করে না
* ❌ Suggestion দেয় না
* ❌ Audit tool না

---

### ❌ VertiPaq Analyzer — কেন ভুল

VertiPaq Analyzer:

* Memory usage analyze করে
* Column size, dictionary size দেখায়

📌 Useful, কিন্তু:

* ❌ Full audit না
* ❌ Design + best practice check করে না

---

## ✅ FINAL CORRECT ANSWER

✔️ **Best Practices Analyzer**

---

# 🧠 PART-2: Question বদলালে answer কিভাবে বদলাবে

এখন আসল শেখার অংশ 👇

---

## 🔁 Version-1: User-specific model view দরকার

### ❓ Changed Question

> You need to limit which tables and measures users can see.

### ✅ Correct Answer

**Perspective Editor**

---

## 🔁 Version-2: Model structure explore করতে হবে

### ❓ Changed Question

> You need to explore tables, measures, and relationships in a hierarchical view.

### ✅ Correct Answer

**TOM Explorer**

---

## 🔁 Version-3: Memory optimization দরকার

### ❓ Changed Question

> You need to analyze column memory usage and compression.

### ✅ Correct Answer

**VertiPaq Analyzer**

---

## 🔥 ONE-LOOK EXAM CHEAT TABLE

| Question says…     | Use                         |
| ------------------ | --------------------------- |
| Audit model issues | **Best Practices Analyzer** |
| Limit user view    | Perspective Editor          |
| Explore metadata   | TOM Explorer                |
| Analyze memory     | VertiPaq Analyzer           |

---

## 🧠 Super Shortcut (Bangla)

> **Audit / Issue / Best Practice → BPA**
> **User view control → Perspective**
> **Structure দেখতে → TOM Explorer**
> **Memory size → VertiPaq**

---

## ✨ এক লাইনে summary

> **Model audit করতে হলে**
> 👉 **Best Practices Analyzer ছাড়া কিছু ভাববে না**

---

Question 11 of 50

You are managing a set of Dataflow Gen2 queries that are currently ingesting tables into a Fabric lakehouse.

You need to ensure that the tables are optimized for Direct Lake connections that will be used by connected semantic models.

What should you do?

Select only one answer.

Apply an incremental refresh policy to the semantic model refreshes.

This answer is incorrect.

Run the VACUUM command.


Use OPTIMIZE to apply V-Order.

This answer is correct.

Use shortcuts to the lakehouse tables from the semantic models.

Each table in a lakehouse has a setting that must be turned on to optimize and apply the V-Order, which will greatly increase the Direct Lake speeds when connecting to these tables.

Delta Lake table optimization and V-Order - Microsoft Fabric | Microsoft Learn

ঠিক আছে 👍
এই প্রশ্নটাও আমি **একই কাঠামোতে** বুঝাবো, যাতে তুমি **কখন কোন option ঠিক হবে** সেটা instinct-এর মতো ধরতে পারো।

---

# 🧠 PART-1: Original Question টা ভালো করে বুঝি

## ❓ Question (সহজ Bangla)

* তুমি **Dataflow Gen2 queries** manage করছো
* এগুলো data ingest করছে **Fabric lakehouse**-এ
* এই lakehouse table গুলোতে
  👉 **Direct Lake connection** দিয়ে **semantic model connect হবে**

👉 তোমার কাজ:

> **Direct Lake এর জন্য table optimize করা**

---

## 🔑 এখানে 3টা খুব গুরুত্বপূর্ণ keyword আছে (এগুলো ধরলেই answer clear)

### 🔹 Clue 1: *Fabric lakehouse*

মানে:

* Delta Lake table
* Spark / SQL / Direct Lake involved

---

### 🔹 Clue 2: *Direct Lake connections*

এটা সবচেয়ে বড় clue 🔥

📌 Direct Lake performance depends on:

* File layout
* Column ordering
* Storage optimization

---

### 🔹 Clue 3: *Ensure tables are optimized*

মানে:

* refresh policy না
* shortcut না
* **physical table optimization দরকার**

---

## 🧩 এখন option গুলো এক এক করে দেখি

---

### ❌ Incremental refresh policy — কেন ভুল?

Incremental refresh:

* **Semantic model refresh** optimize করে
* Import / DirectQuery scenario

📌 Problem:

* ❌ Lakehouse table optimize করে না
* ❌ Direct Lake performance বাড়ায় না

👉 তাই **wrong**

---

### ❌ VACUUM command — কেন ভুল?

VACUUM:

* Old/unused files delete করে
* Storage cleanup

📌 Problem:

* ❌ Query performance improve করে না
* ❌ V-Order apply করে না

👉 Maintenance tool, optimization না

---

### ❌ Shortcuts — কেন ভুল?

Shortcuts:

* Data copy না করে reference করে
* Architecture simplify করে

📌 Problem:

* ❌ Table optimize করে না
* ❌ Direct Lake speed বাড়ায় না

---

### ✅ OPTIMIZE with V-Order — কেন ঠিক?

OPTIMIZE + V-Order:

* Delta Lake feature
* Column-based file layout
* Scan efficiency বাড়ায়

📌 Microsoft Fabric rule:

> **Direct Lake performance = V-Order ON**

এটা করলে:

* Semantic model Direct Lake mode-এ fast query চালাতে পারে
* Storage engine efficient হয়

👉 Exact match with question

---

## ✅ FINAL CORRECT ANSWER

✔️ **Use OPTIMIZE to apply V-Order**

---

# 🧠 PART-2: Question বদলালে answer কিভাবে বদলাবে

এখন আসল শেখার জায়গা 👇

---

## 🔁 Version-1: Import semantic model slow

### ❓ Changed Question

> The semantic model uses Import mode and refresh time is very long.

### ✅ Correct Answer

**Apply incremental refresh policy**

📌 কারণ:

* Import data
* Partition-based refresh

---

## 🔁 Version-2: Storage cost বেশি

### ❓ Changed Question

> Lakehouse storage contains many obsolete files.

### ✅ Correct Answer

**Run VACUUM**

📌 কারণ:

* Old Delta files cleanup

---

## 🔁 Version-3: Data already exists in another lake

### ❓ Changed Question

> You want to avoid copying data into the lakehouse.

### ✅ Correct Answer

**Use shortcuts**

📌 কারণ:

* Reference without duplication

---

## 🔥 ONE-LOOK EXAM CHEAT TABLE

| Question says…          | Answer                 |
| ----------------------- | ---------------------- |
| Direct Lake performance | **OPTIMIZE + V-Order** |
| Import refresh slow     | Incremental refresh    |
| Old files cleanup       | VACUUM                 |
| Avoid data copy         | Shortcuts              |

---

## 🧠 Super Shortcut (Bangla)

> **Direct Lake = V-Order**
> **Import refresh = Incremental**
> **Cleanup = VACUUM**
> **No copy = Shortcut**

---

## ✨ এক লাইনে summary

> **Fabric lakehouse + Direct Lake fast চাইলে**
> 👉 **OPTIMIZE করে V-Order apply করতেই হবে**

---

 You have a Fabric tenant that contains a workspace named Workspace1. Workspace1 contains a lakehouse named Lakehouse1.

You open a notebook in Lakehouse1 and attach it to a Spark session.

You plan to start a new notebook in Lakehouse1 and attach it to the same Spark session. However, you notice that the New high concurrency session option is unavailable, and the only available option is Standard session.

You need to ensure that the high concurrency mode for notebooks is enabled.

Where can you check the high concurrency mode?

Select only one answer.

Fabric tenant settings


Lakehouse settings


Notebook properties from the Edit menu

This answer is incorrect.

Workspace settings

This answer is correct.
The high concurrency mode for Fabric notebooks is set at the workspace level. It is on by default; however, it can be turned off in scenarios where notebooks require dedicated compute resources.

Configure high concurrency mode for notebooks - Microsoft Fabric | Microsoft Learn
ঠিক আছে 👍
এই প্রশ্নটাও আমি **একই exam-learning স্টাইলে** বুঝাবো:

👉 **প্রথমে original questionটা ধাপে ধাপে বুঝাবো**
👉 **তারপর question একটু বদলালে কোন option correct হবে—সেটা দেখাবো**

সব **easy Bangla**, DP-600 focused 👇

---

# 🧠 PART-1: Original Question টা ভালো করে বুঝি

## ❓ Question (সহজ ভাষায়)

* তোমার কাছে একটি **Fabric tenant**
* সেখানে একটি **workspace (Workspace1)**
* Workspace1 এর ভিতরে একটি **Lakehouse (Lakehouse1)**
* তুমি:

  * একটি notebook খুলেছো
  * সেটাকে **Spark session**-এ attach করেছো
* এখন তুমি:

  * আরেকটা notebook খুলতে চাও
  * **same Spark session**-এ attach করতে চাও

কিন্তু সমস্যা 😟
👉 **New high concurrency session option নাই**
👉 শুধু **Standard session** দেখাচ্ছে

---

## 🎯 তোমার লক্ষ্য

> **High concurrency mode ENABLE আছে কিনা check করা / enable করা**

---

## 🔑 সবচেয়ে গুরুত্বপূর্ণ clue 🔥

### 👉 “High concurrency session”

এটা বুঝালেই ৫০% answer clear হয়ে যায়

📌 High concurrency মানে:

* Multiple notebooks
* Same Spark compute
* Shared session

এটা **tenant বা lakehouse-level feature না**
👉 এটা **workspace-level setting**

---

## 🧩 এখন option গুলো এক এক করে দেখি

---

### ❌ Fabric tenant settings — কেন ভুল?

Fabric tenant settings:

* Global level (entire organization)
* Security, feature enable/disable

📌 Problem:

* ❌ Notebook concurrency এখানে control হয় না
* ❌ Workspace-specific behavior না

---

### ❌ Lakehouse settings — কেন ভুল?

Lakehouse settings:

* Table, schema, shortcuts
* Storage-related config

📌 Problem:

* ❌ Spark session behavior এখানে define হয় না

---

### ❌ Notebook properties (Edit menu) — কেন ভুল?

Notebook properties:

* Notebook-specific metadata
* Language, parameters

📌 Problem:

* ❌ High concurrency notebook-level feature না
* ❌ Session sharing control করে না

---

### ✅ Workspace settings — কেন ঠিক?

Workspace settings:

* **Notebook compute behavior**
* **High concurrency mode ON/OFF**
* Shared vs dedicated Spark resources

📌 Microsoft rule:

> **High concurrency mode for Fabric notebooks is configured at the workspace level**

👉 Default ON থাকে, কিন্তু:

* কেউ চাইলে OFF করতে পারে
* OFF থাকলে → only Standard session দেখাবে

---

## ✅ FINAL CORRECT ANSWER

✔️ **Workspace settings**

---

# 🧠 PART-2: Question বদলালে answer কিভাবে বদলাবে

এখন তোমার শেখার আসল অংশ 👇

---

## 🔁 Version-1: Organization-wide feature missing

### ❓ Changed Question

> Notebooks are unavailable for all workspaces in the tenant.

### ✅ Correct Answer

**Fabric tenant settings**

📌 কারণ:

* Tenant-level feature disabled হতে পারে

---

## 🔁 Version-2: Notebook-specific behavior change

### ❓ Changed Question

> You want to configure parameters or language for a notebook.

### ✅ Correct Answer

**Notebook properties**

---

## 🔁 Version-3: Table optimization issue

### ❓ Changed Question

> You want to configure table storage or shortcuts.

### ✅ Correct Answer

**Lakehouse settings**

---

## 🔥 ONE-LOOK EXAM CHEAT TABLE

| Question says…       | Check here             |
| -------------------- | ---------------------- |
| Notebook concurrency | **Workspace settings** |
| Tenant-wide features | Fabric tenant settings |
| Notebook metadata    | Notebook properties    |
| Lakehouse storage    | Lakehouse settings     |

---

## 🧠 Super Shortcut (Bangla)

> **Multiple notebook + same Spark = Workspace**
> **Whole org feature = Tenant**
> **Notebook only = Notebook properties**
> **Data/table = Lakehouse**

---

 You have a Fabric warehouse named Warehouse1.

You discover a SQL query that performs poorly, and you notice that table statistics are out of date.

You need to manually update the statistics to improve query performance for the table.

Which column statistics should you update?

Select only one answer.

columns of the VARCHAR and NVARCHAR data type

This answer is incorrect.

columns used in GROUP BY clauses

This answer is correct.

columns with high cardinality


primary key columns

When manually creating/updating statistics for optimizing query performance, you should focus on columns used in JOIN, ORDER BY, and GROUP BY clauses.

Statistics - Microsoft Fabric | Microsoft Learn
ঠিক আছে 👍
এই প্রশ্নটাও আমি **exact তোমার চাওয়া pattern**-এ করবো:

👉 **প্রথমে original questionটা পরিষ্কার করে বুঝাবো**
👉 **তারপর কেন এই option correct, আর question বদলালে কখন অন্য option correct হবে—সেটা দেখাবো**

সব **সহজ Bangla**, DP-600 exam focus 👇

---

# 🧠 PART-1: Original Question টা ভালো করে বুঝি

## ❓ Question (সহজ Bangla)

* তোমার একটি **Fabric Warehouse (Warehouse1)** আছে
* একটি **SQL query খুব slow**
* তুমি দেখছো 👉 **table statistics out of date**
* তুমি চাও:

  > **Manual statistics update করে query performance improve করতে**

প্রশ্ন:

> **কোন column-এর statistics update করা উচিত?**

---

## 🔑 এখানে সবচেয়ে গুরুত্বপূর্ণ clue 🔥

### 👉 **“Improve query performance”**

Query performance মূলত নির্ভর করে:

* JOIN
* GROUP BY
* ORDER BY
* WHERE clause

📌 Optimizer এই জায়গাগুলোতে **statistics heavily use করে**

---

## 🧩 এখন option গুলো এক এক করে দেখি

---

### ❌ VARCHAR / NVARCHAR columns — কেন ভুল?

* Text column
* সাধারণত:

  * descriptive data
  * rarely used for grouping

📌 Statistics update করলে:

* ❌ query plan খুব একটা improve হয় না

👉 তাই **wrong**

---

### ✅ Columns used in GROUP BY clauses — কেন ঠিক?

GROUP BY মানে:

* Aggregation
* Data distribution বুঝা দরকার

📌 Statistics থাকলে:

* Optimizer জানে:

  * কতগুলো group হবে
  * data skew আছে কিনা
* Better execution plan বানাতে পারে

👉 তাই **Correct Answer**

---

### ❌ Columns with high cardinality — কেন ভুল?

High cardinality মানে:

* অনেক unique value

📌 Problem:

* Cardinality একা performance rule না
* যদি query-তে use না হয় → useless

👉 Question বলছে **which column statistics should you update**,
**not which column has many values**

---

### ❌ Primary key columns — কেন ভুল?

Primary key:

* Already unique
* Often indexed

📌 Optimizer already জানে:

* uniqueness
* distribution

👉 Extra stats update করে বড় gain হয় না

---

## ✅ FINAL CORRECT ANSWER

✔️ **columns used in GROUP BY clauses**

---

# 🧠 PART-2: Question বদলালে answer কিভাবে বদলাবে

এখন আসল শেখার জায়গা 👇

---

## 🔁 Version-1: JOIN slow হচ্ছে

### ❓ Changed Question

> Queries perform poorly due to slow JOIN operations.

### ✅ Correct Answer

**columns used in JOIN conditions**

📌 কারণ:

* Join cardinality estimation critical

---

## 🔁 Version-2: ORDER BY slow

### ❓ Changed Question

> Queries with ORDER BY clauses are slow.

### ✅ Correct Answer

**columns used in ORDER BY clauses**

---

## 🔁 Version-3: Filter slow (WHERE)

### ❓ Changed Question

> Queries are slow due to filtering conditions.

### ✅ Correct Answer

**columns used in WHERE clauses**

---

## 🔁 Version-4: Text search heavy

### ❓ Changed Question

> Queries filter large text columns.

### ✅ Correct Answer

**VARCHAR / NVARCHAR columns**

📌 (এই scenario-তে তখন correct হতে পারে)

---

## 🔥 ONE-LOOK EXAM CHEAT TABLE

| Query pattern | Update stats on      |
| ------------- | -------------------- |
| GROUP BY      | **GROUP BY columns** |
| JOIN          | JOIN columns         |
| ORDER BY      | ORDER BY columns     |
| WHERE         | Filter columns       |
| Text search   | VARCHAR / NVARCHAR   |

---

## 🧠 Super Shortcut (Bangla)

> **Optimizer যেখানেই decision নেয়**
> 👉 **সেই column-এর statistics update করো**

---

## ✨ এক লাইনে summary

> **Manual statistics update করতে হলে**
> 👉 **GROUP BY / JOIN / ORDER BY column-ই প্রথম priority**

---
 You have a Fabric workspace that contains a lakehouse named Lakehouse1. Lakehouse1 contains a table named FactSales that is ingested by using a Dataflow Gen2 query.

There are several applied steps and transformations applied to FactSales during the ingestion process.

You notice that due to the number of Power Query transformations, there are occasional timeout issues for the dataflow.

You need to recommend a solution to prevent the timeout issues.

You have already confirmed that the query cannot be further optimized and that changing the refresh time does not improve the timeout issues.

Which additional action should you recommend?

Select only one answer.

Change the FactSales destination to a newly created Fabric warehouse.


Create a new group for the FactSales query.


Create a second dataflow that ingests the FactSales table with no additional transformations, and then connect the original dataflow to transform the FactSales data by using this second dataflow.

This answer is correct.

Create a shortcut to FactSales, connect the dataflow to the shortcut, and then apply the transformations.

It is considered best practice to create a staging first dataflow that ingests the raw data first, and then a second dataflow to transform the data, commonly applied when there are performance or timeout issues for a query.

Best practices for designing and developing complex dataflows - Power Query | Microsoft Learn

ঠিক আছে 👍
এই প্রশ্নটাও আমি **একদম আগেরগুলোর মতো** করবো:

👉 **প্রথমে প্রশ্নটা ধাপে ধাপে বুঝাবো**
👉 **তারপর কেন এই option correct, আর question বদলালে কখন অন্য option correct হবে—সেটা দেখাবো**

সব **easy Bangla**, DP-600 exam focus 👇

---

# 🧠 PART-1: Original Question টা ভালো করে বুঝি

## ❓ Question (সহজ Bangla)

* তোমার একটি **Fabric workspace**
* এর মধ্যে একটি **Lakehouse (Lakehouse1)**
* একটি table আছে → **FactSales**
* FactSales ingest হচ্ছে **Dataflow Gen2** দিয়ে
* Ingestion সময়:

  * অনেক **Power Query applied steps**
  * অনেক **transformations**
* Problem 😟
  👉 মাঝে মাঝে **dataflow timeout**

তুমি ইতিমধ্যে:

* Query আর optimize করা যায় না
* Refresh time change করেও লাভ হয়নি

👉 এখন প্রশ্ন:

> **Timeout prevent করার জন্য আর কী করা উচিত?**

---

## 🔑 সবচেয়ে গুরুত্বপূর্ণ clue 🔥

### 👉 **“many Power Query transformations + timeout”**

Power BI / Fabric best practice বলে:

> **Heavy transformation একটাই dataflow-তে রাখবে না**

---

## 🧩 Option গুলো এক এক করে দেখি

---

### ❌ Change destination to Fabric Warehouse — কেন ভুল?

Warehouse:

* Storage type change
* SQL endpoint সুবিধা

📌 Problem:

* ❌ Power Query transformation একই থাকবে
* ❌ Timeout issue solve করে না

---

### ❌ Create a new group — কেন ভুল?

Group:

* Just organize queries
* Logical separation only

📌 Problem:

* ❌ Performance change হয় না
* ❌ Timeout solve করে না

---

### ❌ Create shortcut and transform — কেন ভুল?

Shortcut:

* Data reference, no copy
* Architecture convenience

📌 Problem:

* ❌ Transformation load কমায় না
* ❌ Same dataflow execution time

---

### ✅ Create staging + transform dataflows — কেন ঠিক?

এই option বলছে:

1️⃣ **Dataflow-1 (Staging)**

* Raw FactSales ingest
* ❌ No transformations

2️⃣ **Dataflow-2 (Transform)**

* Dataflow-1 থেকে data নেয়
* Transform করে final FactSales বানায়

📌 Benefits:

* Load ভাগ হয়ে যায়
* Timeout কমে
* Retry easier
* Best practice ✔️

👉 Microsoft officially recommend করে

---

## ✅ FINAL CORRECT ANSWER

✔️ **Create a second dataflow that ingests the FactSales table with no additional transformations, and then connect the original dataflow to transform the FactSales data by using this second dataflow.**

---

# 🧠 PART-2: Question বদলালে answer কিভাবে বদলাবে

এখন তোমার শেখার আসল অংশ 👇

---

## 🔁 Version-1: Raw + curated layer design

### ❓ Changed Question

> You want to implement a bronze–silver data architecture.

### ✅ Correct Answer

**Create staging dataflow first, then transformation dataflow**

---

## 🔁 Version-2: Just organize queries

### ❓ Changed Question

> You want to logically organize queries in a dataflow.

### ✅ Correct Answer

**Create a new group**

---

## 🔁 Version-3: Avoid data duplication

### ❓ Changed Question

> You want to reference the same table without copying data.

### ✅ Correct Answer

**Create a shortcut**

---

## 🔁 Version-4: SQL analytics required

### ❓ Changed Question

> You need T-SQL based analytics.

### ✅ Correct Answer

**Change destination to Fabric warehouse**

---

## 🔥 ONE-LOOK EXAM CHEAT TABLE

| Problem               | Best Solution                     |
| --------------------- | --------------------------------- |
| Heavy transformations | **Staging + transform dataflows** |
| Timeout issues        | **Split dataflows**               |
| Just organize         | Group                             |
| No data copy          | Shortcut                          |
| SQL analytics         | Warehouse                         |

---

## 🧠 Super Shortcut (Bangla)

> **Power Query heavy হলে**
> 👉 **একটা dataflow-তে সব রাখবে না**
> 👉 **Staging → Transform split করো**

---

## ✨ এক লাইনে summary

> **Dataflow timeout + many transformations**
> 👉 **Always split into staging + transformation dataflows**

---

ঠিক আছে 👍
এই প্রশ্নটাও আমি **আগেরগুলোর মতো একই শেখার ফরম্যাটে** বুঝাবো:

👉 **প্রথমে original questionটা পরিষ্কার করে বুঝাবো**
👉 **তারপর কেন এই option correct, আর question বদলালে কখন অন্য option correct হবে—সেটা দেখাবো**

সব **easy Bangla**, DP-600 exam focus 👇

---

# 🧠 PART-1: Original Question টা ভালো করে বুঝি

## ❓ Question (সহজ Bangla)

* তোমার একটি **Fabric workspace**
* Workspace-এর ভিতরে একটি **Lakehouse (Lakehouse1)**
* একজন user (**User1**) চায়:
  👉 **Lakehouse Explorer ব্যবহার করে data READ করতে**

👉 তোমার কাজ:

> **User1-কে কোন workspace role দিবে**,
> যাতে **least privilege principle** follow হয়

---

## 🔑 সবচেয়ে গুরুত্বপূর্ণ keyword 🔥

### 👉 **“Lakehouse explorer to read data”**

এখানে বুঝতে হবে:

* Lakehouse Explorer = **Lakehouse data access**
* Viewer role = শুধু report / item view
* **Viewer lakehouse data পড়তে পারে না**

📌 Microsoft Fabric rule:

> **Lakehouse Explorer দিয়ে data পড়তে হলে**
> 👉 User-কে **Admin / Member / Contributor** হতে হবে

---

## 🧩 এখন option গুলো এক এক করে দেখি

---

### ❌ Admin — কেন ভুল?

Admin:

* Full control
* Workspace delete
* Role manage

📌 Problem:

* ❌ Over-privileged
* ❌ Least privilege violate করে

---

### ❌ Member — কেন ভুল?

Member:

* Create, edit items
* Share content

📌 Problem:

* ❌ Contributor থেকেও বেশি permission
* ❌ User শুধু read চায়

---

### ✅ Contributor — কেন ঠিক?

Contributor:

* Lakehouse Explorer দিয়ে data read করতে পারে
* Item edit করতে পারে
* Admin / Member থেকে **কম permission**

📌 Exactly matches:
✔️ Lakehouse data read
✔️ Least privilege

👉 **Best possible minimal role**

---

### ❌ Viewer — কেন ভুল?

Viewer:

* Report / dashboard দেখতে পারে
* ❌ Lakehouse Explorer access নাই
* ❌ Data read permission নাই

👉 তাই **wrong**

---

## ✅ FINAL CORRECT ANSWER

✔️ **Contributor**

---

# 🧠 PART-2: Question বদলালে answer কিভাবে বদলাবে

এখন আসল শেখার অংশ 👇

---

## 🔁 Version-1: User শুধু report দেখবে

### ❓ Changed Question

> User only needs to view reports and dashboards.

### ✅ Correct Answer

**Viewer**

📌 কারণ:

* Lakehouse access দরকার নাই

---

## 🔁 Version-2: User needs full control

### ❓ Changed Question

> User must manage workspace security and settings.

### ✅ Correct Answer

**Admin**

---

## 🔁 Version-3: User creates and shares items

### ❓ Changed Question

> User needs to create, edit, and share Fabric items.

### ✅ Correct Answer

**Member**

---

## 🔥 ONE-LOOK EXAM CHEAT TABLE

| User needs           | Role            |
| -------------------- | --------------- |
| View reports only    | Viewer          |
| Read lakehouse data  | **Contributor** |
| Create & share items | Member          |
| Full control         | Admin           |

---

## 🧠 Super Shortcut (Bangla)

> **Lakehouse Explorer → Viewer চলবে না**
> **Least privilege → Contributor**
> **Everything control → Admin**

---

## ✨ এক লাইনে summary

> **Lakehouse Explorer দিয়ে data পড়তে চাইলে**
> 👉 **Minimum role = Contributor**

---
 




