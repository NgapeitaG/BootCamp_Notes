# Monday the 4th of February 2019

Yarn run - show you each of the scripts which are in it.

## Dev Dependancies

Superagent: is basically so we can consume our routes from the client side. This is our bridge which sits between our client and server.
Supertest is using superagents methods.

## res.json 
 its utilities stringily.json which means to take a javascript object and convert it to a json object and send it as a string. 
It serialises our javascript object, turns it into a string, then calls res.send.

Don’t forget to type in your route your want to display in your browser’s URL.

Curl is going to send a request without a visual browser. Will send a get request and returns the data. 

## Postman  
  Postman is a program which you can find on the DevAcademy computers
	•	Enter request URL, select get request and then send

Increments have a memory of all the user ID’s


## Router.post

db.addUser = 
.then(console.log) // will show the most recently added ID
.catch // lets you fail gracefully
.end() // sends back an empty response
router.put // its for updating a resource
.delete() //deletes entry in database
router.delete //
res.status //

### More info on these topics: https://harakeke-2019-handbook.herokuapp.com/week5/01-web-apis.html
