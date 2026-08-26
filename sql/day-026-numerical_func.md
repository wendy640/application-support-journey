# Day 26 — SQL Numerical Functions: MOD, Integer Division & RANDOM

Today I continued learning **SQL Numerical Functions** in PostgreSQL.

I focused on three additional concepts:

- `MOD()`
- Integer Division
- `RANDOM()`

These functions are useful for calculations, working with remainders, generating random values, and understanding how PostgreSQL handles numeric operations.

---

## 1. MOD()

`MOD()` returns the remainder after dividing one number by another.

```sql
SELECT MOD(17, 5);

Result:

2

Because:

17 ÷ 5 = 3 remainder 2

PostgreSQL also supports the % operator for finding the remainder:

SELECT 17 % 5;

Result:

2
Practical example

MOD() can be useful when checking whether a number is even or odd.

SELECT 
    employee_id,
    MOD(employee_id, 2) AS remainder
FROM employees;

A remainder of 0 means the number is even, while a remainder of 1 means it is odd.

2. Integer Division

I also learned how PostgreSQL handles division when working with integers.

SELECT 17 / 5;

Result:

3

Because both values are integers, the decimal portion is not returned.

If I want a decimal result, I can use a decimal value:

SELECT 17.0 / 5;

Result:

3.4000000000
Key lesson

The data type of the values involved in a calculation can affect the result.

3. RANDOM()

RANDOM() generates a random decimal value between 0 and 1.

SELECT RANDOM();

Example result:

0.736428

The exact value will be different each time the query runs.

Generating a random number

For example, I can generate a random number from 1 to 100:

SELECT FLOOR(RANDOM() * 100) + 1;
Selecting a random employee

RANDOM() can also be combined with ORDER BY:

SELECT *
FROM employees
ORDER BY RANDOM()
LIMIT 1;

This returns one randomly selected employee.

💡 Key Takeaways

Today I learned:

MOD() returns the remainder after division.
% can also be used to calculate a remainder.
Integer division can produce a whole-number result.
Using decimal values can produce a decimal division result.
RANDOM() generates random decimal values.
RANDOM() can be combined with ORDER BY to randomly select records.

These concepts show how SQL can be used not only to retrieve data, but also to perform calculations and manipulate numerical values.

🛠️ Application Support Connection

Numerical operations can be useful in Application Support when investigating:

Transaction amounts
IDs and numbering patterns
Calculations stored in databases
Data validation
Random test data
Query results that don't match expected calculations

Understanding how SQL performs calculations helps when troubleshooting unexpected database results.

🚀 Next

I'll continue with the remaining SQL Numerical Functions before moving on to the next section of my SQL roadmap.

Day 26 ✅

One query at a time. One concept at a time. 🚀

#SQL #PostgreSQL #NumericalFunctions #ApplicationSupport #SQLLearning
