The Requirements File (requirements.txt)
Note: The libraries listed below are recommendations based on the core architecture of the "Fortress" environment.

Copy and save the following content into a file named requirements.txt in your repository’s root directory:

Plaintext
# --- Core UI & Visualization ---
streamlit 
plotly 
matplotlib 
kaleido

# --- Data Engine & Storage ---
pandas 
numpy 
sqlite3

# --- Institutional Connectivity ---
refinitiv-data 
lseg.data

# --- Intelligence & Search ---
openai 
tavily-python 
json_repair

# --- Document Processing ---
pypdf 
pypdf2 
python-docx 
markdown

# --- System & Security ---
python-dotenv 
pycryptodome
README Addition: Item 1 – Environment & Setup
To build a stable research engine, you must prevent "Dependency Hell"—a state where conflicting software libraries break your system. The following instructions ensure your "Fortress" is built on a clean, isolated foundation.

1. Install your Distributor
You require a distribution manager to handle package deployment and library management.

Anaconda: The full-featured "landlord" of your building, pre-packaged with extensive data science libraries.

2. Create your Isolated "Workshop"
Open your terminal (or Anaconda Prompt) and run the following commands to create and enter a sealed environment. We recommend Python 3.11 for maximum compatibility.

Bash
# Create an environment named 'fortress'
conda create -n fortress python=3.11

# Activate the environment
conda activate fortress
3. Populate the Toolbox
With your environment active, install all necessary libraries at once using the requirements.txt file you created in the previous step.

Bash
pip install -r requirements.txt
4. Launching the Interface
💡 Pro-Tip: Always launch your Integrated Development Environment (IDE), such as VS Code, from within this activated terminal. This ensures your workbench has direct access to the specific tools and libraries you just installed.
