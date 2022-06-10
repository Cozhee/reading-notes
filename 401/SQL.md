## Lesson 1 SELECT queires 101
We use these types of queires to retrieve data from a database. An example statement would look similiar to something like `SELECT * FROM restaurants`. Essentially what this query does is select all (*) entires from the restaurants table.
<img width="1168" alt="Screen Shot 2022-06-09 at 4 58 53 PM" src="https://user-images.githubusercontent.com/55909913/172994955-03294185-a2f9-4ee2-9160-dbc6bec4e110.png">

## Lesson 2 Queries with constraints (Pt. 1)
From our queires we can add a constraint to only return us data that we need. This is necessary for large data sets for performance among many other reasons. One example is to use something called the `WHERE` clause. `SELECT name FROM people WHERE name="cody"`. You can have multiple constraints on a single query and can even use the `AND` and `OR` clauses.

## Lesson 3: Queries with constraints (Pt. 2)
Within the constraints you also have comparison operators that can do a number of things. Just to list a few we have `=`, `!=`, `<>`, `LIKE`, `NOT LIKE`, `%`, `IN`, and `NOT IN`. These are just a few and most operators names are descriptive of their actions.

## Lesson 4: Filtering and sorting Query results
With large datasets sometimes our queries can return duplicate data which would not be ideal. In these cases we have a keyword `DISTINCT` that will blindly remove any duplicate values returned in our query. `LIMIT` is an excellent clause to use when you want to only return a specific amount of results from your query. For example `LIMIT 4;` will only return 4 entries. Using the `OFFSET` command will specify where to start counting.

## Lesson 5: Practice
Practice all the commands we just learned!

## Lesson 6: Multi-table queries with JOINs
Multi-table queries can be a little bit more complex but once you understand the syntax are actually powerful and straight forward. Lets say for example we have two tables, `Movies` and `Boxoffice`. We need to select the columns that we want to display from BOTH tables when we join them. So for this example we will use `title`, `domestic_sales`, and `international_sales`. Just making the assumption these tables have these columns. So, `SELECT title, domestic_sales, international_sales` next we join the tables, `FROM movies JOIN boxoffice ON movies.id = boxoffice.movie_id`. This can be a bit confusing but lets take note of `boxoffice.movie_id`. The first part `boxoffice` is just the reference to the table, so our second table! `movie.id` is the properties on the table!

## Lesson 13: Inserting rows
Take for instance we have a new user that we are adding to our database. We need to somehow insert them into our schema! The syntax for this would look something similar to `INSERT INTO <tablename> (columnName, columnName) VALUES (value1, value2, etc..)`. Although this can look to be simple it can sometimes be frustratating just based on types or inserting things like dates or time. This part can be very pick but this is important to keep our schema consistent and secure.

## Lesson 14: Updating rows
Updating rows in a table is somewhat similar to inserting a row. Although the syntax is different it should be straight forward. This is a common task which can be accomplished using the `UPDATE` command. It is common to make mistakes when working with data so having this tool is very handy. Using the syntax `UPDATE <tableName> SET <column> = <your-value> WHERE <your-condition>`. You must pay extra attention when writing these queries in order to maintain consistent data.

## Lesson 15: Deleting rows
The command `DELETE FROM <tableName> WHERE <your-condition>` is a straight forward command to delete entires in your database. Make sure to add in a `WHERE` clause or else you will end up deleting all of your data in a table. Although this is a good method to completely clear out a table it can also be a disatrious one.

## Lesson 16: Creating tables
Creating tables is where you will start to define your database schema. You will label your table names as well as define the type of data each table will represent. Being detailed in this step is cruical to have an air tight database. In order to create a table you run the following command, `CREATE <tableName> (<name> <type> <options>)`. I know this might look a little confusing. But I promise it is easy! [Here](https://sqlbolt.com/lesson/creating_tables) is a quick reference to really see what a simple example looks like! 
 
## Lesson 17: Altering tables
As data expands we need to adapt and have a database to represent our product. Luckily there is an alter command to help us with that! It is similar to creating a row, so here is the syntax, `ALTER TABLE <tableName> ADD column <constraints> DEFAULT <value>`. Confusing I know. That is only because of my examples. So instead [here](https://sqlbolt.com/lesson/altering_tables) is another great reference to see what I mean! My example shows just one simple way to alter a table. There are many more commands you can give after `ALTER` to do all kinds of things.

## Lesson 18: Dropping tables
This last lesson is very straight forward and a simple but deadly command. `DROP TABLE <tableName` will simply destory your table. Deleting all data from existence. This can be a simple process with a table that isnt related to any other table but it can start to get a bit tricky once you start having references. 
