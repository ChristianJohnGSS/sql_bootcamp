# ORDER BY

## Syntax:

```
SELECT <column_name/s>
FROM <table_name>
ORDER BY <column> <ASC or DESC>;
```

- Used to sort rows based on a column value, in either ASC (ascending) or DESC (descending) order

## SQL Keywords:

- ORDER BY
- ASC
- DESC

## Notes:

- `ORDER BY` is generally used at the end of the query because we want to do selection and filtering first
- If `ASC or DESC` is left blank, it will use `ASC` by default
- Able to put columns in `ORDER BY` that is not included in the `SELECT` statement
- Every column included in `ORDER BY` can have one sort keyword `ASC or DESC`

# LIMIT

## Syntax:

```
SELECT <column_name/s> FROM <table_name> LIMIT <count>;
```

- Used to limit the number of rows returned by a query

## SQL Keywords:

- LIMIT

## Notes:

- `LIMIT` goes to the very end of a query and is the last command to be executed

## Challenge:

1. - We want to reward our first 10 paying customers.
   - What are the customer ids of the first 10 customers who created a payment?
2. - A customer wants to quickly rent a video to watch over their short lunch break.
   - What are the titles of the 5 shortest (in length of runtime) movies?
3. - If the previous customer can watch any movie that is 50 minutes or less in run time, how many options does she have?

### Answer:

```
1. SELECT customer_id FROM payment ORDER BY payment_date ASC LIMIT 10;
2. SELECT title FROM film ORDER BY length LIMIT 5;
3. SELECT COUNT(*) FROM film WHERE length <= 50;
```
