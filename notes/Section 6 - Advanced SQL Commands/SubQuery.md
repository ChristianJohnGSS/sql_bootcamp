## Syntax:

```

```

## SQL Keywords:

- Sub Query uses two `SELECT` statements
- Sub Query is first to execute because its inside of parenthesis

## Notes:

-

## Challenge:

-

### Answer:

```
// Sample Query
SELECT title, rental_rate FROM film
WHERE rental_rate > (SELECT ROUND(AVG(rental_rate), 2) FROM film)
```
