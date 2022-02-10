## Syntax:

```
SELECT columns FROM table_A
LEFT OUTER JOIN table_B
ON table_A.matched_column = table_B.matched_column
// Optional, for further filtering
WHERE table_B.id IS NULL
```

## SQL Keywords:

- LEFT OUTER JOIN

## Notes:

- `LEFT OUTER JOIN` results in the set of records that are in the left table, if there is no match with the right table
- Written order of tables in SQL query **matters**. Table to get data from using `LEFT OUTER JOIN` should be on the left-side of the query.
- Can use `WHERE` statement to get unique rows on left table only.

## Challenge:

- N/A

### Answer:

```
// Sample query from course
SELECT film.film_id, title, inventory_id, store_id  FROM film
LEFT JOIN inventory ON
inventory.film_id = film.film_id
WHERE inventory.film_id IS null
```
