# 📅 Day 18 – SELF JOIN, USING & NATURAL JOIN

## Topics Covered

- SELF JOIN
- Employee–Manager relationships
- Table aliases
- LEFT SELF JOIN
- Counting employees under each manager
- USING clause
- NATURAL JOIN

---

## What I Learned

Today I learned how SQL can join a table to itself using aliases. This technique is useful for hierarchical data such as employees and managers.

I practiced:

- Listing employees alongside their managers.
- Counting the number of employees reporting to each manager.
- Finding employees without managers.
- Combining SELF JOIN with other JOINs.

I also explored the `USING` clause, which simplifies joins when both tables share the same column name, and learned why `NATURAL JOIN` is generally avoided in production code.

---

## Biggest Takeaway

Aliases represent different roles within the same table, making SELF JOIN possible.

Understanding the relationship between data is more important than memorizing SQL syntax.

---

## Next Up

Data Manipulation Language (DML):

- INSERT
- UPDATE
- DELETE
- Transactions (`BEGIN`, `COMMIT`, `ROLLBACK`)
