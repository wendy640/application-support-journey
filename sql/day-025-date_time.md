# Day 25 — SQL Date & Time Functions

Today I continued my PostgreSQL learning journey with **Date & Time Functions**.

Date and time functions are useful when working with records that depend on when something happened, such as employee hiring dates, transactions, activity logs, and system events.

## 📅 Functions & Concepts Learned

### 1. CURRENT_DATE

Returns the current date.

```sql
SELECT CURRENT_DATE;
2. EXTRACT()

EXTRACT() allows us to retrieve a specific part of a date.

Extract the year
SELECT 
    first_name,
    last_name,
    EXTRACT(YEAR FROM hire_date) AS hire_year
FROM employees;
Extract the month
SELECT 
    first_name,
    last_name,
    EXTRACT(MONTH FROM hire_date) AS hire_month
FROM employees;
Extract the day
SELECT 
    first_name,
    last_name,
    EXTRACT(DAY FROM hire_date) AS hire_day
FROM employees;
3. AGE()

AGE() calculates the difference between two dates.

SELECT 
    first_name,
    last_name,
    AGE(CURRENT_DATE, hire_date) AS duration
FROM employees;

This can be useful for calculating how long an employee has been with a company.

4. INTERVAL

INTERVAL allows us to work with periods of time.

For example, to find employees hired within the last year:

SELECT *
FROM employees
WHERE hire_date >= CURRENT_DATE - INTERVAL '1 year';

This compares each employee's hire_date with the date one year before the current date.

💡 Key Takeaways

Today I learned how to:

Get the current date using CURRENT_DATE
Extract the year, month, and day from a date using EXTRACT()
Calculate the duration between dates using AGE()
Work with periods of time using INTERVAL
Filter records based on a date range
🛠️ Application Support Connection

Date and time operations are especially useful in Application Support.

When troubleshooting an application, I may need to investigate:

When a user account was created
When an issue occurred
Recent transactions
System activity
Records created within a particular period

Being comfortable with date-based SQL queries will make it easier to investigate these types of issues.

🚀 Next

Next, I'll continue with TO_CHAR() for formatting dates and then complete the Date & Time Functions section.
