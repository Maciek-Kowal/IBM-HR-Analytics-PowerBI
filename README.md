\# HR Attrition Risk Analytics: From Historical Data to Predictive Retention



!\[Power BI](https://img.shields.io/badge/Power\_BI-F2C811?style=for-the-badge\&logo=powerbi\&logoColor=black)

!\[Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge\&logo=python\&logoColor=white)

!\[scikit-learn](https://img.shields.io/badge/scikit\_learn-F7931E?style=for-the-badge\&logo=scikit-learn\&logoColor=white)

!\[Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge\&logo=pandas\&logoColor=white)



\## Executive Summary

This project provides a complete analytics ecosystem designed to transition HR departments from reactive reporting to proactive retention. By integrating descriptive analytics (Power BI) with a predictive machine learning model (Python), the solution identifies which employees are most likely to leave and provides actionable data to mitigate turnover costs.



\### Quick Links

\- \[View Executive Presentation (PDF)](docs/HR\_Attrition\_Risk\_Analytics\_Presentation.pdf)



\## Project Walkthrough



\### 1. Diagnostic Analytics: Understanding the Cost of Turnover

Before predicting the future, we must quantify the current state. The Power BI dashboard analyzes historical data to identify where the company is losing money.

\- Identified a 16.12% historical attrition rate generating $6.81M in estimated turnover costs.

\- Highlighted that Sales Representatives generate the highest attrition costs and pinpointed a critical tenure spike at the 1-year mark.



!\[Power BI Overview](docs/Images/Dashboard1.png)



\*Interactive Tooltip showcasing granular data on hover:\*

!\[Power BI Tooltip](docs/Images/Dashboard2.png)



\### 2. Predictive Analytics: The Machine Learning Engine

To shift from reporting to prevention, a predictive model was developed using Python and scikit-learn. 

\- Model: Random Forest Classifier.

\- Handling Imbalance: Applied SMOTE to correctly identify the minority class (leavers).

\- Business Calibration: The decision threshold was custom-tuned to 0.30 to prioritize recall. This ensures the model catches 68% of all potential leavers, favoring early intervention over strict precision.



!\[Python Model Code](docs/Images/Python.png)



\### 3. Actionable Output: The HR Retention List

Managers do not need complex probability matrices; they need a clear list of targets. The final output of the Python pipeline is a clean, automated report filtered for high-risk profiles.

\- Combines predictive risk scores with original demographic data.

\- Filters for employees with a >30% flight risk.

\- Strips away technical modeling columns to deliver a ready-to-use list for HR outreach.



!\[Clean HR Report](docs/Images/Excel.png)



\### 4. Executive Presentation

All technical findings and business recommendations were synthesized into a concise executive summary presentation for stakeholders.



!\[Executive Presentation](docs/Images/Powerpoint.png)



\## Repository Structure

\- /data: Contains the original dataset and the final exported High-Risk Report.

\- /notebooks: Contains the documented Jupyter Notebook (HR\_Attrition\_Predictive\_Model.ipynb) with the full ML pipeline.

\- /docs: Contains the Executive Summary PDF and project screenshots.

\- / (Root): Power BI project files (.pbip, .Report, .SemanticModel).



\## How to Use

1\. Clone the repository.

2\. To view the descriptive analytics, open HR\_Attrition\_Dashboard.pbip in Power BI Desktop.

3\. To run the predictive pipeline, open the Jupyter Notebook in /notebooks, install the required libraries (pandas, scikit-learn, imblearn), and execute the cells to generate a fresh Clean\_HR\_Risk\_Report.xlsx in the /data directory.

