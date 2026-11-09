
# Solar Power Generation Prediction and Anomaly Detection Dashboard Using Machine Learning

An end-to-end Machine Learning web application designed to predict solar power generation and detect operational anomalies in solar power plants.

---

## 📌 Project Overview

This project is developed by a team of four college students to analyze solar plant generation and sensor data. The system aims to:
1. **Predict Solar Power Generation**: Estimate DC/AC power outputs based on weather sensor metrics and historical trends using regression algorithms.
2. **Detect Plant Anomalies**: Identify underperforming inverters, faulty solar panels, or equipment sensor abnormalities using anomaly detection / classification techniques.
3. **Interactive Visual Dashboard**: Provide operators with an interactive dashboard powered by a Flask backend and dynamic Chart.js charts.

### 📊 Dataset Source
- **Kaggle**: [Solar Power Generation Data](https://www.kaggle.com/datasets/anikannal/solar-power-generation-data)

---

## 🛠️ Technology Stack

| Layer | Technologies |
| :--- | :--- |
| **Data Processing & Analysis** | Python, Pandas, NumPy |
| **Machine Learning** | Scikit-learn, Joblib |
| **Backend API** | Flask, Flask-CORS |
| **Frontend UI** | HTML5, CSS3, Modern JavaScript (Fetch API) |
| **Data Visualization** | Chart.js, Matplotlib / Seaborn (for EDA) |

---

## 📂 Project Structure & Folder Purpose

Below is the directory structure organized for clean separation of concerns:

```text
project/
├── dataset/
│   ├── raw/                  # Original, unmodified Kaggle dataset files
│   └── processed/            # Cleaned, transformed, and feature-engineered datasets
├── notebooks/                # Jupyter Notebooks for EDA, experiments, and training
├── models/                   # Saved ML models, scalers, and encoders (.pkl / .joblib)
├── backend/                  # Flask application, routing, and ML prediction services
├── frontend/                 # Client-side UI (HTML, CSS, JS scripts, Chart.js configs)
├── reports/                  # Project documentation, figures, evaluation summaries
├── .gitignore                # Git ignore rules for virtual environments and caches
├── requirements.txt          # Python project dependencies
└── README.md                 # Project documentation and setup guide
```

### Purpose of Each Folder:

- **`dataset/raw/`**:
  - Stores the original CSV files directly downloaded from Kaggle.
  - **Rule**: These files should remain strictly read-only and never be modified directly.

- **`dataset/processed/`**:
  - Stores datasets generated after data cleaning, handling missing values, date-time formatting, feature scaling, or merging generation and sensor readings.

- **`notebooks/`**:
  - Contains Jupyter Notebooks (`.ipynb`) used for step-by-step Exploratory Data Analysis (EDA), data visualization, hypothesis testing, and model comparison.

- **`models/`**:
  - Stores trained and serialized model artifacts (e.g., Random Forest, Gradient Boosting, or Linear Regression models saved via `joblib` or `pickle`), along with any feature scalers (e.g., `StandardScaler`).

- **`backend/`**:
  - Houses the Flask web server (`app.py`), API endpoints (e.g., `/api/predict`, `/api/anomalies`, `/api/historical`), and server-side business logic for handling user input and running inference.

- **`frontend/`**:
  - Contains all user-interface files:
    - HTML templates for layout and dashboard structure
    - CSS stylesheets for responsive, modern UI design
    - JavaScript modules utilizing `Fetch API` to communicate with the Flask API and `Chart.js` for interactive data visualization.

- **`reports/`**:
  - Dedicated to college project deliverables: exported charts, confusion matrices, evaluation metrics (MAE, RMSE, $R^2$), slides, project reports, and documentation.

---

## 🚀 Beginner-Friendly Setup & Execution Guide

Follow these steps to get your environment ready:

### 1. Prerequisites
- Install **Python 3.8+** (recommended Python 3.10 or 3.11).
- Ensure `pip` is updated (`python -m pip install --upgrade pip`).

---

### 2. Set Up a Virtual Environment

Creating a virtual environment ensures everyone on the team has identical package versions without conflicts.

#### On Windows (PowerShell or Command Prompt):
```powershell
# Navigate to the project root directory
cd project

# Create a virtual environment named 'venv'
python -m venv venv

# Activate the virtual environment
.\venv\Scripts\activate
```

#### On macOS / Linux:
```bash
# Navigate to the project root directory
cd project

# Create a virtual environment
python3 -m venv venv

# Activate the virtual environment
source venv/bin/activate
```

*(You will see `(venv)` prepended to your terminal prompt once activated.)*

---

### 3. Install Dependencies

Install all required Python packages with a single command:
```bash
pip install -r requirements.txt
```

---

### 4. Adding the Dataset
1. Download the dataset from [Kaggle: Solar Power Generation Data](https://www.kaggle.com/datasets/anikannal/solar-power-generation-data).
2. Extract the downloaded CSV files into the **`dataset/raw/`** folder.
3. *Do not rename columns or modify the raw files.*

---

### 5. Running the Workflow (When Developed)

- **Step A: Exploratory Data Analysis & Model Training**
  - Launch Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
  - Open the notebooks in `notebooks/` to clean data, train models, and export trained models to the `models/` directory.

- **Step B: Running the Flask Backend & Dashboard**
  - Run the Flask server:
    ```bash
    python backend/app.py
    ```
  - Open your browser and navigate to `http://127.0.0.1:5000` to interact with the dashboard.

---

## 👥 Team Collaboration Guidelines

1. **Modular Work**: Assign modules cleanly among team members:
   - *Member 1*: Data Ingestion, Cleaning & Preprocessing (`dataset/`, `notebooks/`)
   - *Member 2*: Machine Learning Model Training & Evaluation (`notebooks/`, `models/`)
   - *Member 3*: Flask Backend & REST API Development (`backend/`)
   - *Member 4*: Frontend Dashboard, Fetch API & Chart.js Visualizations (`frontend/`)
2. **Never commit large generated files or virtual environment folders**: The `.gitignore` is already configured to keep your repository clean.

=======
# solar-power-prediction

