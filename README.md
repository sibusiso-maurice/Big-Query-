# BRIGHTLEARN       
Practical exercise (Google BigQuery) 
Dataset: Retail Sales Dataset 
QUESTIONS 
1. WHERE Clause 
Q1. Filter all transactions that occurred in the year 2023. 
Expected output: All columns 
2. Filtering + Conditions 
Q2. Display all transactions where the Total Amount is more than the average Total Amount 
of the entire dataset. 
Expected output: All columns 
3. Aggregate Functions 
Q3. Calculate the total revenue (sum of Total Amount). 
Expected output: Total_Revenue 
4. DISTINCT 
Q4. Display all distinct Product Categories in the dataset. 
Expected output: Product_Category 
5. GROUP BY 
Q5. For each Product Category, calculate the total quantity sold. 
Expected output: Product_Category, Total_Quantity 
6. CASE Statement 
Q6. Create a column called Age_Group that classifies customers as ‘Youth’ (<30), ‘Adult’ 
(30–59), and ‘Senior’ (60+). 
Expected output: Customer_ID, Age, Age_Group 
7. Conditional Aggregation 
Q7. For each Gender, count how many high-value transactions occurred (where Total 
Amount > 500). 
Expected output: Gender, High_Value_Transactions 
8. HAVING Clause 
Q8. For each Product Category, show only those categories where the total revenue 
exceeds 5,000. 
Expected output: Product_Category, Total_Revenue 
9. Calculated Fields 
Q9. Display a new column called Unit_Cost_Category that labels a transaction as: – 'Cheap' if Price per Unit < 50 – 'Moderate' if Price per Unit between 50 and 200 – 'Expensive' if Price per Unit > 200 
Expected output: Transaction_ID, Price_per_Unit, Unit_Cost_Category 
10. Combining WHERE + CASE 
Q10. Display all transactions from customers aged 40 or older and add a column 
Spending_Level showing ‘High’ if Total Amount > 1000, otherwise ‘Low’. 
Expected output: Customer_ID, Age, Total_Amount, Spending_Level 
