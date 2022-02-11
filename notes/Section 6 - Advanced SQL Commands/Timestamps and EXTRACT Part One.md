## Syntax:

```

```

## SQL Keywords:

-

## Notes:

- Column datatypes:
  - TIME - Contains only time
  - DATE - Contains only date
  - TIMESTAMP - Contains date and time
  - TIMESTAMPTZ - Contains date, time and timezone
- Functions:
  - TIMEZONE
  - NOW
  - TIMEOFDAY
  - CURRENT_TIME
  - CURRENT_DATE

## Challenge:

-

### Answer:

```
// Display database settings
SHOW ALL

// Display computer's timezone
SHOW TIMEZONE

// Display timestamp
SELECT NOW()

// Display timestamp in text form
SELECT TIMEOFDAY()

// Displays current time
SELECT CURRENT_TIME

// Displays current date
SELECT CURRENT_DATE
```
