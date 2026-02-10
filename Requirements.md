The Requirements File (requirements.txt)

NOTE: The libraries noted below are just recommendations for those that we found useful in our architechture.

Copy and save the following into a file named requirements.txt in your repository's root directory:

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
To build a stable research engine, you must prevent "Dependency Hell"—a state where different software libraries conflict and break your system. The following instructions ensure your "Fortress" is built on a clean, isolated foundation.

1. Install your Distributor
You require a distribution manager to handle package deployment .

Anaconda: The full-featured "landlord" of your building, pre-packaged with extensive libraries .

2. Create your Isolated "Workshop"
Open your terminal (or Anaconda Prompt) and run the following commands to create and enter a sealed environment .

Bash
# Create an environment named 'fortress' using Python 3.11
conda create -n fortress python=3.11

# Activate the environment
conda activate fortress
3. Populate the Toolbox
With your environment active, install all necessary libraries at once using the requirements.txt file .

Bash
pip install -r requirements.txt

4. Launching the Interface

Always launch your Integrated Development Environment (IDE), such as VS Code, from within this activated terminal. This ensures your workbench has access to the specific tools you just installed.
