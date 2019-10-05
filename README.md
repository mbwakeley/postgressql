# postgressql

# SQL Reference Sheet

## How to create a database

- Type CREATE DATABASE databasename; in Query Tool then refrest

## How to create a table

- In Query tool type the following
  CREATE TABLE table_name (
  column1 datatype,
  column2 datatype,
  column3 datatype,
  ....
  );

## How to get everything from a single table?

    - select * from table_name

## How to get one thing from a single table with a "where" clause

- SELECT column1, column2, columnN FROM table_name;
  SELECT column1, column2, columnN
  FROM table_name
  WHERE [search_condition]

## How to add something to a table

- INSERT INTO TABLE_NAME (column1, column2, column3,...columnN)
  -VALUES (value1, value2, value3,...valueN);
  EX:
  INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
  VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');

## How to edit something inside of a table

UPDATE table_name
SET column1 = value1, column2 = value2...., columnN = valueN
WHERE [condition];
EX:
UPDATE Customers
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'
WHERE CustomerID = 1;

## How to remove something from a table

DELETE FROM table_name
WHERE [condition];
EX:
DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';

## What is a join statement? Why would we use a join statement?

-A JOIN clause is used to combine rows from two or more tables, based on a related column between them.

## create a join statement

- select (what datatypes you want)
  from one table
  inner join another table
  on table.varaible.=table.variable
  ex
  SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
  FROM Orders
  INNER JOIN Customers
  ON Orders.CustomerID=Customers.CustomerID;
