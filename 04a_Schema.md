## 🗄️ Data & Logic: Sample Database Schema

This schema is designed for a relational research environment (e.g., **SQLite** or **PostgreSQL**). By using **RICs (Reuters Instrument Codes)** or **SEDOLs** as Primary Keys, we ensure that data from institutional providers like LSEG remains synchronized with our internal logic. 

This schema is designed for a relational research environment (e.g., SQLite or PostgreSQL). By using RICs (Reuters Instrument Codes) or SEDOLs as Primary Keys, we ensure that data from institutional providers like LSEG remains synchronized with our internal logic.

**📘 Understanding Data Types**
In a structured database, every column is assigned a Data Type to ensure computational accuracy and memory efficiency.

- VARCHAR / TEXT: Used for alphanumeric strings (names, RICs).
- INTEGER: Used for whole numbers (years).
- BIGINT: Used for very large whole numbers (multi-billion dollar revenues) to prevent overflow errors.
- FLOAT / REAL: Used for numbers with decimal points (ratios like P/E).
- DATE: Specifically formatted for time-series consistency.

---

### **1. The Master Registry**
The *Source of Truth* for your investment universe metadata.

| Column | Type | Description |
| :--- | :--- | :--- |
| `RIC` | **PRIMARY KEY** | Unique identifier (e.g., `SONY.T`, `MSFT.O`) |
| `SEDOL` | VARCHAR | Global identifier for cross-border reconciliation |
| `Company_Name` | VARCHAR | Formal legal entity name |
| `Sector` | VARCHAR | Industry classification (GICS or internal) |
| `Currency` | VARCHAR | Reporting currency (e.g., JPY, USD) |

---

### **2. Fundamentals Table (`fact_fundamentals`)**
Stores the high-level valuation snapshots used for screening.

| Column | Type | Description |
| :--- | :--- | :--- |
| `RIC` | **FOREIGN KEY** | Links to the Master Registry |
| `Date` | DATE | Snapshot timestamp |
| `PE_Ratio` | FLOAT | Price-to-Earnings (1 dp) |
| `PB_Ratio` | FLOAT | Price-to-Book (1 dp) |
| `EV_EBITDA` | FLOAT | Enterprise Value to EBITDA |
| `Div_Yield` | FLOAT | Indicated Dividend Yield |

---

### **3. Income Statement Table (`fact_income_statement`)**
Time-series data for historical profitability analysis.

| Column | Type | Description |
| :--- | :--- | :--- |
| `RIC` | **FOREIGN KEY** | Links to the Master Registry |
| `Fiscal_Year` | INTEGER | Year of the reporting period |
| `Total_Revenue` | BIGINT | Top-line revenue in local currency |
| `Net_Income` | BIGINT | Bottom-line profit |
| `EBIT` | BIGINT | Earnings Before Interest and Taxes |

---

### **4. Cash Flow Table (`fact_cash_flow`)**
The *Truth Layer* for analyzing quality of earnings.

| Column | Type | Description |
| :--- | :--- | :--- |
| `RIC` | **FOREIGN KEY** | Links to the Master Registry |
 `Fiscal_Year` | INTEGER | Year of the reporting period |
| `Operating_CF` | BIGINT | Cash generated from core operations |
| `CapEx` | BIGINT | Capital Expenditures |
| `Free_Cash_Flow` | BIGINT | Operating Cash Flow minus CapEx |

---

### 📘 Implementation Notes
* **Normalization:** By separating Income Statement and Cash Flow items into distinct tables, we prevent *Wide Table Syndrome,* making it easier to add new line items in the future without breaking existing queries.
* **Master Keys:** Always clean your `RIC` and `SEDOL` strings (strip whitespace) before insertion to ensure the relational joins function correctly.

**📘 Strategic Guidelines for Database Management**
The Power of the Foreign Key: By using the RIC across all tables, you can write a single SQL query to pull a company's P/E Ratio alongside its Free Cash Flow for the last five years instantly.


💡 Pro Tip: The database schema can contain hundreds of datapoints, so creating a naming convention for metrics that can be easily remembered is essential for ease of use in your code blocks. For example, for inventory and receivables data over time use a convention like INV2025, INV2024, REC2025, REC2024 etc.  
