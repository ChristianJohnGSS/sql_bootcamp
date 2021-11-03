## Syntax:

```
SELECT <column_names> FROM <table_name>
```

`column_names` can be specified using the following:

- column1 **(single)** or column1, column2, column3 and so on... **(multiple)**
- \* (asterisk) **(all)**

## SQL Keywords:

- SELECT - use to select data from a database
- FROM - use to specify which table to `select` or `delete` data from
- \* (ASTERISK) - means select all column in the table

## Notes:

- Do no use \* (asterisk) if you do not need all columns when retrieving data

## Challenge:

- Use a **SELECT** statement to grab the first and last names of every customer and their email address

### Answer:

```
 SELECT first_name, last_name, email FROM customer;
```
