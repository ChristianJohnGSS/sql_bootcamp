## Challenge:

1. How many payment transactions were greater than $5.00?
2. How many actors have a first name that starts with the letter P?
3. How many unique districts are our customers from?
4. Retrieve the list of names for those distinct districts from the previous question.
5. How many films have a rating of R and a replacement cost between $5 and $15;
6. How many films have the word Truman somewhere in the title?

Answer:

```
1. SELECT COUNT(*) FROM payment WHERE amount > 5.00;
2. SELECT COUNT(*) FROM actor WHERE first_name LIKE 'P%';
3. SELECT COUNT(DISTINCT district) FROM address;
4. SELECT DISTINCT district FROM address;
5. SELECT COUNT(*) FROM film WHERE rating = 'R' AND replacement_cost BETWEEN 5 and 15;
6. SELECT COUNT(*) FROM film WHERE title LIKE '%Truman%';
```
