NGO Donations Analytics | Excel Dashboard & SQL Analysis

A fundraising performance analysis project using Microsoft Excel and SQL.

By: Mariam Abdullateef
Date: November 2026

1. Project Overview

Analysed 4,998 NGO donation records using Excel and SQL to evaluate fundraising performance, explore donor contributions, compare regional and project performance, and assess funding against assigned budgets.

The project demonstrates how data analysis can help nonprofit organisations understand fundraising performance, identify contribution patterns and support evidence-based decision-making.

2. Business Questions

The analysis was designed to answer the following questions:

1. What was the total amount raised compared with the overall fundraising budget?
2. How did donations change across the years?
3. Which region contributed the highest amount?
4. Which donor type contributed the most?
5. Which donor made the highest contribution?
6. Which assignment received the highest funding?
7. Was there a relationship between assignment budget and impact score?
8. What was the average donation amount?
   
3. Dataset Description

The project used three separate CSV files obtained from the Kaggle Charity Donations dataset by Ronak Badhe.

Dataset Source: Kaggle – Charity Donations Dataset

The datasets were organised into three tables:

1. Donations Table (donations.csv)

* Donation date
* Donation amount
* Donor ID
* Assignment ID

2. Donors Table (donors.csv)

* Donor name
* Donor type
* Region

3. Assignments Table (assignments.csv)

* Assignment name
* Budget
* Region
* Impact score

The three CSV files were imported into SQL and connected using JOIN operations through donor ID and assignment ID.

This enabled analysis across donation transactions, donor contributions and assignment funding performance

Assignments Table

* Assignment name
* Budget
* Region
* Impact score

The tables were connected using donor ID and assignment ID to support combined analysis.

Dataset source: [[Kaggle – Charity Donations Dataset](https://www.kaggle.com/datasets/ronakbadhe/charity-donations)

4. Tools and Technologies

* Microsoft Excel
* SQL
* Pivot Tables
* Pivot Charts
* Excel formulas and functions
* Data cleaning and preparation
* Dashboard development
* KPI reporting

5. Data Cleaning and Preparation

Data preparation involved Excel and SQL.

Excel preparation

* Checked donation records for duplicates.
* Reviewed missing regional information and used lookup functions to retrieve relevant region details.
* Standardised donor type categories into Individual, Corporate and Foundation.
* Created a budget-versus-donation variance calculation.

SQL preparation and analysis

* Joined the Donations, Donors and Assignments tables.
* Used aggregate functions to calculate total donations, average donations and donation counts.
* Grouped and compared donation performance across regions, donor types and assignments.
* Explored budget and impact score relationships.
* Analysed yearly fundraising performance.

6. SQL Analysis

SQL was used to investigate fundraising patterns and answer key business questions.

The analysis included:

* Total donations received.
* Highest-funded assignment.
* Highest-contributing region.
* Highest-contributing donor.
* Donation contributions by donor type.
* Comparison of assignment budgets and impact scores.
* Yearly donation performance.

Example SQL Query: Yearly Donation Performance

SELECT
    YEAR(donation_date) AS year,
    COUNT(*) AS num_donations,
    ROUND(SUM(amount), 2) AS total_money,
    ROUND(AVG(amount), 2) AS avg_donation
FROM donations
GROUP BY YEAR(donation_date)
ORDER BY year;

This query summarises the number of donations, total amount raised and average donation by year.

7. Excel Dashboard Development

The interactive dashboard was developed using Microsoft Excel, Pivot Tables, Pivot Charts and Slicers.

Dashboard components:

1. Total Donations by Year (2021–2023).
2. Donations by Donor Type.
3. Donations by Region.
4. Budget versus Actual Donations by Region.

The dashboard provides a visual overview of fundraising performance and allows users to explore donation patterns.

8. Key Performance Indicators

Metric	Result
Total Donations	$25,976,215.89
Number of Donations	4,998
Average Donation	$5,197.32
Total Budget	$122,021,185.93
Budget Achievement	21.3%

9. Key Findings

* Total fundraising reached approximately 21.3% of the overall budget.
* Fundraising performance in 2021 and 2022 was stronger than in 2023.
* The East region recorded the highest donation contribution.
* All regions recorded donations below their respective budget targets.

10. Recommendations

Based on the findings, the following actions could support improved fundraising performance:

1. Investigate the decline in fundraising performance during 2023.
2. Examine successful fundraising approaches in the East region for possible application elsewhere.
3. Review regional fundraising targets and budget assumptions.
4. Strengthen donor engagement and retention strategies.
5. Monitor fundraising performance regularly using KPI reporting.

11. Dashboard Preview

12. Project Files

* View Excel Dashboard Workbook
* View Dashboard Screenshot

13. Skills Demonstrated

Technical Skills

* Microsoft Excel
* SQL
* Data Cleaning
* Data Analysis
* Data Integration
* Pivot Tables and Pivot Charts
* Dashboard Development
* KPI Reporting

Analytical Skills

* Fundraising Performance Analysis
* Donor Contribution Analysis
* Regional Performance Analysis
* Budget Monitoring
* Business Insights and Recommendations

14. Project Outcome

This project demonstrates the application of Excel and SQL to analyse nonprofit fundraising data, monitor budget performance and generate insights that can support evidence-based programme and fundraising decisions.
