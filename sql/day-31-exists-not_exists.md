# Day 31 — EXISTS, NOT EXISTS & JOIN + Subqueries

## 📚 What I Learned

Today I continued studying SQL subqueries and covered two major areas:

### 1. EXISTS and NOT EXISTS

I practiced:

* `EXISTS`
* `NOT EXISTS`
* Correlated subqueries
* Comparing values between the outer and inner queries

I learned that:

```sql
EXISTS
```

checks whether a matching row exists, while:

```sql
NOT EXISTS
```

checks whether a matching row does not exist.

### 2. JOIN + Subqueries

I also started combining `JOINs` with subqueries using a related `company_departments` table.

For example:

```sql
SELECT e.employee_name,
       d.department_name,
       e.salary
FROM company_employees e
JOIN company_departments d
    ON d.department_id = e.department_id
WHERE e.salary > (
    SELECT AVG(e2.salary)
    FROM company_employees e2
);
```

This combines a `JOIN` for retrieving related department information with a subquery for calculating the average salary.

## 💡 Key Takeaway

Today helped me understand that subqueries can be combined with other SQL concepts to solve more practical problems.

I'm still working on one correlated subquery challenge and will continue with it tomorrow.

**Day 31 ✅**

#SQL #PostgreSQL #LearningSQL #ApplicationSupport #TechJourney
