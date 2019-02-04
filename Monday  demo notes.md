					    Monday the 21st of January 2019

		 (These are the notes which I took whilst watching a code from class demo video on youtube.)

# Week 3 - Code from class demo

## Databases:
	•	Create
	•	Read
	•	Update
	•	Delete
	•	Sequel
	•	knex.js
	•	Spreadsheet
- fields
- schema / metadata (The description of how the fields are gonna look)
- columns, rows, tables
- table entities
	•	Primary keys
	•	Foreign key

## Metadata (Schema)
Name of the table (Fields and columns)
- Types


# Data:

## Files vs servers

### Relational/ structured storage:
there’s a relationship shown between al the data

Started with yarn init -y
Yarn add knex 
Yarn knex init

- We will be using development in our knexfile.js
- 	useNullasDefault :true

-	Migration: is a script that we build out that will build our database (yarn knex migrate:make)
- exports.up (will build out a database schema
- exports.down (will get rid of it)

#### exports.up = function(knee, Promise) {
return knee.schema.createTable(‘tasks’ , (table) => {
table.increments(‘id’)
Increments creates a new data type
table.string(‘name’)
table.boolean(‘completed’)
})
}

#### exports.down = function(knee, Promise) {
return knee.schema.createTable(‘tasks’ , (table) => {
table.increments(‘id’)
table.string(‘name’)
table.boolean(‘completed’)
})
}

## The way in which we run these commands is:
$yarn knex migrate:latest

 Creates = dev.sqlite3

	•	You have to create tables in a sequence if there’s a relationship between tables. This is where foreign keys come in.

yarn knex seed:make
Yarn knex seed:run

index.js

const knee = require (‘knex’)
Const knexConfig = require(‘./knexfile’).developement

Const db = knex(config) This connects to our database

db(’tasks’) = references the tasks table
.select()
.then(tasks => {
tasks.forEach(task => {
console.log(task)
	})
})
	
.then(() => db.destroy()) (This will close our connection)

Selects our tasks tables, then grabs the tasks for each and returns them.



#### Website about Knex.js:
https://knexjs.org


Ask a tutor how would they commend we go over the concepts we’ve learnt so far. 
Should we go over the exercises or code from class?


### tasks.completed ( line 10 of index.js)
Will evaluate as truth or false. 


	•	Knex writes the Sql for you. 
	•	SQL is not taught to us
	•	It’s not really needed in web app

# Summary of concepts:
## Make and run migration
## Make and run seeds

### Exercise: Today we’re building a todo list

Use command b to format your file. It will fix indentations.

Check in and out with your pair. 

#### Be comfortable in a pair and be comfortable with going solo. 


	•	Migrations allow you to define sets of schema changes so upgrading a database is a breeze.
	•	Schema is the name of the table also known as metadata


