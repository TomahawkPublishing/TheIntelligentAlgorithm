Repository Contents
This repository provides a modular toolkit to help you build your own "Fortress" research environment. Each component is intentionally stripped back to its core logic to serve as a readable guidepost for your own development.

1. Web Applications & UI
Sydney Weather App: A "Hello World" Streamlit application to verify your local server and Cloudflare Tunnel are functioning correctly.

AI Research Chatbot (Coming Soon): An example Streamlit interface integrating the OpenAI API with Tavily for real-time web-augmented research.

2. Environment & Setup
Conda/Anaconda Guide: Step-by-step instructions for creating isolated Python virtual environments to prevent library conflicts.

Library Management: A requirements.txt file and guide for installing essential financial and AI libraries (Pandas, Streamlit, OpenAI, etc.).

3. API Integrations & Connectivity
LSEG (Refinitiv) Integration: Sample code to authenticate and pull fundamental data, such as a trailing P/E Ratio, directly into your environment.

OpenAI & Tavily: Boilerplate code for connecting to frontier models and search tools to provide your "Virtual Analyst" with real-time context.

Cloudflare Tunneling: Configuration samples for setting up a secure "subway" connection to your local Mac Mini without opening public ports.

4. Data & Logic
Database Schema: A sample "Goldilocks" schema for organizing financial and ESG data for high-speed querying.

The Dummy Prompt: A sample financial analysis prompt designed to demonstrate "Constraint-based" prompt engineering, without revealing the firm’s proprietary methodologies.

⚠️ Disclaimer & Usage
For Educational Use Only The code provided here is a skeletal framework. It is intentionally basic and lacks the robust error-handling, encryption, and "fail-safes" required for a production-level institutional environment.

Not Financial Advice This repository does not provide investment recommendations. The "Intelligent Algorithm" is designed to assist in human reasoning and probabilistic thinking; it is not a "black box" for generating trades.

API Responsibility Users are responsible for their own API keys and any costs incurred through LSEG, OpenAI, or Tavily. Never commit your .env files or raw API keys to a public repository.
