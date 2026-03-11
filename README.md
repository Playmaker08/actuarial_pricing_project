# Motor Insurance Pricing Analytics & Simulator

## Project Overview

This project presents an end-to-end motor insurance pricing analysis combining actuarial reasoning, machine learning modeling, and business intelligence visualization. The objective is to understand the key drivers of insurance premiums and develop a predictive pricing model that can estimate premiums for new policy scenarios.

The project analyzes a motor insurance portfolio of nearly 4,000 policies and builds a pricing simulator capable of estimating premiums based on vehicle characteristics and insurance coverage.

The final output includes an interactive **Power BI dashboard** and a **machine learning pricing simulator** that demonstrate how predictive analytics can support underwriting and pricing decisions.

---

## Project Objectives

The project aims to:

- Analyze the structure and exposure of a motor insurance portfolio
- Identify the key factors that influence insurance premium pricing
- Build a predictive model to estimate policy premiums
- Simulate pricing for new insurance policy scenarios
- Present insights through an interactive business dashboard

---

## Dataset

The dataset used in this project contains information about motor insurance policies and vehicle characteristics.

Key variables include:

- **Insurance Type** (Comprehensive / Third Party)
- **Vehicle Type** (Car, Bike, Truck, etc.)
- **Vehicle Make**
- **Vehicle Model**
- **Vehicle Age**
- **Sum Insured**
- **Policy Premium**

The dataset contains approximately **4,000 insurance policies**.

---

## Project Workflow

The project follows a full analytics pipeline:

### 1. Data Cleaning and Preparation
Performed in Python.

Tasks included:
- Handling missing values
- Creating derived variables
- Feature engineering
- Preparing data for modeling

---

### 2. Exploratory Actuarial Analysis

Exploratory analysis was conducted to understand the portfolio structure and pricing patterns.

Key analyses included:

- Premium distribution
- Premium rate analysis
- Premium vs sum insured relationship
- Pricing differences across vehicle types and insurance coverage

The analysis confirmed that premium pricing largely follows a tariff-like structure:

Premium ≈ Premium Rate × Sum Insured

---

### 3. Premium Prediction Model

A machine learning model was developed to estimate policy premiums based on vehicle and policy characteristics.

Features used include:

- Insurance Type
- Vehicle Type
- Vehicle Make
- Vehicle Model
- Vehicle Age
- Sum Insured

The model was trained using Python and evaluated using standard regression metrics.

---

### 4. Pricing Simulator

The trained model was used to simulate premiums for new policy scenarios.

The simulator predicts:

- **Predicted Premium**
- **Premium Rate**
- **Risk Tier classification**

Risk tiers were defined relative to the portfolio average premium rate:

- Low Risk
- Medium Risk
- High Risk

This allows underwriters to quickly benchmark simulated policies against the existing portfolio.

---

### 5. Business Intelligence Dashboard

An interactive **Power BI dashboard** was developed to communicate the results.

The dashboard consists of four pages:

#### Page 1 – Portfolio Overview
Provides a high-level view of the insurance portfolio including:

- Total policies
- Average premium
- Average premium rate
- Premium distribution
- Premium rate comparison across segments

#### Page 2 – Pricing Structure Analysis
Explores the factors that drive premium levels:

- Premium vs insured value
- Premium contribution by vehicle segment
- Premium ranking by vehicle model
- Pricing segmentation by vehicle type and coverage

#### Page 3 – Portfolio Exposure Analysis
Examines how risk exposure is distributed within the portfolio:

- Policy count by vehicle type
- Policy count by insurance type
- Exposure by vehicle manufacturer
- Vehicle age distribution

#### Page 4 – Pricing Simulation Results
Demonstrates the application of the pricing model:

- Predicted premium scenarios
- Risk tier distribution
- Premium benchmarking vs portfolio average
- Simulated policy comparison

---

## Key Insights

Several important insights emerged from the analysis:

### 1. Insurance Coverage Drives Pricing
Comprehensive policies generate significantly higher premiums than third-party policies due to broader coverage.

### 2. Vehicle Value is a Primary Pricing Driver
Premium levels scale almost linearly with the insured value of the vehicle.

### 3. Premium Distribution is Highly Skewed
A small number of high-value policies contribute disproportionately to total premium revenue.

### 4. Portfolio Exposure is Concentrated
Policy exposure is concentrated among certain vehicle types and manufacturers, suggesting potential concentration risk.

### 5. Machine Learning Enables Pricing Simulation
The predictive model allows insurers to estimate premiums for new policy scenarios and evaluate pricing relative to the existing portfolio.

---

## Tools and Technologies

- **Python**
- Pandas
- NumPy
- Scikit-learn

- **Power BI**
- Data visualization
- Dashboard development

---

## Project Structure

Motor-Insurance-Pricing-Analytics/
│
├── data/
│ └── motor_insurance_dataset.csv
│
├── notebooks/
│ ├── 01_data_cleaning.ipynb
│ ├── 02_actuarial_eda.ipynb
│ ├── 03_premium_modeling.ipynb
│ └── 04_pricing_simulator.ipynb
│
├── dashboard/
│ └── actuarial_pricing_dashboard.pbix
│ └── actuarial_pricing_dashboard.pdf
│
└── README.md

---

## Business Value

This project demonstrates how insurance companies can combine actuarial analysis, machine learning, and data visualization to support pricing decisions.

The pricing simulator provides a practical framework for evaluating new policies and benchmarking them against existing portfolio pricing structures.

---

## Future Improvements

Potential extensions include:

- Incorporating claims data for loss modeling
- Building frequency and severity models
- Implementing GLM-based actuarial pricing models
- Developing a real-time pricing API
- Integrating the pricing simulator into underwriting systems

---

## Author

This project was developed as part of a data analytics portfolio demonstrating actuarial analysis, machine learning, and business intelligence skills in insurance pricing.
