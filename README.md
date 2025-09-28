# Elevate_Labs_Task3
Filtering, Projection

Interview Questions: 1..What does SELECT * do?
  `SELECT *` returns **all columns** of a table for every row.  
  It’s a quick way to see all data but can be inefficient if the table is large or you only need specific columns.

2. How do you filter rows  
  Use a **WHERE clause** to return only rows that meet a condition.  
  Example: `SELECT * FROM Employees WHERE Department = 'HR';`  
  The database evaluates the condition for each row and includes only matching rows.

3. What is LIKE '%value%'  
  `LIKE` performs **pattern matching** on text.  
  `%` means “any sequence of characters,” so `LIKE '%value%'` finds rows where the column contains “value” anywhere.  
  `_` matches a single character.

4. What is BETWEEN used for  
  `BETWEEN` checks whether a value falls **within a range, inclusive of the endpoints**.  
  Example: `OrderDate BETWEEN '2025-01-01' AND '2025-01-31'` returns rows where `OrderDate` is on or between those dates.

5. How do you limit output rows  
  Use **LIMIT** (MySQL, PostgreSQL) or **TOP** (SQL Server) to restrict the number of rows returned.  
  Example: `SELECT * FROM Employees LIMIT 10;` shows only the first 10 rows in the result set.

6. Difference between = and IN  
  `=` compares a column to **one value**.  
  `IN` compares a column to **a list of possible values**.  
  Example:  
    - `WHERE City = 'Paris'` matches only Paris.  
    - `WHERE City IN ('Paris','London','Rome')` matches any of the listed cities.
      
7. How to sort in descending order  
  Use **ORDER BY … DESC** to sort from highest to lowest or newest to oldest.  
  Example: `SELECT * FROM Products ORDER BY Price DESC;`.

8. What is aliasing  
  Aliasing gives a **temporary name** to a column or table for clarity or convenience.  
  Example:  
  `SELECT FirstName AS Name FROM Employees;`  
  `Employees AS e` lets you reference the table as `e` in joins.

9. Explain DISTINCT  
  `DISTINCT` removes **duplicate rows** from the result set so each unique combination of selected columns appears once.  
  Example: `SELECT DISTINCT Department FROM Employees;` returns each department only once.

10. What is the default sort order  
  When you use **ORDER BY** without specifying direction, the database sorts in **ascending (ASC) order** by default.  
  Example: `SELECT * FROM Orders ORDER BY OrderDate;` lists oldest dates first.
