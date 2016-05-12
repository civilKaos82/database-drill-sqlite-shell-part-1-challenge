# SQL Queries:  Part Orders

## Summary 
This challenge will build on the SQL queries that we've already written.  We'll be writing more complex queries making use of groupings, the [like operator][SQLite like operator] [SQLite aggregate functions][], and [subqueries][SQLite subqueries].


## Releases
### Pre-release:  Review the Schema
We're going to work with the database `orders.db`.  Get oriented by reviewing the `.schema`.  Take note of the tables and their columns.  It might help to break out the [Schema Designer][] and model the schema visually.


### Release 0: Where, Count, and Exporting

Create a list of all the students with straight hair.  How about curly hair?  How many students with curly hair are there?  How many students with straight hair?  Use the `COUNT` function.

Let's put the list of all the curly haired students in a file.  Type `.output curly_haired_students.txt`.  Now do the query for the curly haired students.  The list shouldn't be shown on your terminal, but it should now be saved in the file.

Type `.quit` and then `subl curly_haired_students.txt`.  You should see the big file of all the students with curly hair!  Make sure your `sql_history` file is there by typing `ls`.

Then start up the database again `sqlite3 students.db`.  Let's change the output back to the terminal or STDOUT.  Type `.output stdout`.

###Release 1: The LIKE method

Let's play around with SQLite's `LIKE` method.  It works similar to regular expressions, but with it's own syntax.  See if you can figure out the below calls:

Create a list of all the people with .com email addresses.  List only their names and their email addresses.  How many .com email addresses are there?  How many .info?

Find all the people that have a phone number with an extension.  (Look at the whole list to make sure you are matching the different variations of an extension - ie `x3467` or `x29987`)  Create an alphabetical list of all the people with an extension on their phone number AND have a ".com" email address.

###Release 2: Group and Count

Create a count of the two hair types, curly and straight.  Use the `GROUP` method to create a nice clean output that shows just the hair type and count.  Like this:

```
hair type      COUNT(hair_type)
----------  -------------
curly          516
straight       484
```

This is trickier... You may have to search up the answer or ask your fellow boots!

###Release 3: Ordering and Limiting

Order everyone by birthdate in ascending order.  Order alphabetically by last name.  Now first name?  Now list only the first and last names and their birthday.  And then order those names by birthdate in descending order!

Then list just the oldest 10 students.  Now list the youngest 10 students.

Is the SQL coming back to you?  Find a cheat sheet for reference if you need to!

Quit out of sqlite, do `subl sql_history.txt`, and paste the history of all your SQL commands into the source file `sqllite_shell_1.md`.  Add comments to organize these commands. 
 

##Optimize Your Learning 

##Resources


[Schema Designer]: https://schemadesigner.devbootcamp.com
[SQLite aggregate functions]: https://www.sqlite.org/lang_aggfunc.html
[SQLite like operator]: http://www.tutorialspoint.com/sqlite/sqlite_like_clause.htm
[SQLite subqueries]: http://www.techonthenet.com/sqlite/subqueries.php

