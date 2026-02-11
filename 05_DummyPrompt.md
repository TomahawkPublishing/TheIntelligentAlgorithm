### 🏗️ A. The Dummy AI Prompt: "The System Schema"
This template demonstrates ***Constraint-Based*** Prompt Engineering. 

The Meta-Template
Use this structure as a baseline. The variables in brackets [ ] should be tailored to your specific investment philosophy.

**THE ANALYTICAL PERSONA**
Act as an [INDUSTRY ROLE] tasked with performing a [TYPE OF ANALYSIS]. 
Your objective is to provide a neutral, probabilistic assessment of 
the subject matter based on provided data.

**THE LOGICAL CONSTRAINTS** 

1. **Linguistic Neutrality:** Remove all subjective qualifiers. Convert 
   descriptive narrative into objective, evidence-based statements.
2. **The Counter-Thesis:** For every positive observation identified, 
   the model must generate a logical "Pressure Test" or failure scenario.
3. **Data Hierarchy:** Prioritize [SPECIFIC DATA TYPE] over [SECONDARY DATA TYPE]. 
   If a conflict between sources occurs, defer to the primary source.
4. **Contextual Anchoring:** Identify if the current data set appears 
   to be an outlier compared to the 5-year historical average.

**OUTPUT STRUCTURE**
The analysis must be delivered in the following modular format:
- **I. Structural Foundation:** (Primary data and core metrics)
- **II. Logic Check:** (The skepticism layer and counter-arguments)
- **III. Probability Range:** (The estimated outcomes based on evidence)

**INPUT DATA**
[PASTE YOUR AGGREGATED RESEARCH OR LSEG DATA HERE]

**💡 Pro Tip: Tuning the "Engine" (Temperature & Tokens)**
To achieve institutional-grade results, you must calibrate the model's technical parameters. In your code (OpenAI/Tavily integrations), consider the following settings:

- Temperature (0.0 to 0.3): For financial analysis, keep this low. A temperature of 0.0 makes the model deterministic and literal. Higher temperatures (above 0.7) introduce "creativity," which in a valuation context is often synonymous with "hallucination."
- Max Tokens: Set this based on your required depth. A *Quick Snapshot* may only need 500 tokens, while a *Deep Dive* into an annual report might require 2000+. Limiting tokens forces the AI to be concise and prevents *drift.* It also reduces compute costs. 
- Frequency/Presence Penalty: Set these to 0.0. You want the model to be able to repeat key financial terms or RICs as often as necessary without the AI trying to find *creative* synonyms that might obscure the data.

📘 Strategic Guidelines for Implementation
- Modular Thinking: Encourage users to swap out the Linguistic Neutrality rule for their own constraints. This demonstrates the utility of the tool without giving away your specific "Red Flags."
- The Counter-Thesis Logic: This is a high-value educational point. It teaches the "Probabilistic Mindset" by forcing the AI to look for the "Bear Case" without defining exactly what your specific bear indicators are.
- Industrializing Curiosity: By standardizing the Output Structure, you show how a researcher can quickly scan 50 different analyses and find the information they need in the exact same spot every time.
