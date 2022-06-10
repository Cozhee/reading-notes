## Lesson 1 SELECT queires 101
We use these types of queires to retrieve data from a database. An example statement would look similiar to something like `SELECT * FROM restaurants`. Essentially what this query does is select all (*) entires from the restaurants table.

## Lesson 2 Queries with constraints (Pt. 1)
From our queires we can add a constraint to only return us data that we need. This is necessary for large data sets for performance among many other reasons. One example is to use something called the `WHERE` clause. `SELECT name FROM people WHERE name="cody"`. You can have multiple constraints on a single query and can even use the `AND` and `OR` clauses.

## Lesson 3: Queries with constraints (Pt. 2)
Within the constraints you also have comparison operators that can do a number of things. Just to list a few we have `=`, `!=`, `<>`, `LIKE`, `NOT LIKE`, `%`, `IN`, and `NOT IN`. These are just a few and most operators names are descriptive of their actions.

## Lesson 4: Filtering and sorting Query results
With large datasets sometimes our queries can return duplicate data which would not be ideal. In these cases we have a keyword `DISTINCT` that will blindly remove any duplicate values returned in our query. `LIMIT` is an excellent clause to use when you want to only return a specific amount of results from your query. For example `LIMIT 4;` will only return 4 entries. Using the `OFFSET` command will specify where to start counting.

## Lesson 5: Practice
Practice all the commands we just learned!

## Lesson 6: Multi-table queries with JOINs
Multi-table queries can be a little bit more complex but once you understand the syntax are actually powerful and straight forward. Lets say for example we have two tables, `Movies` and `Boxoffice`. We need to select the columns that we want to display from BOTH tables when we join them. So for this example we will use `title`, `domestic_sales`, and `international_sales`. Just making the assumption these tables have these columns. So, `SELECT title, domestic_sales, international_sales` next we join the tables, `FROM movies JOIN boxoffice ON movies.id = boxoffice.movie_id` 
