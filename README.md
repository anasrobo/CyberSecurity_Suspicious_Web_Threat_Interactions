# Cybersecurity Web Attack Analysis

## Project Overview

This project focuses on analyzing web traffic and cybersecurity attack data to detect suspicious activities and potential attacks using exploratory data analysis (EDA) and machine learning models.

The primary objectives are:

1. **To explore web traffic patterns and identify anomalies.**
2. **To classify cybersecurity threats using machine learning techniques.**
3. **To provide actionable insights into network security.**

# Dataset Used

CloudWatch_Traffic_Web_Attack.csv: Web traffic logs with details like bytes transferred, timestamps, and IP addresses.


Analysis and modeling are conducted in the Jupyter notebook Cyber_Security.ipynb.
Datasets
1. CloudWatch_Traffic_Web_Attack.csv

Description: Contains web traffic logs likely from AWS CloudWatch, aimed at detecting suspicious activities.
Rows: 282
Key Columns:
bytes_in, bytes_out: Data transferred (mean: 1.2M in, 84.5K out).
creation_time, end_time: Timestamps (converted to datetime in analysis).
src_ip, dst_ip: Source and destination IPs.
All columns are non-null; no duplicates found.

## Installation and Dependencies
To run this project, install Python and the following libraries:

```
pandas
matplotlib
seaborn
scikit-learn
tensorflow
joblib
```

#Install via pip:
```
pip install pandas matplotlib seaborn scikit-learn tensorflow joblib
```

# Usage

Clone the Repository:
```
git clone https://github.com/anasrobo/CyberSecurity_Suspicious_Web_Threat_Interactions.git
cd your-repo-name
```

# Upload Datasets:

Place CloudWatch_Traffic_Web_Attack.csv in the project directory.


# Run the Notebook:

Open Cyber_Security.ipynb in Jupyter Notebook or JupyterLab.
Execute cells sequentially to load data, perform EDA, and train models.


# Load Saved Models:

Random Forest: random_forest_model.pkl
Conv1D Neural Network: conv1d_model.keras
Dense Neural Network: dense_model.keras
Example loading:import joblib
from tensorflow.keras.models import load_model
rf_model = joblib.load('random_forest_model.pkl')
conv1d_model = load_model('conv1d_model.keras')
dense_model = load_model('dense_model.keras')

# Analysis and Results
Exploratory Data Analysis (EDA)

Data Loading: Loaded CloudWatch_Traffic_Web_Attack.csv (282 rows, 16 columns).
Overview: 
Shape: (282, 16)
No missing values or duplicates.
Statistical summary showed high variance in bytes_in (max: 25.2M) and bytes_out.


Visualizations: Histogram of bytes_in and bytes_out distributions (plotted with KDE).

## Machine Learning Models

# Random Forest Classifier:
Trained to classify traffic as normal or suspicious.
Saved as random_forest_model.pkl.


# Neural Networks:
Conv1D Model: Sequence-based anomaly detection, 50 epochs, 100% test accuracy.
Dense Model: General classification, also achieved 100% accuracy.
Both saved as .keras files.


# Evaluation: 
Models tested on a subset, showing perfect accuracy (note: small dataset size may affect generalizability).

#Contributing
Contributions are welcome! Fork the repository, make changes, and submit a pull request. Ensure code adheres to PEP 8 standards.

#License
This project is licensed under the MIT License. See the LICENSE file for details.

---

> Built with ❤️ by Anas
