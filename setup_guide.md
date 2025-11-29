# 📘 Complete Setup Guide for Beginners

## Table of Contents
1. [Environment Setup](#environment-setup)
2. [Installing Python](#installing-python)
3. [Project Setup](#project-setup)
4. [Running the Analysis](#running-the-analysis)
5. [Troubleshooting](#troubleshooting)

---

## Environment Setup

### Step 1: Check Python Installation
Open your terminal/command prompt and type:
```bash
python --version
```

You should see Python 3.8 or higher. If not, proceed to install Python.

### Step 2: Installing Python (if needed)

**Windows:**
1. Go to https://www.python.org/downloads/
2. Download Python 3.11 (recommended)
3. Run installer
4. ✅ CHECK "Add Python to PATH"
5. Click "Install Now"

**Mac:**
```bash
brew install python@3.11
```

**Linux:**
```bash
sudo apt update
sudo apt install python3.11 python3-pip
```

---

## Project Setup

### Step 1: Create Project Folder
```bash
mkdir shipping-events-analysis
cd shipping-events-analysis
```

### Step 2: Create Virtual Environment
**Why?** Keeps project dependencies isolated.

```bash
# Create virtual environment
python -m venv venv

# Activate it
# On Windows:
venv\Scripts\activate

# On Mac/Linux:
source venv/bin/activate
```

You should see `(venv)` in your terminal prompt.

### Step 3: Create Project Structure
```bash
# Create folders
mkdir data notebooks src outputs
mkdir outputs/figures outputs/reports

# Create files
touch README.md requirements.txt setup_guide.md
touch src/__init__.py src/data_loading.py
touch src/data_cleaning.py src/visualizations.py
```

### Step 4: Install Dependencies
Create `requirements.txt` with the dependencies listed above, then:

```bash
pip install -r requirements.txt
```

This will take 2-5 minutes.

---

## Running the Analysis

### Step 1: Create Jupyter Notebook
```bash
jupyter notebook
```

This opens in your browser. Create new notebook: notebooks/shipping_analysis.ipynb

### Step 2: Load the Data
In the first cell:
```python
from datasets import load_dataset
import pandas as pd

# Load dataset
ds = load_dataset("happyhackingspace/shipping-events-eu")
dataset = ds["train"]
df = dataset.to_pandas()

print(f"Dataset loaded: {len(df)} rows")
df.head()
```

### Step 3: Explore the Data
```python
# Basic info
print(df.info())
print(df.describe())

# Check for missing values
print(df.isnull().sum())
```

---

## Troubleshooting

### Issue: "python: command not found"
**Solution:** Python not installed or not in PATH
- Reinstall Python with "Add to PATH" checked

### Issue: "pip: command not found"
**Solution:** Try `python -m pip` instead of `pip`

### Issue: "ModuleNotFoundError"
**Solution:** Make sure virtual environment is activated
```bash
# Check if (venv) is in prompt
# If not, activate it:
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate   # Windows
```

### Issue: Jupyter won't open
**Solution:** 
```bash
pip install jupyter --upgrade
python -m jupyter notebook
```

---

## Next Steps
1. ✅ Complete setup
2. 📊 Load and explore data
3. 🧹 Clean the data
4. 📈 Create visualizations
5. 📝 Document findings

Need help? Create an issue on GitHub!