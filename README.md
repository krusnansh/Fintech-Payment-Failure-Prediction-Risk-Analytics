Fintech Payment Failure Prediction & Risk Analytics
Analyze fintech payment failures, identify operational and customer-level risk drivers, and prepare the dataset for machine learning-based failure prediction using Alteryx.


| Business Question | Key Result |
|---|---|
| **How big is the payment failure problem?** | **971 of 9,754 transactions failed (9.95%)**, with **₹6.43M** in failed transaction value. |
| **Where are failures concentrated?** | Failure rates were analyzed across **payment gateways, issuer banks, and payment methods**. Cashfree had the highest gateway failure rate at **11.10%**. |
| **Which customer segments are riskier?** | **Low-balance customers had a 15.31% failure rate**, compared with **7.04% for high-balance customers**. |
| **Does retrying indicate higher failure risk?** | Failure rate increased from **9.16% with 0 retries** to **13.39% with 2 retries**, before declining to **11.68% at 3 retries**. |
| **Why do payments fail?** | Root causes included **Timeout (190)**, **Bank server down (162)**, **Limit exceeded (142)** and **OTP failure (98)**. |

Data Cleaning & Preparation
The dataset was cleaned and validated before analysis. The workflow includes data-type handling, timestamp parsing, missing-value treatment, duplicate detection, validation rules, and data-quality flags.

<img width="1097" height="357" alt="data cleaning workflow" src="https://github.com/user-attachments/assets/fda956af-a25f-46ef-8ccd-137c726ec663" />

Key preparation steps included:
- 9,754 unique transactions retained after duplicate detection
- 246 duplicate records identified
- Validation checks for amount, email, phone, PAN, pincode, IP address, and business-rule exceptions
- Creation of payment failure and failed transaction value fields for analysis

AI-Assisted Data Standardization
Alteryx Precision Match was used to standardize inconsistent categorical values across city, issuer_bank, and payment_gateway. LLM Override was used to provide the AI model connection for the Precision Match tools.

<img width="737" height="250" alt="Before Precision Match " src="https://github.com/user-attachments/assets/09550778-a4bd-45e8-b6eb-492cfe543203" />

Examples of inconsistent values included variations such as bangalore, hdfc, and kotak.

<img width="723" height="208" alt="After Precision Match" src="https://github.com/user-attachments/assets/c67c923f-b812-4b0b-8d32-3f23b024dce0" />

These were standardized into consistent values such as Bengaluru, HDFC Bank, and Kotak Mahindra Bank.

Analysis Workflow
The analysis was structured around five business questions:
Overall Payment Failure → Failure Concentration → Customer & Transaction Risk → Retry Behavior → Failure Root Causes

<img width="1308" height="437" alt="Insights" src="https://github.com/user-attachments/assets/b43934be-700c-4081-81f1-a498278a9331" />


Tools Used
Alteryx Designer, Input Data, Select, Data Cleansing, Unique, Formula, Summarize, Join, Browse, LLM Override, Precision Match.

Current Status
Completed: Data cleaning, validation, duplicate handling, AI-assisted standardization, and business analysis.
