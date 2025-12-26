Perfect 👍
These are **FOUNDATION questions**. Once these are clear, **joins, pipelines, modeling, performance — everything clicks**.

I’ll explain in **simple exam language**, then give you the **Notebook vs Dataflow vs Pipeline decision chart** you asked for.

---

# 1️⃣ WHAT IS A FACT TABLE? (DP-600 CORE CONCEPT)

![Image](https://docs.precisely.com/docs/sftw/spectrum/22.1/en/webhelp/EnterpriseDataIntegrationGuide/Images/EDI_StarSchemaDbDiagram.png)

![Image](https://i.sstatic.net/aB9k9.jpg)

![Image](https://media.geeksforgeeks.org/wp-content/uploads/20211002145356/starskema.png)

## ❓ WHAT is a Fact Table?

A **fact table stores business EVENTS** and **MEASURES**.

👉 Think:

> **“Something happened, and we measured it.”**

---

## ❓ WHAT does a Fact Table contain?

### ✅ Always contains:

* **Numeric measures**

  * SalesAmount
  * Quantity
  * Cost
* **Foreign keys**

  * CustomerKey
  * ProductKey
  * DateKey

### ❌ Never contains:

* Descriptive text
* Attributes like Name, City, Category

---

## ❓ HOW does a Fact Table work?

* Each row = **one business event**
* It **connects to dimension tables**
* Used for **aggregation** (SUM, AVG, COUNT)

📌 Example:

```
FactSales
---------
SalesID
CustomerKey
ProductKey
DateKey
SalesAmount
Quantity
```

---

## ❓ WHEN do we query Fact Tables?

When we want:

* Total sales
* Revenue by year
* Quantity by product
* KPIs

---

## 🧠 EXAM RULE (MEMORIZE)

> **Fact tables answer: HOW MUCH / HOW MANY**

---

# 2️⃣ WHAT IS A DIMENSION TABLE?

![Image](https://www.techtarget.com/rms/onlineimages/simple_data_warehouse-f_mobile.png)

![Image](https://ars.els-cdn.com/content/image/3-s2.0-B9780124114616000101-f10-22-9780124114616.jpg)

![Image](https://help.hcl-software.com/hclinformix/1410/whse/ddi043.gif)

## ❓ WHAT is a Dimension Table?

A **dimension table stores descriptive information**.

👉 Think:

> **“Context for the numbers.”**

---

## ❓ WHAT does a Dimension Table contain?

### ✅ Always contains:

* Descriptive attributes

  * Name
  * Category
  * City
  * Region
* **Primary key**

  * CustomerKey
  * ProductKey

### ❌ Never contains:

* Measures like SalesAmount
* Aggregations

---

## ❓ HOW does a Dimension Table work?

* Filters the fact table
* Provides grouping context

📌 Example:

```
DimCustomer
-----------
CustomerKey
CustomerName
City
Country
CustomerType
```

---

## ❓ WHEN do we query Dimension Tables?

When we want:

* Sales **by customer**
* Revenue **by region**
* Orders **by date**

---


## 🧠 EXAM RULE (MEMORIZE)

> **Dimensions answer: WHO / WHAT / WHERE / WHEN**

---

# 3️⃣ HOW FACT & DIMENSION WORK TOGETHER (STAR SCHEMA)

![Image](https://bookshelf.erwin.com/bookshelf/public_html/12.0/Content/Resources/Images/2387.png)

![Image](https://cdn.sqlbi.com/wp-content/uploads/image1-11.png)

![Image](https://www.montecarlodata.com/wp-content/uploads/2024/08/star-schema-fact-dimension-table.webp)

### Relationship:

```
Dimension (1) ────< Fact (Many)
```

### Why?

* Efficient queries
* Better performance
* Easier DAX

---

## 🔥 VERY IMPORTANT DP-600 RULES

### ❌ Dimension → Dimension joins

🚫 Avoid

### ❌ Fact → Fact joins

🚫 Avoid

### ✅ Fact → Dimension joins

✔ Correct

---

## 🧠 GOLDEN EXAM RULE

> **Facts are filtered by Dimensions, not the other way around**

---

# 4️⃣ NOTEBOOK vs DATAFLOW vs PIPELINE (DECISION CHART)

This is **EXAM GOLD**. Save this.

---

## 📌 FABRIC INGESTION & TRANSFORMATION DECISION CHART

| Scenario                      | Use This                     | Why                    |
| ----------------------------- | ---------------------------- | ---------------------- |
| Small/medium data + transform | **Dataflow Gen2**            | Power Query, code-free |
| Big data + heavy transform    | **Notebook (Spark)**         | Scales for billions    |
| Big data + no transform       | **Pipeline (Copy activity)** | Cheapest & fastest     |
| Warehouse ingestion (code)    | **COPY (T-SQL)**             | High throughput        |
| External data, no copy        | **Shortcut**                 | Zero movement          |

---

## ❓ HOW TO DECIDE IN EXAM (FAST)

Ask **one question**:

### “Is the data BIG?”

* ❌ No → Dataflow Gen2
* ✅ Yes → Notebook or Pipeline

Then ask:

### “Do I need transformation?”

* ❌ No → Pipeline (Copy)
* ✅ Yes → Notebook

---

## 🧠 ONE-LINE MEMORY LOCK

> **Big + Transform = Notebook**
> **Big + No Transform = Pipeline**
> **Small + Transform = Dataflow**

---

# 5️⃣ WHY THIS MATTERS FOR JOINS (LINKING YOUR DOUBT)

Because:

* Fact tables are **LEFT table**
* Dimensions are **RIGHT table**

So in exams:

```
Fact LEFT JOIN Dimension
```

👉 To **keep all facts**, even if dimension is missing.

---

## ✅ FINAL SUMMARY (READ BEFORE EXAM)

* Fact = numbers + keys
* Dimension = description
* Fact answers **HOW MUCH**
* Dimension answers **WHO / WHAT / WHERE**
* Fact + Dimension → LEFT JOIN
* Big data + transform → Notebook
* Small data + transform → Dataflow
* Big data + no transform → Pipeline

---
 
 
