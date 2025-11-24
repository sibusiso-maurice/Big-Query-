SELECT  FROM `brightlearndata.RetailSalesDataset.Retail Sales Dataset` LIMIT 1000

---1. WHERE Clause – Filter 2023 Transactions
SELECT *
FROM `brightlearndata.RetailSalesDataset.Retail Sales Dataset`
WHERE EXTRACT(YEAR FROM Date) = 2023;

---2. Show transactions where Total Amount > dataset average
SELECT
  *
FROM
  brightlearndata.RetailSalesDataset.`Retail Sales Dataset`
WHERE
  `Total Amount` > (
    SELECT
      AVG(`Total Amount`)
    FROM
      brightlearndata.RetailSalesDataset.`Retail Sales Dataset`
  );


  ---3. Total revenue
SELECT
  SUM(`Total Amount`) AS Total_Revenue
FROM
  brightlearndata.RetailSalesDataset.`Retail Sales Dataset`;


---4. Distinct Product Categories
SELECT DISTINCT
  `Product Category`
FROM
  brightlearndata.RetailSalesDataset.`Retail Sales Dataset`;


---5. Total quantity sold per Product Category
SELECT
  `Product Category`,
  SUM(Quantity) AS Total_Quantity
FROM
  brightlearndata.RetailSalesDataset.`Retail Sales Dataset`
GROUP BY `Product Category`;

---6. Create Age Group (Youth / Adult / Senior)
SELECT
  `Customer ID`,
  Age,
  CASE
    WHEN Age < 30 THEN 'Youth'
    WHEN Age BETWEEN 30 AND 59 THEN 'Adult'
    ELSE 'Senior'
    END
    AS Age_Group
FROM `brightlearndata`.`RetailSalesDataset`.`Retail Sales Dataset`

---7. High-value transactions (>500) per Gender
SELECT
  Gender,
  COUNTIF(`Total Amount` > 500) AS High_Value_Transactions
FROM
  `brightlearndata.RetailSalesDataset.Retail Sales Dataset`
GROUP BY Gender;

---8. Product categories with total revenue > 5000
SELECT
  `Product Category`,
  SUM(`Total Amount`) AS Total_Revenue
FROM
  brightlearndata.RetailSalesDataset.`Retail Sales Dataset`
GROUP BY `Product Category`
HAVING SUM(`Total Amount`) > 5000;


---9. Unit Cost Category (Cheap / Moderate / Expensive)
SELECT
  `Transaction ID`,
  `Price per Unit`,
  CASE
    WHEN `Price per Unit` < 50 THEN 'Cheap'
    WHEN `Price per Unit` BETWEEN 50 AND 200 THEN 'Moderate'
    ELSE 'Expensive'
  END AS Unit_Cost_Category
FROM
  brightlearndata.RetailSalesDataset.`Retail Sales Dataset`;


10. Customers aged 40+ with Spending Level
SELECT
  `Customer ID`,
  Age,
  `Total Amount`,
  CASE
    WHEN `Total Amount` > 1000 THEN 'High'
    ELSE 'Low'
  END AS Spending_Level
FROM
  brightlearndata.RetailSalesDataset.`Retail Sales Dataset`
WHERE
  Age >= 40;
