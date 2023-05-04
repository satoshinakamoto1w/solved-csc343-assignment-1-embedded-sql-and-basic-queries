Download Link: https://assignmentchef.com/product/solved-csc343-assignment-1-embedded-sql-and-basic-queries
<br>



Part 1. Database design and implementation

1.1. Create an E/R diagram of the CEA database

1.2. Convert this diagram into a relational schema. Specify all basic attribute types. Specify all primary keys.

1.3. Think of and list all required value constraints on course codes, department codes, start and end dates, course grades, year, ranking, semester, time of day, gender, and anything else you can think of to prevent inconsistent data from being added to the database.

1.4. Convert your logical CEA schema into a physical schema – set of tables with constraints – using the PostgreSQL DBMS. Learn how to create new data types such as <u><a href="https://www.postgresql.org/docs/9.1/static/sql-createdomain.html">domains</a></u> and <u><a href="https://www.postgresql.org/docs/9.1/static/datatype-enum.html">enums</a></u> and apply this knowledge to restrict the domains of each data column.

1.5. Now, recall all the courses you have taken so far, and write and run SQL insert statements for inserting data about departments, courses and the instructors you encountered during your study at UofT.

1.6. Write all the required insert statements to enter complete information for two students (you and your project partner).

1.7. After this task is complete, convert your physical schema into an equivalent schema for SQLite. Record and report all the difficulties that you encountered during this process. Are there any constraints that you were not able to enforce in SQLite?

1.8. If you performed tasks 1.5 -1.6 accurately, the same insert statements should also work for SQLite. Insert your initial data into an SQLite database using your sql script for insertions.<strong>           </strong>

<h1>Part 2. SQL embedded into a JDBC application</h1>

2.1. Create a Java application which provides an interface to enter user experiences into an SQLite version of the CEA database. A student who was previously added to the database, should be able to identify himself, to select a course from a list of available courses, and to insert all the experiences described in the specification.

2.2. Use the interface (either GUI or TUI) to truthfully and accurately record your own experiences about each course you have taken.

2.3. In order to perform meaningful data analytics in the second assignment, we will combine all the information you entered into a single database. Towards this goal, write an export utility which will perform basic select-project-join operations on all your data tables, and will output the data as a single report in a (comma-separated) csv format.

Each row in this table should contain complete information about a particular (course edition – user name pair). The column headers are as follows (be precise):

<ul>

 <li>Course number (with department code)</li>

 <li>Course start date</li>

 <li>Course end date</li>

 <li>Time of day</li>

 <li>Total number of students</li>

 <li>Name of the course instructor(s): one or many delimited by |</li>

 <li>Student user name</li>

 <li>Course grade</li>

 <li>Student age</li>

 <li>Student year and month of birth, space delimited</li>

 <li>Student gender</li>

 <li>Student country of birth</li>

 <li>List of skills acquired outside academia in form of skill-rank pair, delimited by |</li>

 <li>Student start date at the University</li>

 <li>Course satisfaction</li>

 <li>Instructor ranking</li>

 <li>List of skills learned in the course: in form of skill – rank before- rank after, delimited by |</li>

 <li>List of topics learned in the course: in form of topic-interest before-interest after, delimited by |</li>

</ul>

All the rankings are numeric on the scale 1-5 (5 is the highest)