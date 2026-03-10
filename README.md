Motor Insurance Pricing Analytics
An Actuarial Data Science Project
This project develops a data-driven actuarial pricing analytics framework to analyze and model motor insurance premiums using vehicle and policy risk characteristics.
Using a portfolio of motor insurance policies, the analysis investigates how observable attributes such as vehicle type, insured value, insurance coverage type, vehicle make, and vehicle age influence premium levels. The project combines actuarial exploratory analysis, predictive modeling in Python, and an executive dashboard in Power BI to generate insights that support pricing and portfolio segmentation decisions.
Project Objectives
The primary objective of this project is to build an interpretable actuarial pricing framework that explains how motor insurance premiums vary across policy and vehicle characteristics.
Specifically, the project aims to:
Analyze how insurance premiums differ across vehicle types, insurance coverage types, and manufacturers
Examine the relationship between insured value and premium levels
Identify key rating factors that influence premium variation
Engineer actuarial pricing metrics such as vehicle age and premium rate
Develop predictive models capable of estimating motor insurance premiums
Translate findings into business insights through an interactive Power BI dashboard
Actuarial Business Problem
Motor insurers must differentiate premiums across policyholders based on risk characteristics while maintaining consistency and transparency in their pricing structures.
This project addresses the actuarial pricing problem of determining:
How observable vehicle and policy characteristics influence motor insurance premiums, and whether these characteristics can be used to construct a consistent and interpretable pricing framework.
While traditional actuarial ratemaking relies on claims experience and exposure data, this dataset focuses on premium outcomes and policy characteristics, allowing us to analyze how current premiums reflect observable risk factors.
The goal is therefore not to estimate losses or reserves, but rather to:
understand the structure of premium differentiation
evaluate risk segmentation across policyholders
build a predictive model to estimate premiums
provide pricing insights for underwriting and portfolio management
Dataset
The dataset used in this project is a Motor Insurance Dataset containing approximately 4,000 policies.
Each record represents a motor insurance policy with information about the vehicle, insurance coverage, and premium charged.
Key Variables
Variable	Description
INSURANCE TYPE	Insurance coverage type (Comprehensive, Third Party)
VEHICLE TYPE	Type of vehicle (Car, Bike, Truck)
VEHICLE USE	Usage of vehicle
VEHICLE MAKE	Vehicle manufacturer
VEHICLE MODEL	Vehicle model
VEHICLE MAKE YEAR	Manufacturing year of the vehicle
SUM INSURED	Total insured value of the vehicle
POLICY PREMIUM	Annual premium charged
Dataset Size
~4,000 policies
8 variables
Key Analytical Questions
This project explores several actuarial pricing questions:
Portfolio Overview
What is the distribution of premiums across the portfolio?
How does the insured value vary across policies?
Which insurance types dominate the portfolio?
Risk Segmentation
How do premiums differ across vehicle types?
Are certain manufacturers or models priced higher?
Does vehicle age influence premium levels?
How does the premium rate differ across policy segments?
Pricing Structure
Is premium proportional to sum insured?
Which factors appear to drive premium variation?
Are there segments that appear overpriced or underpriced relative to others?
Predictive Modeling
Can we predict policy premiums using vehicle and policy characteristics?
Which variables are the strongest drivers of premium predictions?
Methodology
The project follows a structured actuarial analytics workflow.
1. Data Preparation
Data loading and cleaning
Handling categorical variables
Feature engineering
Creation of derived actuarial variables
Key engineered features include:
Vehicle Age
vehicle_age = current_year - vehicle_make_year
Premium Rate
premium_rate = policy_premium / sum_insured
These features allow us to analyze pricing intensity and vehicle risk characteristics.
2. Exploratory Actuarial Analysis
Exploratory analysis focuses on identifying premium patterns across risk factors, including:
Premium distribution
Premium by insurance type
Premium by vehicle category
Premium vs insured value
Premium rate segmentation
Visualization tools include:
distribution plots
boxplots
segment comparison charts
correlation analysis
3. Predictive Modeling
Predictive models are developed to estimate policy premiums based on observable features.
Models evaluated include:
Linear Regression
Random Forest Regressor
Gradient Boosting / XGBoost
The goal is not only predictive accuracy but also interpretability of premium drivers.
Key outputs include:
model performance metrics
feature importance rankings
insights into pricing factors
4. Executive Dashboard
To translate analytical results into business insights, an interactive Power BI dashboard was developed.
The dashboard includes several analytical views:
Portfolio Overview
Total policies
Average premium
Average insured value
Premium distribution
Risk Segmentation
Premium by vehicle type
Premium by insurance type
Premium by vehicle manufacturer
Premium by vehicle age
Pricing Insights
Premium vs insured value relationship
Premium rate comparisons across segments
Key drivers of premium variation
The dashboard is designed to support management-level decision making and pricing strategy discussions.
Project Structure
actuarial-motor-insurance-pricing/

data/
    raw/
        motor_insurance_dataset.csv

notebooks/
    01_data_cleaning.ipynb
    02_actuarial_eda.ipynb
    03_premium_modeling.ipynb

dashboard/
    motor_insurance_dashboard.pbix

images/

README.md
Tools and Technologies
Programming
Python
Libraries used:
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
Data Visualization
Power BI
Features used:
interactive filters
KPI cards
segmentation visuals
premium distribution charts
Key Insights
Key findings from the analysis include:
Insurance type is a major pricing driver, with comprehensive policies commanding substantially higher premiums than third-party coverage.
Insured value strongly correlates with premium levels, reflecting value-based pricing practices.
Premiums differ across vehicle categories and manufacturers, suggesting implicit risk segmentation in pricing.
Vehicle age influences pricing, though its effect varies depending on vehicle type and coverage.
Predictive models demonstrate that a combination of vehicle attributes and insured value can explain a substantial portion of premium variation across policies.
Limitations
This dataset does not contain:
claims
accident history
loss amounts
exposure duration
Therefore, the project cannot estimate:
loss ratios
pure premiums
actuarial reserves
technical profitability
The analysis instead focuses on observed premium structure and pricing behavior, rather than full actuarial ratemaking based on claims experience.
Future Improvements
Several extensions could further enhance the project:
Incorporating claims and loss data to perform full actuarial ratemaking
Applying GLM models commonly used in actuarial pricing
Using SHAP or explainable AI techniques to interpret pricing drivers
Expanding the dataset to include driver demographics and accident history
Author
Andy Nguyen
Business Analytics & Economics
DePauw University
Interests:
Actuarial Analytics
Financial Data Science
Risk Modeling
Insurance Pricing
Key drivers of premium variation
The dashboard is designed to support management-level decision making and pricing strategy discussions.
