## Syntax:

```
N/A
```

## SQL Keywords:

- OUTER JOINS

## Notes:

- `OUTER JOINS` allows us to specify how to deal with values only present in one of the tables being joined.
  - FULL OUTER JOIN
    - Get everything, even if there are some rows that has no match with each table
    - Could have `NULL` values since everything is grabbed regardless if there is no match
    - Can add `WHERE` statement to find values that's not `NULL` (filter items to get only records with no `NULL` records)
  - LEFT OUTER JOIN
  - RIGHT OUTER JOIN

## Challenge:

- N/A

### Answer:

```
// FULL OUTER JOIN example
// Get unique rows from both tables

SELECT * FROM customer
FULL OUTER JOIN payment
ON customer.customer_id = payment.customer_id
WHERE customer.customer_id IS null
OR payment.payment_id IS null
```
