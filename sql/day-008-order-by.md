# Day 8: Sorting and Limiting Data with SQL

Today, I learned how to sort, organize, and limit query results using SQL.

These commands are commonly used in Application Support to investigate records, retrieve recent transactions, and paginate large datasets.

---

# 📖 What I Learned

## ORDER BY

The `ORDER BY` clause sorts query results.

Ascending order (ASC) is the default.

```sql
SELECT *
FROM products
ORDER BY price ASC;
```

Descending order:

```sql
SELECT *
FROM products
ORDER BY price DESC;
```

---

## ASC and DESC

- ASC → Lowest to Highest
- DESC → Highest to Lowest

Example:

```sql
SELECT name, salary
FROM employees
ORDER BY salary DESC;
```

---

## LIMIT

Returns only a specified number of rows.

Example:

```sql
SELECT *
FROM products
LIMIT 5;
```

Useful when viewing only the first few records.

---

## OFFSET (Pagination)

OFFSET skips rows before returning results.

Example:

```sql
SELECT id, name, price
FROM products
ORDER BY id
LIMIT 10
OFFSET 10;
```

This returns rows 11–20.

This technique is commonly used for pagination.

---

## FETCH FIRST

Another way to limit returned rows.

```sql
SELECT player_name, score
FROM scores
ORDER BY score DESC
FETCH FIRST 3 ROWS ONLY;
```

---

## NULLS FIRST and NULLS LAST

Sometimes a column contains NULL values.

SQL allows us to control where NULL values appear.

```sql
SELECT product_name, category, discount_percent
FROM products
ORDER BY discount_percent ASC NULLS LAST;
```

This places products without discounts at the bottom.

---

# 💻 Hands-on Practice

## Find the five most expensive products

```sql
SELECT name, price
FROM products
ORDER BY price DESC
LIMIT 5;
```

### Output

Returns the five products with the highest prices.

---

## Retrieve page 2 of products

```sql
SELECT id, name, price
FROM products
ORDER BY id ASC
LIMIT 10
OFFSET 10;
```

### Output

Returns products 11–20.

---

## Find the top three players

```sql
SELECT player_name, score
FROM scores
ORDER BY score DESC
FETCH FIRST 3 ROWS ONLY;
```

### Output

Returns the three highest-scoring players.

---

## Display discounts with NULL values last

```sql
SELECT product_name, category, discount_percent
FROM products
ORDER BY discount_percent ASC NULLS LAST;
```

### Output

Displays products with discounts first, followed by products without discounts.

---

# 🧩 Application Support Scenario

Imagine a customer support team receives this request:

> "Can you show me the latest five orders placed today?"

An Application Support Engineer could write:

```sql
SELECT order_id, customer_name, created_at
FROM orders
ORDER BY created_at DESC
LIMIT 5;
```

This quickly retrieves the five most recent orders.

---

Another example:

> "The customer is on page 3 of the application. Why can't they see their order?"

Many web applications use pagination.

```sql
SELECT *
FROM orders
ORDER BY order_id
LIMIT 20
OFFSET 40;
```

Understanding LIMIT and OFFSET helps Application Support Engineers verify exactly what users see on each page.

---

# ⚠️ Challenges I Faced

One thing I learned today is that SQL executes clauses in a specific order.

For pagination to work correctly, `ORDER BY` should be used before `LIMIT` and `OFFSET`.

Without sorting first, the returned rows may not be consistent.

---

# 🎯 Key Takeaway

Today's lesson showed me that SQL is not just about retrieving data—it is also about presenting it in a meaningful way.

Sorting, limiting, and paginating data are essential skills for investigating records and supporting business applications.

---

# ➡️ Next Steps

Tomorrow I'll begin learning aggregate functions such as:

- COUNT()
- SUM()
- AVG()
- MIN()
- MAX()
