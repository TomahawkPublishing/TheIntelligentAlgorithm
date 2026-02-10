### 🗄️ Data & Logic: Sample Database Schema

This schema is designed for an SQLite or PostgreSQL environment. It follows the "Architecture of Information" by separating metadata from volatile financial metrics.

**1. The Master Registry**

This table acts as the "Source of Truth" for every entity in your universe.

Column	Type	Description
RIC	PRIMARY KEY	The unique identifier (e.g., SONY.T)
SEDOL	VARCHAR	Secondary unique identifier for global cross-referencing
Company_Name	VARCHAR	The formal entity name
Sector	VARCHAR	Industry classification
Currency	VARCHAR	The reporting currency of the entity

**2. Fundamentals Table (fact_fundamentals)**
Captures the "Snapshot" metrics that drive your initial screening.

Column	Type	Description
RIC	FOREIGN KEY	Links to the Master Registry
Date	DATE	The date the snapshot was captured
PE_Ratio	FLOAT	Price-to-Earnings (1 dp)
PB_Ratio	FLOAT	Price-to-Book (1 dp)
EV_EBITDA	FLOAT	Enterprise Value to EBITDA
Div_Yield	FLOAT	Indicated Dividend Yield

**3. Income Statement Table (fact_income_statement)**
Stores time-series data for historical analysis.

Column	Type	Description
RIC	FOREIGN KEY	Links to the Master Registry
Fiscal_Year	INTEGER	The year of the report
Total_Revenue	BIGINT	Top-line revenue in local currency
Net_Income	BIGINT	Bottom-line profit
EBIT	BIGINT	Earnings Before Interest and Taxes

**4. Cash Flow Table (fact_cash_flow)**
Essential for your "Quality of Earnings" checks.

Column	Type	Description
RIC	FOREIGN KEY	Links to the Master Registry
Fiscal_Year	INTEGER	The year of the report
Operating_CF	BIGINT	Cash generated from core operations
CapEx	BIGINT	Capital Expenditures
Free_Cash_Flow	BIGINT	Operating CF minus CapEx

**📘 Strategic Guidelines for Database Management**
The Power of the Foreign Key: By using the RIC across all tables, you can write a single SQL query to pull a company's P/E Ratio alongside its Free Cash Flow for the last five years instantly.

Industrialization: In your book's framework, this schema allows you to move from "searching for data" to "querying for insight." You are no longer managing files; you are managing a structured library.

Data Integrity: Always ensure your RIC or SEDOL strings are cleaned of whitespace. A SONY.T (with a space) will not match SONY.T (without a space), causing a "Ghost in the Machine" during your analysis.
