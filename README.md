# Fintech-New-Features-Launch-Transactions-Analysis (Work in Progress)
**Objective:**  
Evaluate the impact of launching a **QR Code payment feature** on customer engagement by comparing user behavior **before and after the release**. The project integrates multiple data sources, prepares analytical features, and measures changes in key metrics such as transaction frequency, active users, basket size, and recurrence. The final outcome is to generate actionable insights and recommendations on how the feature affects adoption and user engagement.


# QR Code Feature Impact Analysis

## Dataset
- **Name:** Financial Transactions Dataset: Analytics ([kaggle.com](https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets?utm_source=chatgpt.com))  
- **Source:** Kaggle — *computingvictor/transactions-fraud-datasets*  
- **Description:** Synthetic financial transactions designed for analytics including fraud detection, customer behavior and expense forecasting.  

## Objective
Evaluate the impact of launching a **QR Code payment feature** on user engagement, by comparing behavior **before vs. after** the feature release. Use data from multiple tables to engineer engagement metrics and generate actionable insights.

## Data Tables Available
- `users_data.csv` — demographics & financial profiles of users  
- `cards_data.csv` — card attributes  
- `transactions_data.csv` — transaction logs (timestamp, amount, merchant, MCC, etc.)  
- `train_fraud_labels.json` — fraud labels (optional, mainly for fraud detection)  
- `mcc_codes.json` — mapping of merchant category codes  

## Phases & Backlog
1. **Exploratory Data Analysis (EDA)**  
   - Understand table shapes/types  
   - Check nulls, duplicates, outliers  
   - Define `LAUNCH_DATE` and pre/post windows  

2. **Data Merge**  
   - Join tables (transactions ↔ users, cards, MCC)  
   - Validate join quality (match rates, missing keys)  

3. **Data Transformation**  
   - Parse dates, normalize amounts  
   - Create engagement features (frequency, amounts, diversity, recurrence)  
   - Flag periods (`pre` / `post`)  

4. **Engagement Analysis**  
   - Compute metrics (active users, tx/user, average ticket, etc.) pre vs post  
   - Segment by merchant categories, value bands  

5. **Insight Generation & Storytelling**  
   - Key findings + hypotheses  
   - Recommendations and limitations  

## What We’ve Done So Far
- Converted string-fields (`$`-formatted) to numeric types  
- Created `has_error` flag → ~1.6% transactions with error, ~98.4% without  
- Visualized missing data in `transactions` (merchant_city, mcc, zip have missing values)  

## Next Steps
- Finalize EDA deliverables  
- Perform data merge  
- Transform data for engagement metrics  
- Conduct pre/post analysis for QR Code feature (once `LAUNCH_DATE` set)  
- Generate insights and prepare executive summary  

## Project Management
This project is tracked via GitHub Projects:  
👉 [Project Board — QR Code Feature Impact Analysis](https://github.com/users/ana-nobre/projects/6)  

## Deliverables
- Data quality issues list + EDA notes  
- Unified analytic DataFrame ready for metrics  
- Comparison plots and tables (pre vs post)  
- Actionable insights report  

## Reference
- "Financial Transactions Dataset: Analytics", Kaggle — computingvictor/transactions-fraud-datasets ([kaggle.com](https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets?utm_source=chatgpt.com))  
