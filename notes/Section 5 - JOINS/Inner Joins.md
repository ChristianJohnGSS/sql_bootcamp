## Syntax:

```
SELECT * FROM table_A INNER JOIN table_B ON table_A.column_match = table_B.column_match
```

## SQL Keywords:

- INNER JOIN

## Notes:

- `INNER JOIN` is used to get rows from both table that has a matching column data with each other
- If there is duplicate with column names, use table to select specific column e.g. `table.column`
- In PostgreSQL, writing only `JOIN` will default to `INNER JOIN`

## Challenge:

- N/A

### Answer:

```
// Practice code from course

SELECT payment_id, payment.customer_id, first_name
FROM payment
INNER JOIN customer
ON payment.customer_id = customer.customer_id;
```
