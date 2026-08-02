# 📅 Day 16 – Understanding LEFT JOIN in PostgreSQL

Today, I learned how **LEFT JOIN** works and why it's one of the most useful JOIN types for reporting and troubleshooting.

Unlike `INNER JOIN`, which only returns matching records, `LEFT JOIN` keeps every record from the left table and fills unmatched records with `NULL`.

---

## 📚 Topics Covered

- LEFT JOIN
- INNER JOIN vs LEFT JOIN
- NULL values in JOIN results
- Finding missing records using `IS NULL`
- COUNT(*) vs COUNT(column)
- Multi-table LEFT JOINs

---

## 🎯 Key Takeaways

- Learned that LEFT JOIN always returns every row from the left table.
- Understood how NULL values indicate missing relationships.
- Practiced identifying employees without project assignments.
- Learned the difference between `COUNT(*)` and `COUNT(column)` when working with LEFT JOINs.
- Improved my confidence in writing multi-table reporting queries.

---

## 💻 Practice Completed

- Employee Assignment Reports
- Project Team Reports
- Department Reports
- Project Team Size Analysis
- Employees Without Assignments
- Multi-table LEFT JOIN Challenges

---

## 🧠 Reflection

Today's lesson taught me that the type of JOIN you choose directly affects the result of your query.

One concept I'll definitely remember is:

- `COUNT(*)` counts every returned row.
- `COUNT(column)` ignores NULL values.

That small difference can completely change the accuracy of a report when using LEFT JOIN.

---

## 🚀 Next Up

Tomorrow I'll continue learning more JOIN types and explore how different joins help answer different business questions in relational databases.

---

> *Not every record has a match—and that's exactly when LEFT JOIN becomes powerful.*
