## Syntax:

```
SELECT DISTINCT <column_name/s> FROM <table_name>
```

- Retrieves unique values of a column or group of columns from a table

## SQL Keywords:
- SELECT
- DISTINCT
- FROM

## Notes:

- Keyword `DISTINCT` must be before a column or can be used as a function (with parenthesis) `DISTINCT(column_name/s)`
- With and without use of parenthesis yields different format of results for multiple columns

## Challenge:

- Use what you've learned about SELECT DISTINCT to retrieve the distinct rating types of our films could have been in our database

### Answer:

```
SELECT DISTINCT rating FROM film;
// or
SELECT DISTINCT(rating) FROM film;
```
