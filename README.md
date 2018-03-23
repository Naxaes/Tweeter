# Tweeter

This is a project for the SQL-course at [Ludu.co](https://www.ludu.co/course/learn-sql).


## Setup

The application uses python 3 and 4 external libraries:
* **flask** - For setting up the server.
* **wtforms** - For easily creating forms.
* **psycopg2** - For inteacting with our database.
* **passlib** - To hash and salt passwords.


You'll also need four tables in your database:
* Users(**userID**, username, email, age)
* Tweets(**tweetID**, posterID, content, time_posted)
* Followers(**userID**, followerID)
* Passwords(**userID**, password)


You can download the libraries and create the tables manually, or by running `setup.py`. The file will download the libraries and create an `create.sql` file with all tables. It'll also create 4 CSV-files with compatible data for each table.


## Running the application

To run the application, simply run _application.py_. By default, all functionality will be limited, as it is expected you provide the functionality yourself by filling in the functions in the file _exercise_queries.py_.

If you want to run the full-featured application, change the import in _applications.py_ from "from exercise_queries ..." to "from solution_queries ...". 

## Common errors
* **The application throws the error "Did you remember to start your server?".**

If you want to run the full-featured version, you'll have to start the server. This is done by launching psql and connecting to the database.

Another possible solution is to change the arguments to the database class in the file _solution_queries.py_, as they are hardcoded to work for those who follow the course. Change these values to the default values given to you when you run psql (those in square brackets below):

![image](https://imgur.com/54Dq2XV)
