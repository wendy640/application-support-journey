# Day 30 — SQL Subqueries: WHERE and IN

## 📚 Topics Learned

Today I continued my SQL learning journey by studying **Subqueries**, focusing on:

* `WHERE` with subqueries
* `IN` with subqueries
* Single-value subqueries
* Multi-row subqueries
* Using aggregate functions inside subqueries

## 🧠 What is a Subquery?

A subquery is a SQL query nested inside another query.

It allows the result of one query to be used by another query.

### Example

```sql
SELECT employee_name, salary
FROM company_employees
WHERE salary > (
    SELECT AVG(salary)
    FROM company_employees
);
```

The inner query calculates the average salary, while the outer query finds employees earning more than that average.

## 🔹 Using IN with a Subquery

`IN` is useful when a subquery can return multiple values.

```sql
SELECT employee_name, department_id, salary
FROM company_employees
WHERE department_id IN (
    SELECT department_id
    FROM company_employees
    WHERE employee_name IN ('Alice', 'Emma', 'Bob')
);
```

The subquery identifies the relevant department IDs, and the outer query retrieves employees belonging to those departments.

## 📝 Practice Completed

I practiced queries for:

1. Employees earning above average salary
2. Employees earning below average salary
3. Employees with the highest salary
4. Employees in the same department as Alice
5. Employees earning more than Alice
6. Employees in departments where someone earns more than 90,000
7. Employees in departments associated with Alice, Bob, or Emma

## 💡 Key Takeaway

A useful way to think about subqueries is:

**Inner query → produces information → outer query uses that information**

I also learned that `=` is generally appropriate when I'm comparing against a single value, while `IN` is useful when the subquery can return multiple values.

## 🔜 Next

Next lesson:

* `EXISTS`
* `NOT EXISTS`
* Correlated subqueries

I will continue building on this before moving deeper into SQL `JOINs`.

---

### 📌 About This Article

This article documents **Day 30 of my SQL learning journey**, where I practiced SQL subqueries using the `WHERE` clause and `IN` operator with a practical employee dataset.

The goal of this learning series is to build strong SQL fundamentals through consistent practice and gradually develop the skills needed for **Application Support and software-related roles**.

## 💬 Comment

Day 30 completed! 🎉

Today was all about understanding how one query can provide information that another query can use.

Next stop: **EXISTS and NOT EXISTS.** 🚀
