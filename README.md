# SQL Queries:  Part Orders

## Summary 
This challenge will build on the SQL queries that we've already written.  We'll be writing more complex queries making use of groupings, the [like operator][SQLite like operator] [SQLite aggregate functions][], and [subqueries][SQLite subqueries].


## Releases
### Pre-release:  Review the Schema
We're going to work with the database `orders.db`.  Get oriented by reviewing the `.schema`.  Take note of the tables and their columns.  It might help to break out the [Schema Designer][] and model the schema visually.


### Release 0:  Query the Database
For each of the data requests below, write a single SQL query that will retrieve the requested data. Copy the working query for each request to the file `queries.md`.

If we want to double-check the results of our queries, each desired result set is recorded as a CSV file in the query_results directory—viewing the CSV files on GitHub will present them as nicely formatted tables.


1. Generate a report for parts ordered more than five times. The report should contain the number of times the part has been ordered, the part name, and the part code.  Order the data by the number of times the part was ordered from most to least and then alphabetically by name.

2. Our Engineering Department has designed a new part that needs to be made of copper.  We want to contact our suppliers who produce copper parts to get quotes for how much each would charge to make the part.  Generate a report with the name and phone number of any supplier from whom we've ordered copper parts.  Order the data alphabetically by supplier name.

3. For whichever part we've ordered most frequently, generate a report on the delivery performance of each time the part was ordered.  Include the part's id, the part's name, the order invoice number, the supplier's name, the date the part was ordered, the date the part was expected, the date the part was received, and the number of days the delivery was late.  Order the data based on the order date beginning with the most recent order.

  *Note:* Don't hardcode values related to the part ordered the most times.
  
4. We want to review the delivery performance of our most frequent suppliers.  Generate a report with the names of any suppliers from whom we've ordered more than twenty parts.  Include the average number of days late that that each supplier's parts were received.



Let's play around with SQLite's `LIKE` method.  It works similar to regular expressions, but with it's own syntax.  See if you can figure out the below calls:

2. Create a list of all the people with .com email addresses.  List only their names and their email addresses.  How many .com email addresses are there?  How many .info?

3. Find all the people that have a phone number with an extension.  (Look at the whole list to make sure you are matching the different variations of an extension - ie `x3467` or `x29987`)  Create an alphabetical list of all the people with an extension on their phone number AND have a ".com" email address.

4. Create a count of the two hair types, curly and straight.  Use the `GROUP` method to create a nice clean output that shows just the gender name and count.  Like this:

```
hair type      COUNT(hair_type)
----------  -------------
curly          516
straight       484
```

This is trickier... You may have to search up the answer or ask your fellow boots!

5. Order everyone by birthdate in ascending order.  Order alphabetically by last name.  Now first name?  Now list only the first and last names and their birthday.  And then order those names by birthdate in descending order!

6. Then list just the oldest 10 students.  Now list the youngest 10 students.
 

##Optimize Your Learning 

##Resources


[Schema Designer]: https://schemadesigner.devbootcamp.com
[SQLite aggregate functions]: https://www.sqlite.org/lang_aggfunc.html
[SQLite like operator]: http://www.tutorialspoint.com/sqlite/sqlite_like_clause.htm
[SQLite subqueries]: http://www.techonthenet.com/sqlite/subqueries.php

