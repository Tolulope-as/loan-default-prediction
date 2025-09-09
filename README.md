# 📊 Loan Defaulters Prediction Project  

## 📌 Project Overview  
This project focuses on predicting loan defaulters for a financial institution. Identifying potential defaulters early helps reduce business risks, improve lending strategies, and minimize financial losses.  

The project involves:  
- **Data Preprocessing** – cleaning, encoding categorical variables, scaling numerical features.  
- **Model Training & Evaluation** – comparing multiple machine learning models (Logistic Regression, Decision Tree, Random Forest, XGBoost, LightGBM).  
- **Handling Imbalanced Data** – using **SMOTE** and `scale_pos_weight` to ensure the minority class (defaulters) is well represented.  
- **Model Deployment** – building a user-friendly prediction app with **Streamlit**.  
- **Business Insights** – interactive **Power BI Dashboard** for visual exploration of customer and loan patterns.  

---

## 🧾 Dataset  
The dataset contains customer loan information with the target column:  

- **good_bad_flag** →  
  - `0` = Defaulter (Minority Class)  
  - `1` = Non-Defaulter (Majority Class)  

### Key Features Used:  
 1. bank_account_type 
 2. employment_status_clients
 3. age 
 4. loannumber 
 5. loanamount 
 6. totaldue 
 7. termdays 
 8. good_bad_flag
 9. loan_approval_min 
 10. early_payments 
 11. late_payments
 12. payment_status_score 
 13.  repayment_behaviour_score(RBS) 

---

## ⚙️ Methodology  

1. **Exploratory Data Analysis (EDA)**  
   - Checked distributions, outliers, and missing values.  
   - Built initial visualizations to understand patterns in defaulters vs non-defaulters.  

2. **Preprocessing**  
   - Encoding categorical variables (OneHotEncoder).  
   - Scaling numerical features (StandardScaler).  
   - Balancing classes with **SMOTE**.  

3. **Model Training**  
   Models compared:  
   - Logistic Regression  
   - Decision Tree  
   - Random Forest  
   - XGBoost  
   - LightGBM  

4. **Evaluation Metrics**  
   Since missing a defaulter is more costly than misclassifying a good customer, the focus was on:  
   - **Recall (Sensitivity)** – ability to catch defaulters.  
   - **Precision** – avoid too many false alarms.  
   - **F1-Score** – balance of precision and recall.  
   - Confusion Matrix for class-level insights.  

5. **Deployment**  
   - Saved best model with `joblib`.  
   - Built **Streamlit App** (`app.py`) for loan default prediction.  
   - Exposed user inputs (age, income, loan amount, etc.) to return prediction results.
   - Live link:(https://tolu-defaulters-predictionmodel.streamlit.app/)
6. **Visualization (Power BI)**  
   - Created a dashboard with KPIs:  
     - % of Defaulters vs Non-Defaulters  
     - Loan Term distributions  
     - Age group vs Default rate  
     - Termdays vs Default patterns  
     - Repayment status score impact on defaults  

---

## 📊 Results & Insights  
- **Logistic Regression** gave the highest **F1-score** and recall.  
- Business conclusion: **Recall was prioritized** to minimize the risk of lending to defaulters.  
- SMOTE balancing reduced overall accuracy.  
- Power BI visuals helped uncover patterns such as higher defaults in lower income groups and weaker credit scores.  

---

## 🚀 Deployment  

1. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   streamlit run app.py
   
## Author
- Name:Arowosegbe Tolulope Sarah
- Email: arowosegbetolu8@gmail.com

