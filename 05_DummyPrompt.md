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
- Modular Thinking: ***Customize Your Guardrails.*** Do not treat the *Linguistic Neutrality* rule as static. Swap it out for constraints that align with your specific mandates. For example, if you are analyzing distressed debt, replace it with a rule requiring the model to "Identify all legal seniority claims in the capital structure." This allows you to leverage the tool's utility while maintaining your proprietary *Red Flag* indicators in your own local environment.
- The Counter-Thesis: ***Mandate Internal Dissent.*** Institutionalize a *Probabilistic Mindset* by making the Counter-Thesis constraint mandatory in every prompt. By forcing the AI to generate a failure scenario for every positive observation, you bake objective skepticism into your workflow. Use this to automate the bear case.
- Industrializing Curiosity: ***Standardize for Speed.*** Strictly adhere to the Output Structure. By enforcing a consistent modular format (Foundation, Logic Check, Probability Range), you transition from reading to scanning. This allows you to process hundreds of company analyses in the time it usually takes to read five, knowing exactly where to find the "Logic Check" in every document.
