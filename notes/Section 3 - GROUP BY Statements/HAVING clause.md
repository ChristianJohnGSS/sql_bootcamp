## Syntax:

```
SELECT column_A, SUM(column_B) FROM table GROUP BY column_A HAVING SUM(column_B) > 100
```

## SQL Keywords:

- HAVING

## Notes:

- `HAVING` clause allows us to filter after an aggregation has already taken place.
- Aggregation on columns is done after `WHERE` clause is executed.

## Challenge:

1. - We are launching a platinum service for our most loyal customers. We will assign platinum status to customers that have 40 or more transaction payments.
   - What customer_ids are eligible for platinum status?

2. - What are the customer ids of customers who have spent more than $100 in payment transactions with our staff_id member 2?

### Answer:

```
// Number 1
SELECT customer_id, COUNT(*) FROM payment
GROUP BY customer_id
HAVING COUNT(*) >= 40

// Number 2
SELECT customer_id, SUM(amount) FROM payment
WHERE staff_id = 2
GROUP BY customer_id
HAVING SUM(amount) > 100
```
