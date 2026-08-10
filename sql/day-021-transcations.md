# 📅 Day 21 – SQL Transactions

## Topics Covered

- BEGIN
- COMMIT
- ROLLBACK
- SAVEPOINT
- ROLLBACK TO SAVEPOINT

## What I Learned

Today I learned how SQL transactions allow database changes to be controlled safely.

### BEGIN

Starts a transaction.

### COMMIT

Permanently saves the changes made during the transaction.

### ROLLBACK

Undoes all changes made during the current transaction.

### SAVEPOINT

Creates a checkpoint within a transaction.

### ROLLBACK TO SAVEPOINT

Undoes changes made after a specific savepoint while keeping earlier changes within the transaction.

## Practical Exercises

I created a separate `transaction_employees` table for practice and worked through:

- Salary updates with ROLLBACK
- Department updates with COMMIT
- Multiple changes within one transaction
- SAVEPOINT and partial rollback
- Verifying changes using SELECT

## Key Takeaway

A safe database workflow is:

1. BEGIN
2. Make changes
3. Check the result
4. COMMIT or ROLLBACK

## Next Up

SQL Functions:

- Text/String Functions
- Numerical Functions
- Date & Time Functions
- NULL Functions
