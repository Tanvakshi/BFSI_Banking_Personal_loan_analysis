Domain: Banking, Financial Services, and Insurance (BFSI)
Tools Used: Python, SQL, Data Visualization
-------------------------------------------------------------------------
The Problem: The bank has a large customer base of depositors (liability), but only a small percentage take out personal loans(asset). Marketing for entire customer base is operationally inefficient and cost-intensive. 
------------------------------------------------------------------------
The Goal: Optimize the Liability Customer (depositor) conversion rate for this bank by identifying key demographic and financial indicators that predict a high probability of loan acceptance.
------------------------------------------------------------------------
Action plan: 1. Migrated raw .CSV file into a SQLite environment (google colab) to filter data.
            2. SQL Querying: Used advanced filtering logic to isolate high-potential segment of customers (i.e, customers with high income and advanced education levels)
            3. Using Python, I analyzed the correlation between different variables such as: Income, Education & Loan Acceptance -- in order to be able to find the "income threshold" where conversion probability spikes.
            4 Data Visualisation : Plot Distribution Plots (Histograms) and use KDE (Kernel Density Estimation) to visualize the "overlap" between customers who accepted the loan versus those who did not.
-------------------------------------------------------------------------
Key Insights/ Result:
           1. Leading Indicator: Identified that "high-value segment" customers with an annual income exceeding $110k and an Education Level of 2 or higher (Graduate/Professional) are 3x more likely to accept a loan offer.
           2. Targeting Efficiency: By focusing marketing efforts on this specific segment, the bank can potentially reduce marketing spend by 60%* while maintaining 80%* of current conversion volume.
           3. Secondary Lead Indicator: Analysis showed that higher credit card spending (CCAvg) is a secondary lead indicator for loan requirement, allowing for better cross-selling opportunities.
----------------------------------------------------------------------------------------------------------------
*60% Less Marketing Spend Logic:
  Bank's total database has 5,000 customers. If we call everyone,we pay for all 5,000 phone calls - 100% marketing spend.
  Through SQL analysis, we found that the "High-Value" group (Income>$110k + Graduate) only consists of 2,000 people.
  The Math: 2000 / 5000 = 40%
  Conclusion: Hence we are only calling 40% of the people, i.e,"High-Value" group, saving 60% on marketing (money & time). 
-----------------------------------------------------------------------------------------------------------
*80% Conversion Volume" Logic (Concentration)
  no. of Customers who actually took loan in the past = 480
  Through SQL filtering, we found that out of those 480 "Yes" responders, 384 of them were in our "High-Value" group.
  The Math: 384 / 480 = 80%
  Conclusion: Even though we ignored 60% of the customers, we still retain 80% of the actual profit.

