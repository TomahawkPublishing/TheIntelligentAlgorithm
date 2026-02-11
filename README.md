## The Intelligent Algorithm: Value Investing in the Age of Artificial Intelligence 

This repository provides a modular toolkit to support the text of the book published in March 2026. The aim is to help you build your own *Fortress* research environment. Each component is intentionally stripped back to its core logic to serve as a readable guidepost for your own development. For the complete guide buy the book here www.intelligentalgorithm.com.

## ⚖️ Conceptual Framework
This toolkit is built upon the **Four Laws** established in the book:

- **Sovereign Fortress:** Run your logic on your own silicon to protect your IP.
- **Industrialized Curiosity:** Automate data retrieval to focus on deep reasoning.
- **Reasoning over Prediction:** Use LLMs as logic engines, not crystal balls.
- **Probabilistic Mindset:** Structure data to survive uncertainty, not just predict outcomes.


## 🛠️ Tools Provided

**1. Environment & Setup**
Conda/Anaconda Guide: Step-by-step instructions for creating isolated Python virtual environments to prevent library conflicts. For detailed environment instructions, see our [Setup Guide](./01a_EnvironmentSetup.md)
Library Management: A ```requirements.txt``` file and guide for installing essential financial and AI libraries (Pandas, Streamlit, OpenAI, etc.) [Requirements](./01b_Requirements.md).

**2. Web Applications & UI**
Sydney Weather App: A simple Streamlit application to get you up and running with your very own localhost server. [Weather App](./02a_StreamlitWeatherApp).
A simple AI chatbot in Streamlit connected to OpenAI and Tavily (you will need your own API Keys). [Chatbot](./02b_StreamlitAIChatbot).

**3. API Integrations & Connectivity**
LSEG (Refinitiv) Integration: Sample code to authenticate and pull fundamental data, such as a trailing P/E Ratio, directly into your Streamlit environment. Check [LSEG Snapshot](./03_LSEGSnapshot) for more information. You will need your own API key.

**4. Data & Logic**
Database Schema: A sample schema for organizing your data for high-speed querying. Find the basic guidelines [here](./04a_Schema.md).
In addition, there are some basic instructions for setting up an [SQLite](./04b_CreateSQLiteDatabase.md) database using this schema and some sample [script](./04c_DatabaseInitializer) showing how to retrieve data from it.  

**5. The Dummy AI Prompt**

A sample financial analysis prompt designed to demonstrate **Constraint-based** prompt engineering. Tailor as you will. [Dummy Prompt](./05_DummyPrompt.md).

---

## 🏗️ The Repository Architecture
To visualize how these components interact within your *Fortress*, consider this mental model:

* **The Foundation (Registry/DB):** Your `MasterData.db` acts as the persistent memory, ensuring data sovereignty.
* **The Windows (API/Connectivity):** LSEG, OpenAI, and Tavily provide the external views and raw materials for your analysis.
* **The Front Door (Streamlit UI):** The interface where you interact with your data and AI logic in a secure, local environment.
* **The Engine (The Prompt):** The internal logic and "Intelligent Algorithm" that directs the AI's reasoning.

*Good luck :)* 

---
## 🚀 Deployment & Security
### Local-First Architecture
This toolkit is designed for **Local Deployment**. The Streamlit applications are intended to run on your own machine (localhost) to ensure that your proprietary research data and API keys never leave your controlled environment.

### GitHub & Git Hygiene
If you use GitHub to track your progress, you must protect your "Fortress" by using a `.gitignore` file. This prevents sensitive files from being uploaded to the public web. 

**Essential .gitignore Rules:**
Create a file named `.gitignore` in your root directory and add the following lines:
```text
# Sensitive API Keys
*APIKey.txt
.env

# Local Databases
*.db
*.sqlite

# Python Environment & Cache
venv/
__pycache__/
.DS_Store
```

## ⚠️ Disclaimer & Usage

### 1. For Educational and Research Purposes Only
The code and logic contained in this repository are provided as a **skeletal proof-of-concept**. This environment is intentionally *open* to facilitate learning and **lacks the enterprise-grade error handling, multi-layer encryption, and systemic fail-safes** required for a production-level institutional environment. Use in a live trading or production setting is strictly at the user's own risk.

### 2. No Investment Advice
This repository and its associated book, *The Intelligent Algorithm*, do not constitute financial, investment, or legal advice. 
* **Not a Black Box:** The tools provided are designed to augment human reasoning and facilitate **probabilistic thinking**; they are not an automated system for generating trade signals or financial recommendations.
* **Independent Diligence:** Users must perform their own independent research and consult with qualified professionals before making any investment decisions.

### 3. Security & API Responsibility
Users maintain **total sovereignty** and responsibility over their local environment:
* **Cost Management:** You are solely responsible for any costs incurred via third-party APIs (LSEG, OpenAI, Tavily, etc.).
* **Credential Security:** You are responsible for the encryption and storage of your API keys. **NEVER** commit `.env` files, `.txt` keys, or database files to a public repository. 
* **Data Privacy:** This toolkit is designed for local execution. Deploying these applications to the cloud may expose your proprietary research and sensitive keys; do so only with a full understanding of the security implications.

### 4. Limitation of Liability
The author and contributors shall not be held liable for any financial losses, data breaches, or system failures resulting from the use or modification of this code.



