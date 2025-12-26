
# 🔐 GOVERNANCE IN MICROSOFT FABRIC (DP-600 EXAM GUIDE)

![Image](https://data-marc.com/wp-content/uploads/2023/06/fabriccontrols_featuredimage.png?w=1024)

![Image](https://miro.medium.com/v2/resize%3Afit%3A2000/1%2AIiTz1p8Q96nszPK8nJd-JA.png)

![Image](https://learn.microsoft.com/en-us/fabric/governance/media/onelake-catalog-govern/onelake-catalog-govern-tab-view-more-report-admins.png)

---

## 1️⃣ WHAT IS GOVERNANCE? (EXAM DEFINITION)

### ❓ What does *governance* mean?

> **Ensuring data is secure, discoverable, compliant, and trusted across the organization.**

Governance answers:

* Who can access data?
* What data is sensitive?
* Can users trust this data?
* Can auditors track usage?

---

## 2️⃣ GOVERNANCE vs SECURITY (VERY IMPORTANT)

| Topic          | Purpose                                   |
| -------------- | ----------------------------------------- |
| **Security**   | Prevent unauthorized access               |
| **Governance** | Control, classify, audit, and manage data |

🧠 **Exam Rule**

> Security = access
> Governance = control + compliance + visibility

---

## 3️⃣ CORE GOVERNANCE COMPONENTS IN FABRIC

### 🔹 1. Sensitivity Labels (MOST TESTED)

### ❓ What are Sensitivity Labels?

They **classify data** based on sensitivity:

* Public
* Internal
* Confidential
* Highly Confidential

---

### ❓ WHEN do you use Sensitivity Labels?

Use when:

* Question says **“protect sensitive data”**
* Organization needs **compliance**
* Data must be restricted across Fabric

📌 Applies to:

* Lakehouse
* Warehouse
* Semantic models
* Reports

---

### ❓ WHAT do Sensitivity Labels do?

✅ Restrict access
✅ Apply policies
✅ Track data usage
✅ Integrate with Purview

---

### 🧠 EXAM RULE

> **Organization-wide protection = Sensitivity labels**

---

## 4️⃣ MICROSOFT PURVIEW (GOVERNANCE ENGINE)

![Image](https://learn.microsoft.com/en-us/purview/media/overview/high-level-overview-large.png)

![Image](https://learn.microsoft.com/en-us/purview/media/concept-lineage/lineage-end-end.png)

![Image](https://learn.microsoft.com/en-us/purview/media/catalog-lineage-user-guide/show-column-flow-in-lineage-inline.png)

### ❓ What is Microsoft Purview?

> The **governance and compliance backbone** for Fabric.

---

### ❓ WHAT does Purview provide?

* Data catalog
* Lineage
* Classification
* Impact analysis
* Audit & compliance

---

### ❓ WHEN do exam questions expect Purview?

When you see:

* “Discover data”
* “Understand lineage”
* “Audit data usage”
* “Compliance requirements”

---

### 🧠 EXAM RULE

> **Discovery, lineage, audit = Purview**

---

## 5️⃣ DATA LINEAGE (VERY COMMON)

### ❓ What is lineage?

> Shows **where data comes from and where it goes**.

Example:

```
Source → Dataflow → Lakehouse → Semantic Model → Report
```

---

### ❓ WHEN is lineage used?

* Impact analysis
* Change management
* Audits

---

### 🧠 EXAM RULE

> **Need to trace data flow = Lineage**

---

## 6️⃣ CERTIFICATION & PROMOTION (TRUST SIGNALS)

### ❓ What are Certified & Promoted datasets?

| Status    | Meaning            |
| --------- | ------------------ |
| Promoted  | Recommended        |
| Certified | Trusted & governed |

---

### ❓ WHEN to use Certification?

Use when:

* Dataset is enterprise-approved
* Users should trust & reuse it

---

### 🧠 EXAM RULE

> **Enterprise-trusted dataset = Certified**

---

## 7️⃣ ONE LAKE & GOVERNANCE

### ❓ How does OneLake help governance?

* Single storage layer
* Centralized access
* Reduced data duplication
* Easier auditing

---

### 🧠 EXAM RULE

> **Central storage = better governance**

---

## 8️⃣ GOVERNANCE VS PERMISSIONS (COMMON TRAP)

| Feature                | Governance? | Security? |
| ---------------------- | ----------- | --------- |
| Sensitivity labels     | ✅           | ✅         |
| Workspace roles        | ❌           | ✅         |
| Item-level permissions | ❌           | ✅         |
| RLS / OLS              | ❌           | ✅         |
| Purview lineage        | ✅           | ❌         |

🚫 Do NOT confuse roles with governance

---

## 9️⃣ DP-600 GOVERNANCE KEYWORDS (MEMORIZE)

| Keyword                   | Answer             |
| ------------------------- | ------------------ |
| Sensitive data            | Sensitivity labels |
| Compliance                | Purview            |
| Discover data             | Data catalog       |
| Trace data                | Lineage            |
| Trusted dataset           | Certified          |
| Organization-wide control | Governance         |

---

## 🔥 GOVERNANCE TRAP QUESTIONS (MINI)

### Q1

> Restrict access to sensitive data across Fabric?

❌ Workspace roles
✅ **Sensitivity labels**

---

### Q2

> Understand impact of deleting a table?

❌ Performance analyzer
✅ **Lineage**

---

### Q3

> Users must trust a dataset?

❌ Promote
✅ **Certify**

---

### Q4

> Find datasets across organization?

❌ OneLake Explorer
✅ **Purview Catalog**

---

## 🎯 FINAL GOVERNANCE MEMORY LOCK

> **Governance = classify, catalog, trace, trust**

---

## ✅ YOU’RE NOW EXAM-READY FOR GOVERNANCE

You now know:

* What governance is
* How it differs from security
* What DP-600 tests
* How to spot governance questions instantly

---

Perfect 🔥
This is **exactly the right level** for last-day DP-600 prep.

Below you’ll get **30 HIGH-QUALITY GOVERNANCE QUESTIONS**, split into:

1️⃣ **10 Governance TRAP questions** (exam-style, tricky wording)
2️⃣ **10 Case-study questions** (short scenarios like DP-600)
3️⃣ **10 Real-world project questions** (industry + decision logic)

I’ll include **answers + WHY**, but keep it **fast to revise**.

---

# 🔐 PART 1 — 10 GOVERNANCE TRAP QUESTIONS (DP-600 STYLE)

### 1️⃣

**Question:**
You need to restrict access to sensitive data across all Fabric items.

❌ Workspace roles
❌ Item-level permissions
✅ **Sensitivity labels**

🧠 Rule: **Organization-wide control = Sensitivity labels**

---

### 2️⃣

**Question:**
Users must discover datasets and understand how data flows end to end.

❌ OneLake Explorer
❌ Deployment pipelines
✅ **Microsoft Purview**

🧠 Rule: **Discovery + lineage = Purview**

---

### 3️⃣

**Question:**
You want users to trust a dataset as the official source.

❌ Promoted dataset
✅ **Certified dataset**

🧠 Rule: **Enterprise trust = Certified**

---

### 4️⃣

**Question:**
Which feature helps identify downstream impact before deleting a table?

❌ Performance Analyzer
❌ Sensitivity labels
✅ **Lineage**

---

### 5️⃣

**Question:**
Which is governance, not security?

❌ Row-level security
❌ Object-level security
✅ **Data catalog**

---

### 6️⃣

**Question:**
You want to classify data but not restrict access.

❌ RLS
❌ CLS
✅ **Sensitivity labels**

---

### 7️⃣

**Question:**
Which applies governance consistently across Lakehouse, Warehouse, and reports?

❌ Workspace roles
✅ **Sensitivity labels**

---

### 8️⃣

**Question:**
Auditors request usage tracking and compliance reporting.

❌ Item permissions
❌ Deployment pipelines
✅ **Microsoft Purview**

---

### 9️⃣

**Question:**
Which does NOT enforce governance?

❌ Dataset certification
❌ Lineage
✅ **Row-level security**

---

### 🔟

**Question:**
Which feature improves reuse and trust but does not change access?

❌ Sensitivity labels
✅ **Dataset promotion**

---

# 🧠 PART 2 — 10 CASE-STUDY GOVERNANCE QUESTIONS

### 1️⃣ Finance Case

A bank must classify customer data and apply compliance policies.

✅ **Sensitivity labels + Purview**

---

### 2️⃣ Healthcare Case

Auditors need to trace patient data from source to report.

✅ **Lineage in Purview**

---

### 3️⃣ Retail Case

Multiple teams reuse sales datasets; one must be official.

✅ **Certified semantic model**

---

### 4️⃣ Manufacturing Case

IoT data flows through notebooks → lakehouse → Power BI.

What ensures traceability?

✅ **Lineage**

---

### 5️⃣ Enterprise BI Case

Users complain they don’t know which dataset to use.

✅ **Promoted / Certified datasets**

---

### 6️⃣ Legal Compliance Case

Data must be labeled as Confidential automatically.

✅ **Sensitivity labels**

---

### 7️⃣ IT Governance Case

Admins want a single view of all data assets.

✅ **Purview Data Catalog**

---

### 8️⃣ Merger Case

Two organizations combine Fabric tenants and need consistent governance.

✅ **Sensitivity labels + Purview**

---

### 9️⃣ Security Audit Case

Auditors want to see who accessed sensitive reports.

✅ **Purview audit logs**

---

### 🔟 Data Ownership Case

Teams must know who owns each dataset.

✅ **Purview metadata & catalog**

---

# 🏭 PART 3 — 10 REAL-WORLD PROJECT-BASED QUESTIONS

### 1️⃣ Banking Project

Live transaction data, strict compliance, audit trails required.

✅ **Purview + Sensitivity labels**

---

### 2️⃣ Healthcare Analytics

Patient data must be masked, but lineage preserved.

✅ **Dynamic data masking + Lineage**

---

### 3️⃣ Retail Enterprise BI

Hundreds of reports, users confused about which dataset to trust.

✅ **Certified datasets**

---

### 4️⃣ Government Project

All data must follow classification rules.

✅ **Sensitivity labels**

---

### 5️⃣ Manufacturing Data Platform

Executives ask: “Where does this KPI come from?”

✅ **Lineage**

---

### 6️⃣ Insurance Reporting

Different departments reuse central datasets.

✅ **Promoted + Certified semantic models**

---

### 7️⃣ Telecom Big Data

Centralized lake with many consumers.

What improves governance?

✅ **OneLake + Purview**

---

### 8️⃣ SaaS Analytics Platform

Customers demand transparency in data flow.

✅ **Lineage + Catalog**

---

### 9️⃣ Retail Compliance

Some datasets are internal, some public.

✅ **Sensitivity labels**

---

### 🔟 Global Enterprise

Need to manage governance without changing user permissions.

✅ **Governance tools (labels, catalog, lineage)**

---

# 🎯 FINAL GOVERNANCE DECISION MAP (SAVE THIS)

| Requirement             | Choose               |
| ----------------------- | -------------------- |
| Classify / protect data | Sensitivity labels   |
| Discover data           | Purview catalog      |
| Trace data flow         | Lineage              |
| Trust datasets          | Certification        |
| Control access          | RLS / OLS (security) |

---

# 🧠 ONE-LINE MEMORY LOCK (EXAM GOLD)

> **Governance = classify, catalog, trace, trust**
> **Security = allow or deny access**

---

## ✅ YOU ARE NOW VERY STRONG IN GOVERNANCE

 
