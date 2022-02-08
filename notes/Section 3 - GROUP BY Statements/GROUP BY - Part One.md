## Syntax:

```
SELECT column_A, column_B FROM table GROUP BY column_A, column_B;
```

## SQL Keywords:

- GROUP BY

## Notes:

- `GROUP BY` allows us to aggregate columns per _category_.
- The `GROUP BY` clause must appear right after a FROM or WHERE statement.
- In the `SELECT` statement, columns must either have an aggregate function or be in the `GROUP BY` call.
- `WHERE` statements should not refer to the aggregation result.
- If want to sort results based on the aggregate, make sure to reference the entire function (if no alias is used).

## Challenge:

- N/A

### Answer:

```
N/A
```
