Day 27 — SQL Conditional Functions
Overview

Today I started learning SQL Conditional Functions in PostgreSQL.

The section covers:

CASE Expressions
CASE in Aggregations
COALESCE()
NULLIF()
GREATEST() and LEAST()

I completed the first two lessons today.

1. CASE Expressions

CASE allows SQL to return different values depending on whether a condition is true.

CASE
    WHEN salary > 100000 THEN 'High'
    WHEN salary >= 80000 THEN 'Medium'
    ELSE 'Low'
END

This can be useful for categorizing or transforming data based on business rules.

2. CASE in Aggregations

I also learned how CASE can be combined with aggregate functions.

COUNT() with CASE
COUNT(
    CASE
        WHEN salary > 100000 THEN 1
    END
)

This counts only employees whose salary is greater than 100,000.

SUM() with CASE
SUM(
    CASE
        WHEN salary > 100000 THEN salary
        ELSE 0
    END
)

This calculates the total salary of employees whose salary is greater than 100,000.

Combining the Concepts

I practiced combining:

CASE
COUNT()
SUM()
GROUP BY

to create department-level reports containing employee counts and salary totals.

Key Takeaway

One of my biggest takeaways today is that CASE can be used beyond simple conditional output.

When combined with aggregate functions, it allows me to perform conditional counting and calculations directly in SQL.

Next Lesson

Tomorrow I'll continue with:

COALESCE()

and learn how to handle NULL values more effectively in PostgreSQL.
