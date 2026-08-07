# 📅 Day 20 – Data Manipulation Language (DML)

## Topics Covered

- INSERT
- UPDATE
- DELETE

---

## What I Learned

Today I learned how to modify data stored in a PostgreSQL database.

### INSERT
- Insert single records
- Insert multiple records
- Use DEFAULT values

### UPDATE
- Update one or many records
- Update multiple columns
- Perform calculations during updates
- Use CASE expressions

### DELETE
- Delete specific rows
- Delete multiple rows
- Use RETURNING to view deleted records
- Understand the difference between DELETE and TRUNCATE

---

## Key Takeaways

- Always verify records with SELECT before UPDATE or DELETE.
- Always use a WHERE clause unless intentionally affecting every row.
- PostgreSQL's RETURNING clause is a useful way to confirm which rows were modified or deleted.

---

## Next Up

Tomorrow I'll begin learning:

- Transactions
  - BEGIN
  - COMMIT
  - ROLLBACK
