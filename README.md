# Birthdays-Reminder-Flask
Create a web application to keep track of friends’ birthdays.
<img src="https://i.imgur.com/KoRB6OV.png" width="1000px"/>


# Testing
Run flask run in your terminal while in your lab9 directory to start a web server that serves your Flask application.</br>


# Understanding
In application.py, you’ll find the start of a Flask web application. The application has one route (/) that accepts both POST requests (after the if) and GET requests (after the else). Currently, when the / route is requested via GET, the index.html template is rendered. When the / route is requested via POST, the user is redirected back to / via GET.</br>

birthdays.db is a SQLite database with one table, birthdays, that has four columns: id, name, month, and day. There are a few rows already in this table, though ultimately your web application will support the ability to insert rows into this table!</br>

In the static directory is a styles.css file containing the CSS code for this web application. No need to edit this file, though you’re welcome to if you’d like!</br>

In the templates directory is an index.html file that will be rendered when the user views your web application.</br>

# Implementation Details
 the implementation of a web application to let users store and keep track of birthdays.</br>

When the / route is requested via GET, your web application should display, in a table, all of the people in your database along with their birthdays.</br>
First, in application.py, add logic in your GET request handling to query the birthdays.db database for all birthdays. Pass all of that data to your index.html template.</br>
Then, in index.html, add logic to render each birthday as a row in the table. Each row should have two columns: one column for the person’s name and another column for the person’s birthday.</br>
When the / route is requested via POST, your web application should add a new birthday to your database and then re-render the index page.
First, in index.html, add an HTML form. The form should let users type in a name, a birthday month, and a birthday day. Be sure the form submits to / (its “action”) with a method of post.</br>
Then, in application.py, add logic in your POST request handling to INSERT a new row into the birthdays table based on the data supplied by the user.
Optionally, you may also:</br>

Add the ability to delete and/or edit birthday entries.</br>
Add any additional features of your choosing!</br>
