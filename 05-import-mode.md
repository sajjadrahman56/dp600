# 🔥 What is a “MODE” in Power BI / Fabric?

## ❓ What does *mode* mean?

A **storage mode** defines:

> **WHERE the data lives**
> **HOW queries are executed**
> **WHO does the compute work**

Think of mode as the **contract between Power BI and the data**.

---

## 🧠 Big Picture (one glance)

![Image](https://i0.wp.com/radacad.com/wp-content/uploads/2023/06/directlake-diagram-1.png?ssl=1)

![Image](https://learn.microsoft.com/en-us/fabric/onelake/media/onelake-overview/access-onelake-data-other-tools.png)

![Image](https://i0.wp.com/radacad.com/wp-content/uploads/2017/09/2017-09-13_12h13_49.png?fit=1155%2C723\&ssl=1)

---

# 1️⃣ IMPORT MODE — “Data lives INSIDE Power BI”

## 🔹 What is Import mode?

In **Import mode**, data is:

* Copied into the **semantic model**
* Stored in **VertiPaq (compressed, in-memory)**
* Queried **without touching the source**

### 📍 Where is the data?

➡️ Inside Power BI / Fabric capacity memory

---

## 🔹 How Import mode works (step-by-step)

1. Power BI **imports data**
2. Data is **compressed**
3. Queries run **in-memory**
4. Source system is **not queried again** (until refresh)

---

## 🔹 When should you use Import mode?

Use Import mode when:

* ❌ No lakehouse / warehouse exists
* ✅ Data size is manageable
* ✅ Performance is top priority
* ❌ Near real-time is NOT required

---

## 🏭 Real-world industry examples

### 📊 Finance / Sales reporting

* Monthly revenue
* Budget vs actuals
* Excel / CSV / SQL sources

### 🏢 Small–Medium companies

* No Fabric storage yet
* Want fast dashboards quickly

---

## 🧠 Exam rule

> **No OneLake + fast analytics = Import**

---

# 2️⃣ DIRECT LAKE MODE — “Data stays in OneLake”

## 🔹 What is Direct Lake?

Direct Lake:

* Reads **Delta tables directly from OneLake**
* No data copy into Power BI memory
* Uses Fabric-optimized query engine

### 📍 Where is the data?

➡️ **OneLake (Lakehouse / Warehouse)**

---

## 🔹 How Direct Lake works

1. Data stored as **Delta files**
2. Power BI reads data **directly**
3. Queries bypass SQL & refresh
4. Near Import-like performance

---

## 🔹 When should you use Direct Lake?

Use Direct Lake when:

* ✅ Data is **very large**
* ✅ Data already in **OneLake**
* ✅ Near real-time reporting needed
* ❌ You want minimal data duplication

---

## 🏭 Real-world industry examples

### 🏬 Retail

* Billions of sales transactions
* Frequent updates
* Central lakehouse

### 🏭 Manufacturing / IoT

* Sensor data
* Streaming + batch analytics
* Fabric-native architecture

---

## 🧠 Exam rule

> **Big data + OneLake + NRT = Direct Lake**

---

# 3️⃣ DIRECTQUERY MODE — “Data stays at the SOURCE”

## 🔹 What is DirectQuery?

In DirectQuery:

* Data is **never imported**
* Every visual sends queries to the source
* Power BI acts as a **query generator**

### 📍 Where is the data?

➡️ External system (SQL, Azure SQL, Synapse, etc.)

---

## 🔹 How DirectQuery works

1. User interacts with report
2. Power BI generates SQL/KQL
3. Query runs on source system
4. Results returned to visual

---

## 🔹 When should you use DirectQuery?

Use DirectQuery when:

* ✅ Source must stay **authoritative**
* ✅ Data changes constantly
* ❌ You cannot copy data
* ❌ Latency is acceptable

---

## 🏭 Real-world industry examples

### 🏦 Banking

* Live account balances
* Regulatory systems
* No data duplication allowed

### 🏥 Healthcare

* Patient systems
* Compliance constraints
* Real-time lookups

---

## 🧠 Exam rule

> **Source must remain authoritative = DirectQuery**

---

# 🔥 SIDE-BY-SIDE: HOW THEY REALLY DIFFER

| Aspect         | Import          | Direct Lake  | DirectQuery   |
| -------------- | --------------- | ------------ | ------------- |
| Data location  | Power BI memory | OneLake      | Source system |
| Performance    | ⭐⭐⭐⭐⭐           | ⭐⭐⭐⭐☆        | ⭐⭐            |
| Near real-time | ❌               | ✅            | ✅             |
| Data refresh   | Required        | Not required | Not required  |
| Source load    | None            | Minimal      | High          |
| Big data       | ⚠️              | ✅            | ⚠️            |
| Fabric-native  | ❌               | ✅            | ❌             |

---

# 🧠 REAL-WORLD DECISION LOGIC (EXAM GOLD)

Ask these **in order**:

### 1️⃣ Is data already in OneLake?

→ **Direct Lake**

### 2️⃣ Must source stay authoritative?

→ **DirectQuery**

### 3️⃣ No Fabric storage & need speed?

→ **Import**

---

# 🔥 COMMON DP-600 TRAPS (NOW YOU’LL AVOID)

❌ “Import can’t handle large data”
✔ It can — depends on compression & capacity

❌ “DirectQuery is best for real-time”
✔ Direct Lake is usually better in Fabric

❌ “You must use Lakehouse”
✔ Import works without any Fabric storage

---

# 🎯 FINAL MEMORY LOCK

> **Import = data inside model**
> **Direct Lake = data in OneLake**
> **DirectQuery = data at source**

---

 
