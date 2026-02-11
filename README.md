## The Intelligent Algorithm: Value Investing in the Age of Artificial Intelligence 

This repository provides a modular toolkit to support the text of the book published in March 2026. The aim is to help you build your own "Fortress" research environment. Each component is intentionally stripped back to its core logic to serve as a readable guidepost for your own development. Buy the book here www.intelligentalgorithm.com.

1. Environment & Setup
Conda/Anaconda Guide: Step-by-step instructions for creating isolated Python virtual environments to prevent library conflicts. For detailed environment instructions, see our [Setup Guide](./01a_EnvironmentSetup.md)
Library Management: A requirements.txt file and guide for installing essential financial and AI libraries (Pandas, Streamlit, OpenAI, etc.) [Requirements](./01b_Requirements.md).

2. Web Applications & UI
Sydney Weather App: A simple Streamlit application to get you up and running with your very own localhost server [Weather](./02a_StreamlitWeatherApp).
A simple AI chatbot in Streamlit connected to OpenAI and Tavily (you will need your own API Keys) [Chatbot](./02b_StreamlitAIChatbot).

3. API Integrations & Connectivity
LSEG (Refinitiv) Integration: Sample code to authenticate and pull fundamental data, such as a trailing P/E Ratio, directly into your Streamlit environment. Check [LSEG Snapshot](./03_LSEGSnapshot) for more information. You will need your own API key.

4. Data & Logic
Database Schema: A sample schema for organizing your data for high-speed querying. Find the basic guidelines [here](./04a_Schema.md).
In addition, there are some basic instructions for setting up an [SQLite](./04b_CreateSQLiteDatabase.md) database using this schema and is some sample [script](./04c_DatabaseInitializer) showing how to retrieve data from it.  

6. A The Dummy AI Prompt: A sample financial analysis prompt designed to demonstrate "Constraint-based" prompt engineering. Tailor as you will. [Dummy Prompt](./05_DummyPrompt.md).

⚠️ Disclaimer & Usage
For Educational Use Only The code provided here is a skeletal framework. It is intentionally basic and lacks the robust error-handling, encryption, and "fail-safes" required for a production-level institutional environment.

Not Financial Advice: This repository does not provide investment recommendations. The "Intelligent Algorithm" is designed to assist in human reasoning and probabilistic thinking; it is not a "black box" for generating trades.

API Responsibility Users are responsible for their own API keys and any costs incurred through LSEG, OpenAI, or Tavily. Never commit your .env files or raw API keys to a public repository.
