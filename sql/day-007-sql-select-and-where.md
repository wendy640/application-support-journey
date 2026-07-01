# Day 7: Writing My First SQL Queries – SELECT and WHERE

Today was my first hands-on SQL practice after setting up PostgreSQL and pgAdmin.

I learned how to retrieve and filter data from a database using SQL.

## SELECT

The `SELECT` statement is used to retrieve data from a table.

Example:

```sql
SELECT * FROM employees;
```

This retrieves every column and every row from the `employees` table.

To retrieve only specific columns:

```sql
SELECT first_name, last_name
FROM employees;
```

## WHERE

The `WHERE` clause filters records based on a condition.

Example:

```sql
SELECT *
FROM employees
WHERE department = 'Engineering';
```

## Comparison Operators

I also learned how to filter data using comparison operators:

- =
- >
- <
- >=
- <=
- <>

## Logical Operators

SQL allows multiple conditions using:

- AND
- OR
- NOT

Example:

```sql
SELECT *
FROM employees
WHERE department = 'Engineering'
AND salary > 50000;
```

## BETWEEN

Used to find values within a range.

```sql
SELECT *
FROM employees
WHERE salary BETWEEN 50000 AND 80000;
```

## IN

Checks if a value exists in a list.

```sql
SELECT *
FROM employees
WHERE age IN (25,30,35);
```

## LIKE and ILIKE

Used for pattern matching.

LIKE is case-sensitive in PostgreSQL.

ILIKE is case-insensitive.

Example:

```sql
SELECT *
FROM employees
WHERE first_name LIKE 'Ch%';
```

## IS NULL

Checks for empty values.

```sql
SELECT *
FROM employees
WHERE phone_number IS NULL;
```

## DISTINCT

Returns unique values.

```sql
SELECT DISTINCT department
FROM employees;
```

## AS (Alias)

Renames a column in the output.

```sql
SELECT salary AS Monthly_Salary
FROM employees;
```

## Key Takeaway

Today I realized SQL is like asking a database questions.

The better I understand SQL, the easier it will be to investigate issues, verify records, and troubleshoot applications as an Application Support Specialist.

## Next Step

Learn ORDER BY, LIMIT, COUNT, and Aggregate Functions.
