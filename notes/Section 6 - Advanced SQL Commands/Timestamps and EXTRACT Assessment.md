## Challenge:

1. - During which months did payments occur?
   - Format your answer to return back the full month name.

2. How many payments occured on a Monday?

Answer:

```
1. SELECT DISTINCT TO_CHAR(payment_date, 'MONTH')
FROM payment

2. SELECT COUNT(*), EXTRACT(DOW FROM payment_date)
FROM payment
GROUP BY EXTRACT(DOW FROM payment_date)
HAVING EXTRACT(DOW FROM payment_date) = 1
```
