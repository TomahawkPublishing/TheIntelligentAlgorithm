## 🏗️ Environment & Setup: The Conda Guide

To ensure your research engine runs predictably, you must isolate your workspace. Think of a Virtual Environment as a sealed *clean room* where you define exactly which tools are on the shelves to prevent *Dependency Hell* and library conflicts.

**Step 1: Install your Distributor**

- Before creating an environment, you need a distribution manager to act as the *landlord* of your building.
- Anaconda: The full-featured *landlord.* It comes pre-packaged with an extensive library of data science tools.
- Miniforge/Miniconda: A lighter, *bare-bones* version for those looking to save disk space and system resources.

**Step 2: Create the "Workshop"**

Open your terminal (or Anaconda Prompt) to create your isolated room. We recommend using Python 3.11 for maximum compatibility with institutional financial APIs and modern LLM libraries.

Create an environment named 'fortress'

```bash
conda create -n fortress python=3.11
```

**Step 3: Activate the Environment**

You must "enter" the room before you can begin your research or run any scripts .

```bash
conda activate fortress
```

**Step 4: Install the Essentials**

Once inside, use the provided ```requirements.txt``` to install the complete "toolbox" required for this repository in one go. More information on setting up your file can be found [here](./01b_Requirements.md).


```bash
pip install -r requirements.txt
```

**The Setup Hierarchy**

To maintain a stable development environment, always follow this Workforce Hierarchy:

- Distributor: Anaconda *(The Landlord)*.
- Environment: Your fortress workshop *(The Locked Room)*.
- Interface: VS Code or Jupyter *(The Workbench)*.

**💡 Pro-Tip:** Always launch your code editor (like VS Code) from within the activated environment in your terminal. This ensures your workbench sees and uses the specific tools you have installed for this project.
