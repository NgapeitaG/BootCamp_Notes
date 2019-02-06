Wednesday the 23rd of January 2019

Database Relationships

Constraints:
Is our database having our back. Is your way how you tell your database how you want to setup your database.

Uniqueness:
Is an example of a constraint

Primary keys:
When you add a primary key this is your ID. It is a uniqueness constraint. They are one way of applying a uniqueness constraint. Always relates to a foreign key.

	•	One to many
	•	Many to many

Foreign keys:
Always connects to a primary key. 

On delete:
What you want to happen when you delete something


On update:
Normally you don’t update ID’s (less common)

RDBMS - (they use Sql)
Relational database management system


- doc (MongoDB)
- object
- graph


Relational database:
- it has tables 
- theres a relationship between the tables
- You can tell the database that you’re going to create this relationship between table

Entity relationship diagrams:
Communicates database structure. Only metadata/ schema. There’s is now data or rows. 

Products and categories:

	⁃	When db get’s called, it will use the value in the parenthesis 
e.g. (return db (users)

If we don’t pass anything in for db then it will use the default which is connection.

Last week:
Res.render (‘index’, {user:user})
- always render an object 

Up is applied when you do a migrate latest (do)
Down is applied when you do a migrate rollback

Steps:
	⁃	yarn
	⁃	yarn knex migrate:latest (apply migrations)
	⁃	yarn knex seed:run (apply data to our database)
	⁃	yarn start


.references(‘artists.id) (How to make a foreign key) This uses .references and points to the table.primary key.


Boilerplate: like a template document




