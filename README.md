# Retail Lending Dashboard

This repository contains a Power BI dashboard project analyzing key aspects of retail lending. The dashboard provides insights into loan performance, risk analysis, employee productivity, and overall revenue generation.

## Objective
The primary objective of this dashboard is to:
- Monitor retail loan performance and identify default risks.
- Analyze manager and employee productivity in sanctioning loans.
- Explore revenue generation through processing fees, loan insurance, and repayments.
- Present raw data for further analysis.

## Key Pages in the Dashboard
1. **Summary Page**:
   - Defines **default loans** as loans with a status of "Cancelled" or an active flag of `0`.
   - Includes parameter slicers for **Amount Type**, **Category**, and **Profile** for filtering data dynamically.
   - Aggregates key metrics such as total sums and averages using a centralized **Measure Table**.

2. **Deep-Dive Page**:
   - Defines **Risk Loans** as loans with a tenure >120 months and an interest rate >15%.
   - Introduces custom metrics:
     - **Avg PF Ratio** and **Avg LI Ratio**: Calculated as total loan insurance (LI) and processing fee (PF) ratios divided by the total sanctioned amount.
     - **Avg Manager/Employee Sanctioned**: Average loan sanctioned amounts normalized by unique counts of managers and employees.
   - Productivity categories for employees/managers:
     - **Low:** <5 lakhs
     - **Medium:** <20 lakhs
     - **High:** <50 lakhs
     - **Very High:** >50 lakhs
   - **Efficiency Metrics**:
     - **Login to Sanction Efficiency** and **Sanction to Disbursement Efficiency**: Evaluates time taken for loan processing against benchmarks (Quick, Average, High).
   - Risk Analysis tools using **Risk as Per** and **Risk Analysis Parameters** slicers.

3. **Data Dump Page**:
   - Displays raw data from the original dataset for detailed examination.

## Key Metrics and Calculations
- **Loan Repayment Income:**  
  Disbursed Amount multiplied by (1 + Rate of Interest)
- **Total Revenue:**  
  Sum of Processing Fee, Loan Insurance, and Loan Repayment Income
- **Sanction Efficiency:**  
   - Quick: <0.8× average time
   - Average: Between 0.8× and 1.2× average time
   - High: >1.2× average time

## Features
- **Interactive Visualizations:** Slicers for dynamic filtering by parameters like loan category, profile, and risk metrics.
- **Employee and Manager Analysis:** Productivity metrics categorized into predefined performance buckets.
- **Efficiency Tracking:** Highlights bottlenecks in loan processing times.
- **Comprehensive Metrics:** Aggregated KPIs stored in a centralized measure table for ease of updates.

## Insights
- **Default Loans:** Loans flagged as canceled or inactive are automatically identified as default risks.
- **Risk Analysis:** Long-tenure, high-interest loans are flagged as high-risk, providing actionable insights for risk management.
- **Revenue Drivers:** Processing fees, loan insurance, and repayment income are major revenue contributors.
- **Productivity Trends:** Bucketing employee/manager performance provides a clear view of individual and team contributions.

