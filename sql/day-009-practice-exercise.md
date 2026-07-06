# 📅 Day 9 – Mastering Sorting, Pagination, and Handling NULL Values

Today, I focused on organizing query results, implementing pagination, and handling `NULL` values in PostgreSQL. These concepts are essential for building reports, retrieving data efficiently, and supporting real-world business applications.

---

## 📚 Topics Covered

- `ORDER BY`
- Ascending (`ASC`) and Descending (`DESC`) Sorting
- Sorting by Multiple Columns
- `LIMIT`
- `OFFSET`
- `FETCH FIRST`
- `NULLS LAST`

---

## 🎯 Key Takeaways

- Learned how to sort query results using `ORDER BY`.
- Used `ASC` and `DESC` to control sorting direction.
- Sorted data using multiple columns for more meaningful reports.
- Used `LIMIT` to return only the required number of rows.
- Implemented pagination with `OFFSET`.
- Explored `FETCH FIRST` as an alternative to `LIMIT`.
- Learned how `NULLS LAST` improves report readability by placing missing values at the end of sorted results.
- Strengthened my understanding through real-world business reporting scenarios.

---

## 💻 Practice Completed

Completed SQL exercises involving:

- 📦 Product Reports
- 👥 Customer Pagination
- 💼 Employee Salary Reports
- 🏷️ Product Discount Reports
- 📝 Business Reporting Challenges

---

## 🧠 Reflection

One of today's biggest lessons was understanding the execution flow of a SQL query.

```sql
SELECT
FROM
WHERE
ORDER BY
LIMIT / FETCH FIRST
```

A simple way to think about it is:

- **`WHERE`** → Filters the rows you want.
- **`ORDER BY`** → Sorts the filtered rows.
- **`LIMIT` / `FETCH FIRST`** → Returns only the required number of rows.

Understanding this flow makes it much easier to write accurate and efficient SQL queries.

---

## 🚀 Looking Ahead

Tomorrow, I'll be learning **Aggregate Functions**, including:

- `COUNT()`
- `SUM()`
- `AVG()`
- `MIN()`
- `MAX()`

These functions are widely used for reporting, analytics, and troubleshooting in real-world databases.

---

> *Every query I write brings me one step closer to becoming a better Application Support Engineer.*
