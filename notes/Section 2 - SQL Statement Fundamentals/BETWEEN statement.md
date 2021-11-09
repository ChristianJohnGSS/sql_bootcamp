## Syntax:

```
SELECT <column_name/s> FROM <table_name>
WHERE <column_name> BETWEEN <value_one> AND <value_two>;

SELECT <column_name/s> FROM <table_name>
WHERE <column_name> NOT BETWEEN <value_one> AND <value_two>;
```

- `BETWEEN` operator can be used to match a value against a range of values, values being `BETWEEN` low `AND` high

## SQL Keywords:

- BETWEEN
- NOT BETWEEN

## Notes:

- `Inclusivity` means including the end values to the range condition and `Exclusivity` means excluding the end values to the range condition
- `BETWEEN` uses `inclusivity` and `NOT BETWEEN` uses `exclusivity`. And by using `BETWEEN` and `NOT BETWEEN` in datetime, comparison starts at 0:00 by default

## Challenge:

- N/A

### Answer:

```
N/A
```
