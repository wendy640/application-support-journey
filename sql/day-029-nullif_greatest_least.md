# Day 28 — SQL Conditional Functions

## Topics Covered

Today I completed the SQL Conditional Functions section in PostgreSQL.

* [x] CASE Expressions
* [x] CASE in Aggregations
* [x] COALESCE()
* [x] NULLIF()
* [x] GREATEST() & LEAST()

## CASE Expressions

Used `CASE` to apply conditional logic:

```sql
CASE
    WHEN salary > 100000 THEN 'High'
    WHEN salary >= 80000 THEN 'Medium'
    ELSE 'Low'
END
```

## CASE in Aggregations

Practiced conditional counting:

```sql
COUNT(
    CASE
        WHEN salary > 80000 THEN 1
    END
)
```

And conditional summation:

```sql
SUM(
    CASE
        WHEN salary > 80000 THEN salary
        ELSE 0
    END
)
```

Also combined these with `GROUP BY` for department-level reporting.

## COALESCE()

Learned to return the first non-NULL value:

```sql
COALESCE(email, phone_number, 'No contact information')
```

## NULLIF()

Learned to return `NULL` when two values are equal:

```sql
NULLIF(salary, 80000)
```

Also learned PostgreSQL type casting:

```sql
::text
```

and the division-by-zero protection pattern:

```sql
value / NULLIF(denominator, 0)
```

## GREATEST() & LEAST()

Used `GREATEST()` to establish a minimum:

```sql
GREATEST(salary, 80000)
```

Used `LEAST()` to establish a maximum:

```sql
LEAST(salary, 90000)
```

## Key Takeaway

SQL conditional functions provide powerful ways to transform, clean, compare, and calculate data.

The most valuable part of this section was learning how these functions can be combined instead of using them in isolation.

## Next Step

Before moving to the next SQL topic, I'll practice all five concepts together using my `company_employees` dataset.

**Day 28 complete. ✅**
