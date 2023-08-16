

-- join Customers and Orders tables
-- based on their shared customer_id columns
-- Customers is the left table
-- Orders is the right table 

-- right join the Customers and Orders tables

SELECT Customers.customer_id, Customers.first_name, Orders.item
FROM Customers
RIGHT JOIN Orders
ON Customers.customer_id = Orders.customer_id; 
-- Here, the code right joins the Customers and Orders tables based on customer_id, which is common to both tables. The result set contains customer_id and first_name columns from the Customers table
item column from the Orders table (including those whose customer_id value is not present in the Customers table)



-- left join the Customers and Orders tables

SELECT Customers.customer_id, Customers.first_name, Orders.amount
FROM Customers
LEFT JOIN Orders
ON Customers.customer_id = Orders.customer; 
-- Here, the SQL command selects the customer_id and first_name columns (from the Customers table) and the amount column (from the Orders table).The result set will contain those rows where there is a match between customer_id (of the Customers table) and customer (of the Orders table), along with all the remaining rows from the Customers table.

-- full outer join the Customers and Orders tables


SELECT Customers.customer_id, Customers.first_name, Orders.amount
FROM Customers
FULL OUTER JOIN Orders
ON Customers.customer_id = Orders.customer; 
Here, the SQL command selects the customer_id and first_name columns (from the Customers table) and the amount column (from the Orders table).The result set will contain all rows of both the tables, regardless of whether there is a match between customer_id (of the Customers table) and customer (of the Orders table). 


-- join Customers and Orders tables based on
-- customer_id of Customers and customer column of Orders

SELECT Customers.customer_id, Customers.first_name, Orders.amount
FROM Customers
JOIN Orders
ON Customers.customer_id = Orders.customer; 
-- Here, the SQL command selects the customer_id and first_name columns (from the Customers table) and the amount column (from the Orders table). The result set will contain those rows where there is a match between customer_id (of the Customers table) and customer (of the Orders table).



