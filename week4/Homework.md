## Homework Week 4

You must have done the [SQL Bolt online tutorials 1-4](https://sqlbolt.com/lesson/introduction) first.

Upload 2 files.  Do the quiz.

### Excel export:

Do a query in the database, save it as CSV, and import it to excel and fix the types.

Find the customer id, invoice date, and total from the invoices table in Chinook. You will do a single SELECT statement for this. Your query should order it by Total, descending. Export this to csv or tab-separated text format from your client.  Import it into Excel. Set the number format (remember this has decimal separator of "." not ",") and the date format during the import, or after import.  Save it as Excel format.  We will be checking if the types are correct (numbers are numbers, and dates are dates.)  You can verify if your numbers are numbers by checking if they have a sum.

### Queries Using Chinook Database:

You will return me a PLAIN TEXT FILE (not Word, not .rtf format) of just the queries, not the data results, exactly as you ran them, with “;” at the end of each one. You can label each one with a comment using "--" in front of it. (See screenshot below.) I will run them too, and if one doesn’t run, you won’t get credit, so make sure they all run.  Example contents:

<img src="assets/Homework-a856f.png">

("Use Chinook" means we are using that database for our queries. Most clients don't require it because you pick the database from a menu.)

* 1.A query returning the lastname, firstname, hiredate, and title for the employees. Sort by hire date, descending (most recent first).

* 2.A query returning lastname and firstname, plus postal code, for customers in france or germany. sort by lastname ascending.

* 3.A query to return the 10 longest songs in Tracks with unit price of 0.99. sort by length descending.

* 4.A query to select the tracks with a length between 230000 and 240000 milliseconds. sort by length descending.

* 5.Select the tracks where the genre id is 20 and the album id is 253. Order by track id ascending (lowest number first).

There will be quiz questions on the results of these queries and on aspects of databases from the week's lesson.

Save this file of queries with a .sql ending, like "LynnQueries.sql" and upload it.
