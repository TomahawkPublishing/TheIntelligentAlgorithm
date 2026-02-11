##📘 Guide: Creating your SQLite Database

Since SQLite is "serverless," the database is simply a file on your machine. However, the file must be initialized with your specific table structures before the script above can read it.

**Option A: Using Python to initialize (Recommended)**
You can create a separate "Setup" script (e.g., init_db.py) that runs the CREATE TABLE commands. This ensures your "Fortress" can be rebuilt instantly on any new machine.
Find a sample script [here](./DatabaseIntializer).

**Option B: Using a GUI (DB Browser for SQLite)**
Download DB Browser for SQLite (standard tool for researchers).

Click New Database and save it as MasterData.db.

Go to the Execute SQL tab.

Paste the CREATE TABLE commands from your Schema Markdown.

Click Execute.
