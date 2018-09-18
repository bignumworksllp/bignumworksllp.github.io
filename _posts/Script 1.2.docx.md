**Video 1.2**

**Slide - Video Introduction**

Welcome to the video - Managing data with databases (sqlite3 recipes)

In this video, we are going to learn how to interact with sqllite3
databases using python. We will show the tricks for how to make a
connection, how to create tables, how to insert records and few other
actions with sqlite3 actions using python.

**Slide – Demo**

**Jupyter Notebook**

SQLite3 can be integrated with Python using sqlite3 module. You do not
need to install this module separately because it is shipped by default
along with Python version 2.5.x onwards.

We start with importing the sqlite3 module.

To use sqlite3 module, you must first create a connection object that
represents the database and then optionally you can create a cursor
object, which will help you in executing all the SQL statements.

There are no server processes involved, no configurations required, and
no other obstacles we have to worry about.

Conveniently, a new database file (.sqlite file) will be created
automatically the first time we try to connect to a database. However,
we have to be aware that it won’t have a table, yet.

If we are finished with our operations on the database file, we have to
close the connection via the .close() method:

And if we performed any operation on the database other than sending
queries, we need to commit those changes via the .commit() method before
we close the connection:

**Slide - Next Video**

This concludes this video. In this video, we

In the next video, we will learn how to Acquire data from web using
urllib/xmllib/json

**------------------------- end ---------------------**
