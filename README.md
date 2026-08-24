# AI-Cybersecurity-MachineLearning-Exam
# Machine Learning Exam Project (PGR216)

## Overview
This repository contains my machine learning exam project for PGR216, covering regression pipelines, network intrusion detection, model regularization/dimensionality reduction, and malware image classification using deep learning.

---

## Tasks & Methodology

### 1. Building Energy Efficiency Regression
- **Objective:** Predict Heating Load ($Y_1$) and Cooling Load ($Y_2$) using the UCI Energy Efficiency dataset.
- **Models:** Compared a Linear Regression baseline against a non-linear Random Forest regressor.
- **Key Findings:** Random Forest significantly outperformed Linear Regression, achieving an $R^2$ of $0.998$ for heating load. Cooling load ($Y_2$) proved harder to predict due to higher error margins.

### 2. Network Intrusion Detection (UNSW-NB15)
- **Objective:** Multi-class classification of network traffic and nine attack categories to address severe class imbalance.
- **Approach:** Used Label Encoding for high-cardinality categorical features and trained Random Forest models with class weights and SMOTE.
- **Key Findings:** Standard accuracy hid poor minority-class performance; balancing techniques improved recall for rare attacks like worms, though class scarcity remained challenging.

### 3. Regularization, PCA & Cross-Validation
- **Objective:** Extended the analysis from tasks 1 and 2 by applying Ridge/Lasso regularization, Principal Component Analysis (PCA), and 5-fold cross-validation.
- **Key Findings:** PCA confirmed feature redundancy in the energy dataset (5 components captured 99% variance), but actively degraded performance on the network intrusion dataset where features carried unique information.

### 4. Malware Image Classification (CNN)
- **Objective:** Classify 25 malware families using grayscale images converted from binaries with a custom Convolutional Neural Network (CNN).
- **Approach:** Resized images to $64 \times 64$, applied dropout, and compared a baseline CNN against a class-weighted variant.
- **Key Findings:** The weighted CNN achieved high performance (Balanced Accuracy: $0.946$), though visual similarities between families like Allaple.A and Allaple.L created classification overlap.

---

## Project Structure
- notebooks/        # Jupyter notebooks for each exam task
- data/             # Datasets (UCI Energy, UNSW-NB15, Malimg)
- requirements.txt  # Project dependencies
- README.md         # Project documentation

---

## Tech Stack
- **Language:** Python
- **Libraries:** Scikit-learn, Pandas, NumPy, PyTorch (CNN), Matplotlib, Seaborn

---

## Getting Started

### Prerequisites
Make sure you have Python installed. Clone the repository and install the required dependencies:

git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
pip install -r requirements.txt

### Running the Project
Launch Jupyter Notebook to explore the code and analysis across the individual task files:

jupyter notebook
