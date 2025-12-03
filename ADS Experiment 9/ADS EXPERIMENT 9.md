# ADS EXPERIMENT 9  
Demonstrate ROLLUP and CUBE Operations on a Sample Sales Database.  
  
CREATE TABLE Sales (  
    Region VARCHAR2(20),  
    Product VARCHAR2(20),  
    Amount NUMBER  
);  
  
INSERT INTO Sales VALUES ('North', 'Laptop', 50000);  
INSERT INTO Sales VALUES ('North', 'Mobile', 30000);  
INSERT INTO Sales VALUES ('South', 'Laptop', 45000);  
INSERT INTO Sales VALUES ('South', 'Mobile', 35000);  
  
SELECT   
    Region,  
    Product,  
    SUM(Amount) AS Total_Sales  
FROM Sales  
GROUP BY ROLLUP (Region, Product);  
  
SELECT   
    Region,  
    Product,  
    SUM(Amount) AS Total_Sales  
FROM Sales  
GROUP BY CUBE (Region, Product);  
