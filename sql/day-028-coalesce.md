# Day 28 — SQL COALESCE()

Today I continued my PostgreSQL learning journey by learning **COALESCE()**.

## 📌 What is COALESCE()?

`COALESCE()` returns the **first non-NULL value** from a list of expressions.

It is especially useful when working with missing or NULL data.

### Basic Syntax

```sql
COALESCE(value1, value2, value3, ...)

PostgreSQL checks the values from left to right and returns the first value that is not NULL.

💻 Example
SELECT 
    employee_name,
    COALESCE(department_id, 0) AS department_id
FROM company_employees;

If department_id is NULL, PostgreSQL returns 0 instead.

📝 Working with Text

COALESCE() can also provide a default value for missing text.

SELECT 
    employee_name,
    COALESCE(department_name, 'Not Assigned') AS department
FROM company_employees;

If department_name is NULL, the result will be:

Not Assigned
🔎 COALESCE() with Multiple Values
SELECT COALESCE(NULL, NULL, 'Available', 'Backup');

Result:

Available

PostgreSQL checks each value from left to right and stops at the first non-NULL value.

💡 Key Takeaway

One important lesson from today:

COALESCE() does not change the original data. It allows us to provide a fallback value when a value is NULL.

This makes query results easier to understand and can be useful when displaying reports or working with incomplete database records.

🛠️ Application Support Connection

In Application Support, NULL values can appear frequently when investigating database records.

COALESCE() can help make query results more meaningful when:

User information is missing
Optional fields are NULL
A database report needs default values
Troubleshooting incomplete records
Preparing cleaner data for users or applications
🚀 What's Next?

I'll continue with the next Conditional Functions topic and keep building my PostgreSQL skills step by step.

Day 28 ✅

#SQL #PostgreSQL #COALESCE #ConditionalFunctions #ApplicationSupport #SQLLearning
