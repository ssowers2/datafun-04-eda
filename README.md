# datafun-04-eda
Steps to creating a new Jupyter notebook project

IMPORTANT: To run Jupyter within VS Code, use the Jupyter extension. Go to the Extensions pane on the left sidebar (the icon looks like four squares), searching for "Jupyter," and installing the "Jupyter" extension provided by Microsoft.
---

## Step 1: Create a new repository in Github
1. Log in to GitHub.
Go to Profile>"Your repositories"
Click the "New" button OR in the top-right corner of GitHub>click the + dropdown menu>Select New repository.
Provide a brief description of your project.
Select the Public option so others can view my repository.
Add a Default README File by checkinh the box for Add a README file. The README file is essential for cloning and initializing a project.
Click Create the Repository to finalize the process.

### Step 2: Clone the Repository to my local machine and open in VS Code (ALWAYS use Git to clon)
1. Open Windows PowerShell
2. Type: "cd \" to get to the root directory of the current drive. In this case it's C:\ (CD stands for change directory)
3. Copy repo url from GithHub: https://github.com/ssowers2/datafun-04-eda
4. Clone the repo by using git commands and pasting its url in the command line: ```git clone https://github.com/ssowers2/datafun-04-eda```
5. Open VS Code>File>Open Folder>Select the new repo folder (don't double click it)>Click Select Folder 

### Step 3: Add gitignore and requirements.txt files (if starting project from scratch)
1. Create new file in root project folder named: ".gitignore" If the name or location is not exact, it will not work.".gitignore" files are used to keep things out of GitHub like .venv and secrets
2. Find the .gitignore file in the root of this repo and paste the below contents as a starting point. Contents will vary based on the project: 

# This .gitignore file lists content that does NOT need to be tracked in the project history

# Python virtual environment folder
.venv/

# Visual Studio Code settings and workspace folder
.vscode/

# Compiled Python files
__pycache__/

# macOS system files
.DS_Store

# Jupyter Notebook checkpoint files
.ipynb_checkpoints

1. Create new file in root project folder named: "requirements.txt" If the name or location is not exact, it will not work.
2. The contents in this fle will vary but a good starting point for contents is:
   
# requirements.txt - list all the packages the project needs
# In this file, ignore hashes (#) - they are just used to create comments.
# Lines starting with a hash are ignored when installing packages using this file. 

# ======================================================
# IMPORTANT: The contents of this file varies by project 
# ======================================================

# Some common dependencies are provided in this example.
# Comment them in or out as you need them.

# ======================================================
# STEP A - CREATE A LOCAL PROJECT VIRTUAL ENV (.venv)
# ======================================================

# Create your local project virtual environment
# This step ensures you have an isolated Python environment for your project.
# This is typically just done once at the beginning of a project.
# If it gets messed up, we can delete .venv and recreate it at any time. 

# Run the following command to create a virtual environment in the project root.
### On Windows, Use PowerShell (not cmd) - don't include the #:
# py -m venv .venv

### On Mac/Linux, Use zsh or bash (or PowerShell) - don't include the #:
# python3 -m venv .venv

### If VS Code asks: We noticed a new environment has been created. 
# Do you want to select it for the workspace folder?
# Click Yes. 

# ======================================================
# STEP A (ADVANCED OPTION) - ONLY USE IF REQUIRED
# ======================================================

### IMPORTANT: 
### If the project requires a large tool like Apache Kafka or Spark,
### we may need to install an earlier version of Python
### and specify the required version when we create the virtual environment. 
### On Windows, Use PowerShell (not cmd) - don't include the #:
# py -3.11 -m venv .venv
### On Mac/Linux, Use zsh or bash (or PowerShell) - don't include the #:
# python3 -3.11 -m venv .venv

# ======================================================
# STEP B - ALWAYS ACTIVATE THE (.venv) WHEN OPENING A NEW TERMINAL
# ======================================================

# ALWAYS activate the .venv before working on the project.
# Activate whenever you open a new terminal. 

### Windows PowerShell Command (don't include the #):
# .\.venv\Scripts\activate

### Mac/Linux Command (don't include the #):
# source .venv/bin/activate

# Verify: When active, you can usually see (.venv) in the terminal.

# If using a Jupyter notebook, select the kernel associated with your project (.venv).

# ======================================================
# STEP C - INSTALL PACKAGES INTO (.venv) AS NEEDED
# ======================================================

# Install necessary packages listed below with this command:
# Keep packages updated with the most recent versions.

# When you identify a new package you want to use, 
# Just update the list below and re-run this command. 

### Windows Command (don't include the #):
# py -m pip install --upgrade pip setuptools wheel
# py -m pip install -r requirements.txt

### Mac/Linux Command (don't include the #):
# python3 -m pip install --upgrade pip setuptools wheel
# python3 -m pip install --upgrade -r requirements.txt

# When you identify a new package you want to use, 
# Just update the list below and re-run the install command. 

# ======================================================
# VS CODE: Select Interpreter
# ======================================================
# VS Code needs our populated .venv to interpret our files correctly.
# To set the VS Code Interpreter:
# 1. Open the Command Palette: Press Ctrl+Shift+P (Windows/Linux) or Cmd+Shift+P (Mac).
# 2. Search for "Python: Select Interpreter":
# 3. Type Python: Select Interpreter in the Command Palette search bar and select it from the dropdown.
# 4. Choose an Interpreter - A list of available Python environments will appear.
#    Look for the local .venv option.
# 5. Once selected, check the Python version displayed 
#    in the bottom-left corner of the VS Code window in the status bar.

# ======================================================
# ESSENTIAL TOOLS - UNCOMMENT THE NECESSARY ONES BELOW
# ======================================================

# Up-to-date package management tools
pip
setuptools
wheel

# Easy logging for monitoring code execution
loguru

# Environment variables management
python-dotenv

# ======================================================
# TEXT-TO-SPEECH
# ======================================================
# Offline text-to-speech library for Python (1-15 MB)
pyttsx3  

# ======================================================
# JUPYTER (OPTIONAL, NEEDED FOR NOTEBOOKS)
# ======================================================

# Core IPython package that provides an enhanced interactive Python shell (10-15 MB).
ipython

# Core Jupyter functionality required for running notebooks in VS Code (50-60 MB).
jupyter

# Kernel interface for Jupyter notebooks (required for proper kernel registration)
ipykernel

# Interactive widgets (often used in notebooks).
ipywidgets

# ======================================================
# DATA ANALYSIS 
# ======================================================

# Numerical computations and arrays (20-30 MB)
#numpy

# Data manipulation and analysis (built on numpy, 10-20 MB)
#pandas

# ======================================================
# VISUALIZATION
# ======================================================

# Core library for creating visualizations (~30 MB)
matplotlib

# Statistical data visualization library built on matplotlib (~2-5 MB)
seaborn

# Interactive plotting library, often used with Shiny apps (~20-25 MB)
#plotly

# ======================================================
# CONTINUOUS INTELLIGENCE AND INTERACTIVE ANALYTICS
# ======================================================

# Shiny framework for Python applications (~5-10 MB)
#shiny

# ======================================================
# KAFKA STREAMING MESSAGE BROKER INTEGRATION
# ======================================================

# Apache Kafka Python client (~1 MB)
#kafka-python

# ======================================================
# STREAM PROCESSING - CAN BE VERY LARGE
# ======================================================

# Streaming data processing framework (~200-250 MB)
#pyspark<4.0.0

# ======================================================
# MACHINE LEARNING (ML)
# ======================================================

# Core ML library with flexible APIs (~40-50 MB)
#scikit-learn

# ======================================================
# NATURAL LANGUAGE PROCESSING (NLP) - CAN BE VERY LARGE
# ======================================================

# NLP library for text processing (~10 MB core library; downloading corpora can add ~1 GB).
#nltk

# SpaCy: A powerful NLP library ~50 MB (core library; language models + ~300 MB or more per model).
#spacy

### Step 4: git add, git commit -m "Message here", and git push -u orgin main
1. This is a good time to git-add-commit-push changes to the remote repository in GitHub
2. ```git add .```- stages changes, adds files to source control
3. ```git commit -m "Initial commit"```- creates a labeled snapshot of staged changes.
4. ```git push -u origin main``` - updates the remote repository
5. After subsequent changes, I can use a simpler version of the last command: ```git push```

### Step 5: Set Up virtual environment for my local project (ALWAYS create a local virtual environment for project)
FYI: This is typically done once at the beginning of a project. If it gets messed up, delete .venv and recreate it. Never edit .venv directly. Explore the folder but leave the contents alone!
1. Open project repo folder in VS Code
2. Open terminal and make sure it's set to PowerShell
3. Create .venv by typing the command: ```py -m venv .venv```
4. Activate .venv by typing the command. This is for Windows OS: ```.\.venv\Scripts\activate```
5. Select VS Code interpreter to use .venv: Open the command palette (Ctrl Shift P) and search for "Python: Select Interpreter". Then, select the .venv folder in the project root directory.Now my editor will know about the code in my .venv.

### Step 6:  Install dependencies into .venv that are required for the project
## Python Standard Library
We do not need to install packages from the Python Standard Library - they are included with our version. The standard library includes helpful packages like pathlib, sqlite3, os, sys, time, and more. See the index. 

## External Dependencies
External dependencies are libraries, packages, and modules beyond the standard library and include common packages like pandas, numpy, seaborn, and matplotlib. These must be installed into our local project virtual environment to use them in our code. 
1. Open project repository in VS Code. 
2. Open PowerShell terminal.
3. Activate the .venv (if not already): ```.\.venv\Scripts\activate```
4. Install dependencies listed in requirements.txt file using command: ```py -m pip install -r requirements.txt``` 
5. Example to install single dependency: ```pip install requests```
6. Example how to install multiple at once (space between each dependency): ```pip install numpy pandas requests```