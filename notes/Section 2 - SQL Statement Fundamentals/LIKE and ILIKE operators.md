## Syntax:

```
SELECT <column_name/s> FROM <table_name>
WHERE <column_name> LIKE %<pattern>%
```

- Allows us to query records by finding a match using a pattern against a column

## SQL Keywords:

- LIKE - case-sensitive
- ILIKE - case-insensitive

## Notes:

- `ILIKE` is only used in PostgreSQL, not native in SQL
- `%` (percent) is used to match a pattern of characters based on the position (start or end)
```
first_name (column name)
Christian
Makoto
Michael

// Get records of column first_name that stars with 'Chris'
WHERE first_name LIKE 'Chris%';
// Get records of column first_name that ends with 'koto
WHERE first_name LIKE '%koto';
```
- `_` (underscore) is used to replace a single character to be filled up by the query
```
uuid (column name)
BLC-QMTX59
BLC-DRBN9A
BLC-DRBN9B

// Get records of column uuid that has values that can be placed in the underscore
WHERE uuid LIKE 'BLC-DR____'
```
## Challenge:

- N/A

### Answer:

```
N/A
```
