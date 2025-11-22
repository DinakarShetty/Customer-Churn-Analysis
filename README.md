# 📊 Telecom Customer Churn Analysis

This project analyzes customer churn for a telecom company using the **Telco Customer Churn** dataset.  
The goal is to understand **why customers leave**, identify high-risk groups, and suggest **data-driven actions** to reduce churn.

---

## 🚀 Executive / Dashboard Summary

- Overall churn rate is **~26.5%** – more than **1 in 4 customers** leave the service.  
- **Tenure is critical**:  
  - Over **50% of churned customers** have tenure **less than 1 year**.  
  - Customers with **more than 2 years** tenure have churn rates **below 10%**.  
- **Contract type** strongly influences churn:  
  - **Month-to-month contracts** contribute to **~90% of total churn**.  
  - **One-year and two-year contracts** show churn of only **~10–12%**.  
- **Service-related features** (OnlineSecurity, OnlineBackup, TechSupport, DeviceProtection, StreamingTV, StreamingMovies) are key drivers:  
  - Customers **without** these services churn at **2–3× higher rates** than those who have them.  
  - Example:  
    - **OnlineSecurity = No → ~30% churn**  
    - **OnlineSecurity = Yes → ~15% churn**  
- **Internet and payment behavior**:  
  - **Fiber-optic users** churn at around **~40–45%**, higher than **DSL users (~18%)**.  
  - Customers paying via **Electronic Check** have the highest churn (**~45%**), while **automatic payments (credit card / bank transfer)** show much lower churn (**~15–18%**).

### 🎯 Key Business Takeaways

1. **New & month-to-month customers** are the most vulnerable; retention campaigns should focus here.  
2. Promote **1–2 year contracts** and **AutoPay payment methods** to reduce churn.  
3. Design bundled offers around **OnlineSecurity, TechSupport, and other add-on services**, as they correlate with higher retention.  
4. Revisit pricing, experience, or support for **fiber-optic plans**, which show elevated churn.

---

## 📂 Project Structure

- `Telecom customer churn analysis.ipynb` – main analysis notebook with data cleaning, EDA, and visualizations.
- `Telco_Customer_Churn.csv` – source dataset (not included here if under license; download from Kaggle or official source).
- (Optional) `plots/` – exported chart images for use in reports / presentations.

---

## 🧹 Data Preparation

Main preprocessing steps in the notebook:

- Replaced blank values in `TotalCharges` with **0** for customers with **0 tenure**.
- Converted `SeniorCitizen` from **0/1** to **No/Yes** for better readability.
- Ensured correct data types for numerical and categorical variables.
- Handled categorical variables such as:
  - `PhoneService`, `MultipleLines`, `InternetService`
  - `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`
  - `StreamingTV`, `StreamingMovies`, `Contract`, `PaymentMethod`, etc.

---

## 📈 Visualizations / Dashboard Elements

The notebook includes several key plots (many arranged as subplots):

- **Churn distribution** (pie / bar chart).  
- **Churn vs Tenure** – shows higher churn for newer customers.  
- **Churn by Contract type** – highlights risk in month-to-month contracts.  
- **Churn by InternetService** (DSL, Fiber optic, No internet).  
- **Churn vs Service features** – grouped plots for:  
  - `PhoneService`, `MultipleLines`, `InternetService`  
  - `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`  
  - `StreamingTV`, `StreamingMovies`  
- **Churn by PaymentMethod** – especially Electronic Check vs other methods.  

These charts together act like a **visual dashboard**, helping stakeholders quickly understand where churn is concentrated.

---

## 🛠 Tech Stack

- **Language:** Python  
- **Libraries:**  
  - Data: `pandas`, `numpy`  
  - Visualization: `matplotlib`, `seaborn`  
  - Environment: Jupyter Notebook

---

