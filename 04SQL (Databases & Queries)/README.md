# **Step 4: SQL (Databases & Queries)**

📺 **Resources:**

* [SQL Full Course for Beginners (YouTube)](https://www.youtube.com/watch?v=9Pzj7Aj25lw)
* [SQL Tutorial – W3Schools](https://www.w3schools.com/sql/)

---

### Topics to Cover

* **SQL Basics**

  * SELECT statements
  * WHERE filters (AND, OR, BETWEEN, LIKE, IN)
  * ORDER BY, LIMIT, OFFSET
  * Aliasing columns and tables

* **Aggregation & Grouping**

  * GROUP BY, HAVING
  * Aggregate functions: SUM, AVG, COUNT, MAX, MIN

* **Joins**

  * INNER, LEFT, RIGHT, FULL joins
  * Combining multiple tables

* **Subqueries & Advanced SQL**

  * Nested queries
  * Common Table Expressions (CTEs)
  * Window functions (ROW\_NUMBER, RANK, PARTITION BY)

* **Mini Projects**

  * E-commerce analysis (top products, revenue trends)
---

### **Practice Questions**

---

#### SQL Basics

1. Create a table `Employees` with columns: EmployeeID, Name, Department, Salary, JoiningDate.
2. Insert sample data into `Employees`.
3. Select all columns from `Employees`.
4. Display only Name and Department.
5. Show employees who work in the IT department.
6. Retrieve employees with Salary > 45,000.
7. Show employees who joined after `2020-01-01`.
8. Retrieve employees with Salary between 40,000 and 55,000.
9. Display employees whose Department is either HR or Finance.
10. Retrieve employees whose name starts with 'S'.
11. Show employees whose name ends with 'a'.
12. Display employees ordered by Salary in descending order.
13. Display the first 3 employees based on JoiningDate.
14. Retrieve employees skipping the first 2 rows using OFFSET.
15. Show Employee Name as `Employee_Name` using alias.
16. Display Department as `Dept` and Salary as `Income`.
17. Show top 3 highest paid employees with aliasing.
18. Find the highest salary in the Employees table.
19. Find the total number of employees in each department.
20. Show the average salary of all employees.
21. Display the employee(s) with the lowest salary.

---

#### Aggregation & Joins

1. Count how many employees are in each Department.
2. Find the average salary per Department.
3. Show the highest and lowest salary in each Department.
4. Show total salary paid per Department.
5. Count how many employees joined in each year.
6. Find Departments that have more than 1 employee.
7. Find Departments where average salary > 50,000.
8. Find joining years where more than 2 employees joined.
9. Perform an INNER JOIN to show Employee Name with their Manager.
10. Perform a LEFT JOIN to list all employees and their managers (even if missing).
11. Show total salary per Department using JOIN + GROUP BY.
12. Find the employee with the highest salary using a subquery.
13. Find all employees who earn more than the average salary.
14. Find the second highest salary using a subquery.
15. Find employees who joined after the one with the lowest salary.
16. List Departments that have any employee earning > 60,000.
17. Find the total number of employees and total salary per Department.
18. List all employees whose salary is the maximum in their Department.
19. Show all Departments where no employee earns less than 45,000.
20. Find employees whose joining year matches any HR department employee (using subquery).

---

#### Advanced SQL

1. Use `ROW_NUMBER` to assign rank based on Salary.
2. Use `RANK` and `DENSE_RANK` to handle ties in salaries.
3. Use `PARTITION BY Department` to rank employees within each department.
4. Write a CTE to find average salary per department, then filter where avg > 50,000.
5. Write a nested query to find employees earning above their department’s average.
6. Create a query that returns top 3 earners in each department.
7. Use a window function to calculate running total of salaries.
8. Find the difference between each employee’s salary and department average.
9. Write a query to get year-over-year growth in salary expenses.
10. Create a SQL script for student scores → show top performers per subject.

---

✅ That completes **Step 4: SQL (Databases & Queries)**.