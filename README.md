# 📦 EU Shipping Events Analysis

## Project Overview
This project analyzes shipping and delivery data across European countries to identify patterns in delivery performance, delays, and common issues. The analysis aims to provide actionable insights for improving logistics operations.

## 🎯 Business Questions
1. What is the average delivery time by carrier and service type?
2. Which routes experience the most delays?
3. What are the common causes of delivery failures?
4. How does shipping cost correlate with delivery performance?
5. Which regions have the highest rate of customs issues?

## 📊 Dataset Information
- **Source**: HuggingFace - happyhackingspace/shipping-events-eu
- **Records**: 45,649 shipping events
- **Features**: 33 columns including delivery status, timing, location, and issue flags
- **Period**: Historical EU shipping data

## 🛠️ Technologies Used
- Python 3.8+
- pandas - Data manipulation
- matplotlib & seaborn - Visualization
- datasets (HuggingFace) - Data loading
- jupyter - Interactive analysis

## 📁 Project Structure
```
shipping-events-analysis/
├── README.md
├── requirements.txt
├── setup_guide.md
├── data/
│   └── .gitkeep
├── notebooks/
│   └── shipping_analysis.ipynb
├── src/
│   ├── __init__.py
│   ├── data_loading.py
│   ├── data_cleaning.py
│   └── visualizations.py
├── outputs/
│   ├── figures/
│   └── reports/
└── .gitignore
```

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- pip package manager
- 2GB free disk space

### Installation Steps
1. Clone the repository
```bash
git clone https://github.com/yourusername/shipping-events-analysis.git
cd shipping-events-analysis
```

2. Create virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Run the analysis
```bash
jupyter notebook notebooks/shipping_analysis.ipynb
```

## 📈 Key Findings
*(To be updated after analysis)*

## 👤 Author
Salih Bulut

## 📝 License
This project is open source and available under the MIT License.
