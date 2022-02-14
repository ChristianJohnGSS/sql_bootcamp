## Challenge:

1. How can you retrieve all the information from the cd.facilities table?

2. You want to print out a list of all of the facilities and their cost to members. How would you retrieve a list of only facility names and costs?

3. How can you produce a list of facilities that charge a fee to members?

4. How can you produce a list of facilities that charge a fee to members, and that fee is less than 1/50th of the monthly maintenance cost? Return the facid, facility name, member cost, and monthly maintenance of the facilities in question.

5. How can you produce a list of all facilities with the word 'Tennis' in their name?

6. How can you retrieve the details of facilities with ID 1 and 5? Try to do it without using the OR operator.

7. How can you produce a list of members who joined after the start of September 2012? Return the memid, surname, firstname, and joindate of the members in question.

8. How can you produce an ordered list of the first 10 surnames in the members table? The list must not contain duplicates.

9. You'd like to get the signup date of your last member. How can you retrieve this information?

10. Produce a count of the number of facilities that have a cost to guests of 10 or more.

11. Produce a list of the total number of slots booked per facility in the month of September 2012. Produce an output table consisting of facility id and slots, sorted by the number of slots.

12. Produce a list of facilities with more than 1000 slots booked. Produce an output table consisting of facility id and total slots, sorted by facility id.

13. How can you produce a list of the start times for bookings for tennis courts, for the date '2012-09-21'? Return a list of start time and facility name pairings, ordered by the time.

14. How can you produce a list of the start times for bookings by members named 'David Farrell'?

Answer:

```
1. SELECT * FROM cd.facilities

2. SELECT name, membercost FROM cd.facilities

3. SELECT * FROM cd.facilities WHERE membercost > 0

4. SELECT fA.facid, fA.name, fA.membercost, fA.monthlymaintenance FROM cd.facilities as fA
INNER JOIN cd.facilities AS fB
ON fA.facid = fB.facid WHERE fA.membercost > 0 AND fA.membercost < fb.monthlymaintenance * 0.02

5. SELECT * FROM cd.facilities WHERE name LIKE '%Tennis%'

6. SELECT * FROM cd.facilities WHERE facid IN (1, 5)

7. SELECT memid, surname, firstname, joindate FROM cd.members WHERE TO_CHAR(joindate, 'YYYY-MM') >= '2012-09'

8. SELECT DISTINCT surname FROM cd.members ORDER BY surname LIMIT 10

9. SELECT joindate FROM cd.members ORDER BY joindate DESC LIMIT 1

10. SELECT COUNT(*) FROM cd.facilities WHERE guestcost >= 10

11. SELECT facid, SUM(slots) FROM cd.bookings WHERE EXTRACT(MONTH FROM starttime) = '9' AND EXTRACT(YEAR FROM starttime) = '2012' GROUP BY facid ORDER BY SUM(slots)

12. SELECT facid, SUM(slots) FROM cd.bookings GROUP BY facid HAVING SUM(slots) > 1000 ORDER BY facid

13. SELECT bk.starttime AS start, fc.name FROM cd.bookings AS bk INNER JOIN cd.facilities AS fc
ON bk.facid = fc.facid WHERE fc.name LIKE '%Tennis Court%' AND DATE(bk.starttime) = '2012-09-21'

14. SELECT bk.starttime, firstname || ' ' || surname AS name FROM cd.bookings AS bk INNER JOIN cd.members AS ms ON bk.memid = ms.memid WHERE firstname || ' ' || surname = 'David Farrell' 
```
