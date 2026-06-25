# Customer Churn Prediction System

A data science system designed to identify high-risk telecom subscribers and uncover primary churn drivers using the Telco Customer Churn dataset.

---

## 📌 Project Architecture & Progress Tracking

- [x] **Phase 1: Project Framing & Environment Setup** (Day 1)
- [x] **Phase 2: Data Collection & Understanding** (Day 1)
- [x] **Phase 3: Exploratory Data Analysis (EDA)** (Day 2) ◄ *Current Milestone*
- [ ] **Phase 4: Data Preprocessing & Pipeline Construction** (Upcoming)
- [ ] **Phase 5: Feature Engineering & Selection**
- [ ] **Phase 6: Model Training & Evaluation**
- [ ] **Phase 7: Model Deployment Planning**

---

## 📊 Phase 3: Exploratory Data Analysis (EDA) Insights

During this phase, we conducted Univariate, Bivariate, and Multivariate analyses to uncover structural anomalies and key drivers of customer attrition.

### 🔍 Core Data Findings & Anomalies Isolated
1. **Target Class Imbalance:** The target metric is severely skewed—**73.5% No Churn** vs. **26.5% Churn**. 
2. **The TotalCharges Mismatch:** `TotalCharges` was identified as a text `object` type rather than numeric due to **11 hidden blank string spaces (`" "`)**. This will be programmatically resolved using coercion in Phase 4.
3. **Multicollinearity Flag:** A strong positive linear correlation ($r \approx 0.83$) exists between `tenure` and `TotalCharges`, indicating data redundancy that must be managed during feature selection.

### 💡 Key Business Insights

* **The Month-to-Month Risk:** Customers on short-term Month-to-month contracts exhibit an exponentially higher attrition frequency than those locked into 1 or 2-year commitments.
* **Early Lifecyle Onboarding Friction:** Churn density is heavily clustered between **0 and 6 months**, particularly for customers paying premium rates (>\$75/month) for Fiber Optic lines.
* **Payment Method Friction:** Accounts paying via manual **Electronic Check** show significantly higher churn rates than those using automated card rules or bank transfers.

---

## 🛠️ Workspace Directories

```text
├── data/                             # Raw dataset source files
├── notebooks/
│   ├── 01_data_understanding.ipynb   # Phase 2 Baseline Diagnostics
│   └── 02_exploratory_data_analysis.ipynb # Phase 3 Visualization Pipelines
└── outputs/                          # Saved EDA plot graphics (.png)