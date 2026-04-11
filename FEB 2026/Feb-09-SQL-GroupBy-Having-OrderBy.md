🔹 HAVING_CLAUSE.md

Include:

Definition of HAVING clause

Syntax

Execution order

Difference between WHERE vs HAVING

Notes:

HAVING filters groups

Executes after GROUP BY

Uses aggregate functions (COUNT, SUM, AVG)

🔹 GROUP_BY.md

Include:

Purpose of GROUP BY

Syntax

Example table (empno, ename, deptno)

Explanation of grouping department-wise

Example:

SELECT deptno, COUNT(*)
FROM emp
GROUP BY deptno;

🔹 ORDER_BY.md

Include:

Definition of ORDER BY

ASC vs DESC

Syntax

Multiple column ordering

Examples:

SELECT * FROM emp ORDER BY sal DESC;
SELECT * FROM emp ORDER BY sal, hiredate;

🔹 WHERE_vs_HAVING.md

Make a comparison table:

WHERE	HAVING
Filters rows	Filters groups
Executes before GROUP BY	Executes after GROUP BY
Cannot use aggregate functions	Uses aggregate functions
🔹 SQL_Queries.sql

Put only queries, like:

-- Employees per department (at least one employee)
SELECT deptno, COUNT(*)
FROM emp
GROUP BY deptno
HAVING COUNT(*) >= 1;

-- Departments with more than 2 employees
SELECT deptno, COUNT(*)
FROM emp
GROUP BY deptno
HAVING COUNT(*) >= 2;

-- Order employees by salary
SELECT * FROM emp ORDER BY sal DESC;
