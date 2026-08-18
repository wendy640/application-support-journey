# 📅 Day 22 – SQL Text Functions

## Topics Covered

- UPPER()
- LOWER()
- LENGTH()
- TRIM()
- CONCAT()
- CONCAT_WS()
- REPLACE()
- SUBSTRING()
- LEFT()
- RIGHT()
- POSITION()
- INITCAP()
- REVERSE()
- LPAD()
- RPAD()
- Nested functions

## What I Learned

Today I completed the Text/String Functions section of my SQL learning roadmap.

I practiced using SQL functions to:

- Change text capitalization
- Count characters
- Remove unwanted spaces
- Combine text values
- Replace characters
- Extract portions of strings
- Find the position of text
- Format names
- Pad values for display

## Examples

### Combining text

CONCAT(first_name, ' ', last_name)

### Using a separator

CONCAT_WS(' ', first_name, last_name)

### Cleaning and transforming

UPPER(TRIM(employee_name))

### Formatting IDs

LPAD(employee_id::text, 5, '0')

## Key Takeaway

SQL functions can be used to clean, transform, format, and prepare data—not just retrieve it.

## Status

✅ Text Functions COMPLETE

## Next Up

📊 Numerical Functions
