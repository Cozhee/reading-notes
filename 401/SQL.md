## Lesson 1 SELECT queires 101
We use these types of queires to retrieve data from a database. An example statement would look similiar to something like `SELECT * FROM restaurants`. Essentially what this query does is select all (*) entires from the restaurants table.

## Lesson 2 Queries with constraints (Pt. 1)
From our queires we can add a constraint to only return us data that we need. This is necessary for large data sets for performance among many other reasons. One example is to use something called the `WHERE` clause. `SELECT name FROM people WHERE name="cody"`. You can have multiple constraints on a single query and can even use the `AND` and `OR` clauses.

## Lesson 3: Queries with constraints (Pt. 2)
Within the constraints you also have comparison operators that can do a number of things. Just to list a few we have `=`, `!=`, `<>`, `LIKE`, `NOT LIKE`, `%`, `IN`, and `NOT IN`. These are just a few and most operators names are descriptive of their actions.
