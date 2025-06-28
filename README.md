# Task 4: Aggregate Functions and Grouping

## 🎯 Objective
To use aggregate functions and SQL `GROUP BY` clause to summarize and analyze data stored in relational tables.

## 🛠 Tools Used

- MySQL Workbench

## 📚 Concepts Practiced
- Applying aggregate functions:
  - `SUM()`
  - `COUNT()`
  - `AVG()`
- Grouping data using `GROUP BY`
- Filtering grouped results using `HAVING`

## 💡 Example Queries
```sql
-- 1. Total salary per department
SELECT department, SUM(salary) AS total_salary
FROM employees
GROUP BY department;

-- 2. Average salary per department
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;

-- 3. Count employees in each department
SELECT department, COUNT(*) AS emp_count
FROM employees
GROUP BY department;

-- 4. Departments with more than 2 employees
SELECT department, COUNT(*) AS emp_count
FROM employees
GROUP BY department
HAVING COUNT(*) > 2;
