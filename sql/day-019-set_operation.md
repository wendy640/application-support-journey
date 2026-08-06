# 📅 Day 19 – SQL Set Operators

## Topics Covered

- UNION
- UNION ALL
- INTERSECT
- EXCEPT

---

## What I Learned

Today I learned how SQL combines and compares result sets using set operators.

### UNION
Returns all unique rows from multiple queries.

### UNION ALL
Returns all rows without removing duplicates.

### INTERSECT
Returns only rows that exist in both query results.

### EXCEPT
Returns rows from the first query that are not found in the second.

---

## Key Rules

- Both queries must return the same number of columns.
- Data types must be compatible.
- Columns must appear in the same order.

---

## Biggest Takeaway

The biggest lesson today was understanding that `INTERSECT` compares complete rows rather than individual columns. This helped me understand why adding different labels (such as "Active" and "Premium") prevents rows from matching.

---

## Next Up

Tomorrow I'll begin learning Data Manipulation Language (DML), starting with:

- INSERT
