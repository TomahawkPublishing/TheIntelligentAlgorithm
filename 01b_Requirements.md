## 📄 The Requirements File 

Note: The libraries listed below are recommendations of those we found useful in core architecture. 

Copy and save the library names as a long list in Notepad and save the file as ```requirements.txt``` in your repository’s root directory:

**Core UI & Visualization**

```streamlit 
plotly 
matplotlib 
kaleido
```

**Data Engine & Storage**

```pandas 
numpy 
sqlite3
```

**Institutional Connectivity**

```refinitiv-data 
lseg.data
```

**Intelligence & Search**

```openai 
tavily-python 
json_repair
```

**Document Processing**

```pypdf 
pypdf2 
python-docx 
markdown
```

**System & Security**

```python-dotenv 
pycryptodome
```

Once you have followed the steps in our [Setup Guide](./SETUP.md) open you terminal in the Code Editor (IDE) and run the following:

```bash
pip install -r requirements.txt
```

## 📘 Why a Requirements File is Preferred

While a one-line install is efficient for a quick setup, maintaining a ```requirements.txt``` file is the preferred standard for building a Sovereign Fortress for three key reasons:


- Version Pinning: A requirements.txt allows you to lock specific versions (e.g., pandas==2.1.0). This prevents your "Intelligent Algorithm" from breaking when a library releases a new version that is incompatible with your current code.
- Reproducibility: It ensures that if you move your research to a new machine—or if a reader of your book wants to follow along—everyone is using the exact same software environment, eliminating the "it works on my machine" problem.
- Automation: It allows for a clean, one-command environment build: pip install -r requirements.txt. This industrializes the setup process, moving away from manual, error-prone terminal entries.

**🏗️ One-Line Installation (Alternative)**

If you prefer to install all dependencies manually in a single step, run the following command in your terminal:

```bash
pip install streamlit plotly matplotlib kaleido pandas numpy refinitiv-data lseg.data openai tavily-python json_repair pypdf pypdf2 python-docx markdown python-dotenv pycryptodome
```

*Note: sqlite3 is part of the Python Standard Library and does not require a separate installation.*

💡 Pro-Tip: Always launch your Integrated Development Environment (IDE), such as VS Code, from within this activated terminal. This ensures your workbench has direct access to the specific tools and libraries you just installed.
