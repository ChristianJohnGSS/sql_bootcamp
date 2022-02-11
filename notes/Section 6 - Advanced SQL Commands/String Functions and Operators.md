## Syntax:

```

```

## SQL Keywords:

-

## Notes:

- Link: https://www.postgresql.org/docs/13/functions-string.html

## Challenge:

-

### Answer:

```
// Sample query

SELECT LOWER(LEFT(first_name, 1)) || LOWER(last_name) || '@gmail.com' AS custom_email FROM customer
```
