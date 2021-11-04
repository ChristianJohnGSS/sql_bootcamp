## Syntax:

```
SELECT (column_name/s)
FROM table_name
WHERE conditions;
```

- Allows us to specify conditions on columns for the rows to be returned
- Used with the following:
  - Comparison operators
  - Logical operators

## SQL Keywords:

- WHERE

## Notes:

- After `WHERE` statement, use comparison or logical operators to create conditions based on what you need to get, don't need to write another `WHERE` statement after the first one
- A column can have same name with its table

## Challenge:

1. - A customer forgot their wallet at our store! We need to track down their email to inform them.
   - What is the email for the customer with the name Nancy Thomas?
2. - A customer wants to know what the movie "Outlaw Hanky" is about.
   - Could you give them the description for the movie "Outlaw Hanky"?
3. - A customer is late on their movie return, and we've emailed them a letter to their address at '259 Ipoh Drive'. We should also call them on phone to let them know.
   - Can you get the phone number for the customer who lives at '259 Ipoh Drive'?

### Answer:

```
1.  SELECT email FROM customer WHERE first_name = 'Nancy' AND last_name = 'Thomas';
2.  SELECT description FROM film WHERE title = 'Outlaw Hanky';
3.  SELECT phone FROM address WHERE address = '259 Ipoh Drive';
```
