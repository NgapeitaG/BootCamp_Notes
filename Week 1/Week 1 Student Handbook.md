# Week 1 Handbook notes:

	▪	Node.js lets you run javascript in the terminal
	▪	Yarn is a package manager. We use it to download, build, and install packages for use in our programs.
	▪	A package manager lets you use other people's JavaScript modules. It saves us having to write code from scratch, hence why we use Yarn. 
	▪	Yarn reads the package.json file in the root directory of your project. Of particular interest are the scripts and dependencies properties.

## Useful Yarn commands to understand:

	▪	yarn install - installs all the dependencies listed in your package.json file in a node_modules folder
	▪	yarn start - usually used to launch a server or other continuous development/debugging environment
	▪	[yarn test] - usually used to launch your test suite
	▪	yarn foo - looks for a script in your package.json called 'foo' (in this example) and runs it

You will see frequent references to npm, another package manager for Node. We use Yarn at EDA, but the two share many similarities and you will likely encounter both in the workplace.


## Node.js Documentation:


### fs.readFile(path[, options], callback)

	•	fs.readfile asynchronously reads the entire contents of a file
	•	The callback is passed two arguments (err, data), where data is the contents of the file.
	•	options is usually the encoding so options will be ‘utf8’. If no encoding is specified, then the raw buffer is returned = fs.readFile('/etc/passwd', 'utf8', callback);
	•	When the path is a directory aka a folder, an error will be returned using this node.js method = fs.readFile('<directory>', (err, data) => {
	});


### fs.readFileSync(path[, options])

	•	fs.readFileSync returns the contents of the path.
	•	The path can include a string, buffer, url or integer.
	•	If the encoding option is specified, then this function returns a string. Otherwise, it returns a buffer which is a whole lot of unreadable code = fs.readFileSync('<directory>');

## __dirname

	•	_dirname prints the directory name of the current module/file. This is the same as the path.dirname.

## __filename

	•	The file name of the current module. This is the current module file's absolute path with symlinks resolved.

## __path.join

	•	The path.join() method joins all given path parts together, then normalizes the resulting path.
	•	A TypeError is thrown if any of the path segments is not a string
		
### Example:

path.join('/foo', 'bar', 'baz/asdf', 'quux', '..');
// Returns: '/foo/bar/baz/asdf'

path.join('foo', {}, 'bar');
// Throws 'TypeError: Path must be a string. Received {}'


# Datatypes:

## Seven different datatypes in javascript:

	•	Six data types that are primitives:
	◦	Boolean
	◦	Null
	◦	Undefined
	◦	Number
	◦	String
	◦	Symbol (new in ECMAScript 6)
	•	and Object

## Typeof
	•	The typeof operator returns a string indicating the typeof the value you want to evaluate.
### Example:
console.log(typeof 'blubber');
// expected output: "string"

console.log(typeof true);
// expected output: "boolean"

Or

console.log(‘This is a ?: string, typeof types.str)
// Returns This is a ?: string string

This returns the datatype for the property str in the types const.	

# First-class Functions

	•	An important thing to remember about functions in JavaScript is: functions are values.
	•	We can store functions in variables
	•	We can store functions as properties of other objects
	•	Functions can have properties
	•	We can pass functions as arguments into other functions

# Data Structures

	•	If an object is too deep you can also tell it to give you its keys using the method Object.keys(). For example:
	Object.keys(response)
	Object.keys(response.query)
	•	You will encounter a lot of objects like this over the next few weeks. It's important to not be scared off, to feel comfortable exploring them.
	•	Try different approaches to get information out of objects.

	Testing with Jest
	
	Here’s a basic Jest test:

	test("test some basic js", () => {
  	expect(2+2 === 4).toBeTruthy()
  	expect(3*3).toBe(9)

  	const testArray = ['dave', 'sharon']
  	testArray.push('flora')

  	expect(testArray).toEqual(['dave', 'sharon', 'flora'])
	})

	•	Jest is the framework we use for testing our Javascript code
	•	It works with Babel, Typescript, Node, React, Angular, Vue and more.


## Query selector

		A querySelector() is a function which grabs a reference to an element in your HTML file such as the H1 heading, and then it gives you the ability to change that 				element.

## Example:

	var myHeading = document.querySelector('h1');
	myHeading.textContent = 'Hello world!';
	// Selects the ‘h1’ in your HTML file and changes the heading to ‘Hello world!’

### Variables
	Variables are containers that you can store values in. You start by declaring a variable with the var keyword, followed by any name you want to 	call it:
	var myVariable;

	After declaring a variable, you can give it a value:
	myVariable = 'Bob';

# Operators
	An operator is a mathematical symbol which produces a result based on two given values.
	Assignment = Assigns values to a variable
	Equality === Does a test to see if two values are equal to one another and returns a true/false result. E.g. 3 === 4 //Returns false
	Addition ➕ Adds two numbers or glues two strings together. 
	Subtraction, multiplication and division ➖✖️➗
	Not/does not equal !==	When it is used alongside the Equality operator, the negation (!) operator tests whether two values are not equal.
	! returns the opposite value of what it precedes. It turns a true into a false.

# Arguments
	Arguments are bits of data which functions need to do their job. They go inside the parenthesis() and are separated by comma’s if there are 		more than one argument. 

# Return
	The return statement tells the browser to return the result of anything happening 	inside the function brackets {}. When you 		run your function, it will automatically return the function. 

# Events
	Real interactivity on a website needs events.These are code structures which listen for things happening in browser, running code in response.
	The most obvious example is the click event, which is fired by the browser when you click on something with your mouse.

		A prompt function will bring up a dialog box, a bit like alert().
	⁃	localStorage allows us to store data in the browser and retrieve later on.
	
# Test-driven Development
	
	TDD is writing a test for a function/line of code before you’ve actually written it. By testing the outcome before you've written it, you 			plan more effectively exactly what that code needs to do.

	The goal is to write less code of higher quality, which is always great!

	How do we write TDD?
	RED // GREEN // REFACTOR
1. Name expectations in the first step
expect(addTwo(2)).toBe(4)

Here, I am asserting that when I pass 2 to the addTwo function, I expect the result to be 4. 

2. Next create the function you are asserting.
function addTwo (number) {
  return 4
}

expect(addTwo(2)).toBe(4)

3. Refactor
Refactoring is the process of improving the quality of the code without changing it's behaviour.
function addTwo (number) {
  return number + 2
}

We should always run the tests again after we've refactored to be sure we haven't accidentally broken something.

	Why test driven development is so important
	
	•	Makes us explicitly name our expectations
	•	Allows us to manage complexity in small chunks
	•	Supports refactoring with confidence
	•	Alerts us if we break something by mistake in the future

# Writing tests
	
	It's important that tests are clear, and state exactly what you expect the code to do. It's important that your tests are as clear as possible.

## Each test should be made up of 3 distinct parts:
	1	Arrange
	2	Act
	3	Assert

## example:
test('can create a 2x2 matrix', () => {
  // arrange
  const expected = [[0,0], [0,0]]

  // act
  const actual = makeEmptyMatrix(2)

  // assert
  expect(actual).toEqual(expected)
})


# Networking

	•	A server is often referred to as the physical or virtual machine. It's what responds when we visit a web site, sending us all the information our browser needs to display the site correctly. So basically, it’s in charge of getting data so that we can see those things in our browser as a webpage.

## A service:
	•	Listens for requests and then serves responses
	•	A web server is a service which serves web pages

## Ports:
	•	The particular 'door' at an address
	•	The connection to the application/service, such as HTTP, that is listening for requests
	•	e.g. port 3000
	•	Ports can have various numbers 
	•	More on ports: http://www.networksorcery.com/enp/protocol/ip/ports03000.htm

E.g. 
server.listen(3000, () => {

  console.log('Listening on port 3000...')

})
API:
	•	An API is a thing for computers to talk to each other
	•	


# Express.js

	•	Express makes it easy to create server-side web applications by providing an easy way to read and manipulate the HTTP requests and responses.
	•	the res parameter sends a response to the client.This is a Node.js response object that is provided through Express.
	•	server.get('/', (req, res) => {
	•	  res.send('<h1>Hello world</h1>')
	•	})
	// Responds with ‘Hello world’ when a get request is made to the root (‘/‘). It listens for connections on port 3000.
	•	The app.get() call allows us to define endpoints, also called routes, such as /. The server will only to respond to routes our application defines
	•	Scripts are another name for javascript files.
	
## Separation of concerns

	•	Routes are not related to running the server. 
	•	Routes should always be typed into their own file such as routes.js
	•	We can not only respond to our webpage with strings such as ‘Hello world’ but also with files. We use the res.sendfile method for this.
function home (req, res) {
  res.sendFile(__dirname + '/index.html')
}

## Route parameters

	Another way we can send data to the server from the client is by using route parameters.
	Example:
	app.get('/:org/:repo', function (req, res) {
  	res.send('Org: ' + req.params.org + ', Repo: ' + req.params.repo)
	})

## Serving static files

	All of our static files are put in a main file, usually the public file. Static files are files which should be sent directly to the browser 		without any modification. A good example of a static file are JPG’s and PNG’s.

	Static files aren’t rendered with a template engine.

	Instead of using res.sendFile to display every static file, we can just place them in the ‘public’ directory and use server.use or app.use. 		Look in the example below. 

### Example:
	const express = require('express')
const server = express()
server.use(express.static('public')) 
// This last line serves all the static files within the directory ‘public’.

	Now we can place a directory structure under a public folder for each type of static file we need to serve. This could create paths on our web application like:
	•	http://localhost:3000/images/logo.png
	•	http://localhost:3000/styles/main.css
	•	http://localhost:3000/scripts/tiles.js

# Debugging Node.js
	
	Node comes with a built in debugger you can use to inspect what is going on in your code.
	You can use it by putting debug after your node command. For example, node debug server.js
