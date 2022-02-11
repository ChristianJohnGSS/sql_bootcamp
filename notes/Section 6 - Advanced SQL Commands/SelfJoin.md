## Syntax:

```

```

## SQL Keywords:

-

## Notes:

- Use alias to diffentiate the two tables
- Keyword same as `JOIN`

## Challenge:

-

### Answer:

```
// Sample query

SELECT film_A.title, film_B.title, film_A.length FROM film AS film_A
INNER JOIN film AS film_B ON film_A.film_id != film_B.film_id
AND film_A.length = film_B.length
```
