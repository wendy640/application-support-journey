# Day 24: SQL Numerical Functions

Today, I continued my PostgreSQL journey by learning **Numerical Functions**.

Numerical functions allow us to perform mathematical calculations and manipulate numeric values directly within SQL queries.

## 🔢 Functions I Learned

* `ROUND()` — rounds a number to a specified number of decimal places
* `FLOOR()` — rounds a number down
* `CEIL()` — rounds a number up
* `ABS()` — returns the absolute value
* `POWER()` — raises a number to a specified power
* `SQRT()` — calculates the square root
* `MOD()` — returns the remainder after division
* `TRUNC()` — removes decimal places without rounding

## 💻 Examples

### ROUND()

```sql
SELECT employee_name,
       ROUND(salary, 2) AS rounded_salary
FROM company_employees;
```

### ABS()

```sql
SELECT employee_name,
       ABS(salary - 100000) AS salary_difference
FROM company_employees;
```

### POWER()

```sql
SELECT employee_name,
       POWER(salary, 2) AS salary_squared
FROM company_employees;
```

## 💡 Key Lessons

One important thing I learned today is the difference between:

**`ROUND()`** → rounds a value.

**`TRUNC()`** → cuts off decimal places without rounding.

I also learned that `POWER()` requires **two arguments**: the number and the exponent.

## 🚀 Next

**SQL Date & Time Functions**

Another day of learning and building my SQL foundation for my journey into **Application Support**. 🚀
