# Day 7: Writing My First SQL Queries – SELECT and WHERE

Today was my first hands-on SQL practice after setting up PostgreSQL and pgAdmin.

I learned how to retrieve and filter data from a database using SQL.

## What I Learned

### SELECT

The `SELECT` statement retrieves data from a table.

Example:

```sql
SELECT *
FROM employees;
```

### WHERE

The `WHERE` clause filters records based on a condition.

Example:

```sql
SELECT *
FROM employees
WHERE department = 'Engineering';
```

### Other SQL Concepts Covered

- Comparison Operators (`=`, `>`, `<`, `>=`, `<=`, `<>`)
- AND
- OR
- NOT
- BETWEEN
- IN
- LIKE
- ILIKE
- IS NULL
- IS NOT NULL
- DISTINCT
- AS (Aliases)

---

# 💻 Hands-on Practice

### Retrieve all employees

```sql
SELECT *
FROM employees;
```

**Output**

Returns every employee record in the table.

---

### Retrieve only names

```sql
SELECT first_name, last_name
FROM employees;
```

**Output**

Returns only the employee names.

---

### Retrieve Engineering employees

```sql
SELECT *
FROM employees
WHERE department = 'Engineering';
```

**Output**

Displays only employees working in the Engineering department.

---

### Find employees earning above ₦100,000

```sql
SELECT *
FROM employees
WHERE salary > 100000;
```

**Output**

Returns employees whose salary is greater than ₦100,000.

---

### Find employees aged between 25 and 35

```sql
SELECT *
FROM employees
WHERE age BETWEEN 25 AND 35;
```

**Output**

Returns employees whose ages fall within the specified range.

---

### Search employees whose names start with "Ch"

```sql
SELECT *
FROM employees
WHERE first_name LIKE 'Ch%';
```

**Output**

Returns names beginning with "Ch".

---

## 🧩 Application Support Scenario

Imagine a customer contacts the support team and says:

> "I can't log into my account."

One of the first things an Application Support Engineer might do is verify whether the user's record exists.

Example:

```sql
SELECT *
FROM users
WHERE email = 'john@example.com';
```

If no record is returned, the issue may be that the account doesn't exist.

If the record exists, the investigation can continue by checking the account status, password reset history, or application logs.

This helped me understand that SQL isn't just for developers—it's an essential troubleshooting tool for Application Support professionals.

---

## ⚠️ Challenges I Faced

While learning today, I noticed that SQL syntax must be written carefully.

For example, text values need to be enclosed in single quotes.

❌ Incorrect

```sql
WHERE department = Engineering;
```

✅ Correct

```sql
WHERE department = 'Engineering';
```

Small syntax mistakes can prevent queries from running successfully.

---

## 🎯 Key Takeaway

Today's lesson helped me see SQL as a language for asking questions about data.

The better I become at writing SQL queries, the better I'll be at investigating application issues and supporting users.

---

## ➡️ Next Steps

Tomorrow I'll learn:

- ORDER BY
- LIMIT
- COUNT()
- Aggregate Functions
