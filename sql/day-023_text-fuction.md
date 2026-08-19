# 📅 Day 23 – PostgreSQL Text Expressions

## Topics Covered

- SPLIT_PART()
- Regular Expressions (Regex)
- Text pattern matching

## What I Learned

Today I continued learning PostgreSQL text expressions.

### SPLIT_PART()

SPLIT_PART() splits a string using a delimiter and returns a specific part.

Example:

SPLIT_PART('chinwe@example.com', '@', 1)

Returns:

chinwe

### Regular Expressions

I also learned the basics of using regular expressions with PostgreSQL.

Regex allows patterns to be searched for or matched within text.

## Practical Applications

These techniques can be useful for:

- Working with email addresses
- Extracting parts of structured text
- Investigating data-quality issues
- Finding patterns
- Validating and troubleshooting text data

## Key Takeaway

SQL can do more than retrieve text. PostgreSQL provides tools for analyzing the structure and patterns within textual data.

## Next Up

Continue practicing PostgreSQL text expressions and functions.
