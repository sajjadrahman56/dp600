# 🛡️ Microsoft Fabric (DP-600) Security: The Ultimate Cheat Sheet

This note is designed for a high-impact review before your exam to help you distinguish between security methods instantly.

---

## 🚀 1. Quick Summary Table (Decision Matrix)

| Security Type | Core Action | Metadata Visibility | Key Exam Keywords |
| --- | --- | --- | --- |
| **RLS** | Filters **Rows** (Horizontal) | Visible | `Filter Predicate`, `Security Policy`, `Region`, `User Identity` |
| **CLS** | Restricts **Columns** (Vertical) | Visible | `Deny Select`, `Sensitive Column`, `Salary`, `SSN` |
| **OLS** | Hides **Objects** entirely | **Hidden (Invisible)** | `Hide Table`, `Metadata Security`, `Object doesn't exist` |
| **DDM** | **Masks** Data (Disguise) | Visible | `Mask`, `Redact`, `Partial()`, `Email/Credit Card format` |

---

## 🔍 2. Detailed Breakdown & Exam Scenarios

### **A. Row-Level Security (RLS)**

* **Use Case:** When users share the same table but should only see specific rows (e.g., Sales Managers seeing only their territory).
* **Exam Tip:** If the question mentions creating a **"Filter Function"** or **"Security Policy"**, the answer is **RLS**.
* **Scenario:** "Users should only be able to see their own transactions."  **RLS**.

### **B. Column-Level Security (CLS)**

* **Use Case:** When specific columns contain sensitive PII (Personally Identifiable Information) that should be restricted.
* **Exam Tip:** Look for SQL code using `DENY SELECT` on specific columns.
* **Scenario:** "Everyone can see the Customer table, but the 'CreditCard' column must be restricted to the Finance team only."  **CLS**.

### **C. Object-Level Security (OLS)**

* **Use Case:** The most restrictive form. It prevents users from even knowing a table or column exists.
* **Exam Tip:** If the question mentions hiding **"Metadata"** or preventing **"Schema Discovery"**, the answer is **OLS**.
* **Scenario:** "Ensure that unauthorized users cannot see the 'Bonuses' table listed in their field list or query options."  **OLS**.

### **D. Dynamic Data Masking (DDM)**

* **Use Case:** To display data in a safe format without hiding the entire row or column.
* **Exam Tip:** If you see functions like `Partial()`, `Default()`, or `Email()`, it is **DDM**.
* **Scenario:** "A call center agent needs to see a customer’s email for verification, but it must be displayed as `a***@domain.com`."  **DDM**.

---

## ⚠️ 3. Critical Exam Traps (Pay Attention!)

* **Permissions Matter:** In Microsoft Fabric, RLS/CLS/DDM usually **do not apply** to users with "Admin", "Member", or "Contributor" roles in the workspace. The user must have the **"Viewer"** role for these security rules to trigger.
* **Performance Impact:** RLS can slow down queries if the filter logic is too complex. CLS is generally faster as it is a direct permission check.
* **Direct Lake Fallback:** Be aware that applying RLS/CLS in a Fabric Warehouse might cause Power BI reports to fall back from **Direct Lake** mode to **DirectQuery** mode, which affects performance.

---

## 💡 Memory Technique (The Library Analogy)

* **RLS:** You enter the library, but you can only see books from your specific department on the shelves.
* **CLS:** You can see the books, but the pages containing "Price" or "Author Address" are blacked out.
* **OLS:** The book is not even listed in the library catalog; you don't even know it exists.
* **DDM:** You see the book, but the phone numbers inside are printed as `017********`.

---
