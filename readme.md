Hi There ! <br />

Description: <br />
	Here I written an few sql query to fetch the particular record. <br />

Requirements: <br />
1) SQL Database. <br />
2) SQL Table. (customers, Products, Orders) <br />
<br />
Query with Scenario: <br />
<br />
1) Find all customers in Berlin: <br />
Query: <br />
	SELECT * FROM Customers WHERE City = "Berlin"; <br />
<br />
2) Find all customers in Mexico City: <br />
Query: <br />
	SELECT * FROM Customers WHERE City = "México D.F."; <br />
<br />
3) Find avg price of all products: <br />
Query: <br />
	SELECT AVG(Price) FROM Products; <br />
<br />
4) Find number of products that Have price = 18: <br />
Query: <br />
	SELECT COUNT(ProductID) FROM Products WHERE Price = 18; <br />
<br />
5) Find orders between 1996-08-01 and 1996-09-06: <br />
Query: <br />
	SELECT * FROM Orders WHERE OrderDate BETWEEN "1996-08-01" AND "1996-09-06"; <br />
<br />
6) Find customers with more than 3 orders: <br />
Query: <br />
	SELECT CustomerID, COUNT(CustomerID) FROM Orders GROUP BY CustomerID HAVING COUNT(CustomerID) > 3; <br />
<br />
7) Find all customers that are from the same city: <br />
Query: <br />
	SELECT CustomerID, CustomerName, City FROM Customers 
    WHERE City IN (SELECT City FROM Customers GROUP BY CITY HAVING COUNT(*) > 1) ORDER BY City;
<br />