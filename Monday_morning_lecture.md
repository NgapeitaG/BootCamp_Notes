Week 4:

Monday the 28th of January 2019

React - 

Server- side and client-side rendering:

Client-side = in the browser
Server-side = express 

Bundle.js = has react, all our templates. It has everything in it. 

DOM = is a hierarchy of nodes. It’s an in memory representation of a webpage.

	•	React allows us to make our changes directly to the DOM


Why single page apps?

	•	User experience is huge.



Render a simple component:

	•	JSX - the combination of a html looking syntax and javascript. It’s a syntax that looks like html. It’s an html placeholder.
	•	props.name
	•	react native - build apps and webpages with react
	•	react-dom
	•	rendering views to a template


	•	React came out six years ago
	•	yarn install, yarn start

Difference between HTML & JSX:
	•	div class = div classname (JSX)
	•	<img src=“” />    use /> for input tags, image tags, br, hr etc.
	•	when you have a component, it has to has a single parent
	•	templates is called a component in react
	•	usually start with a DIV

Import and export:
	▪	Capitalize file name and function name for components. Name the component name the same as the function name.
	▪	We’re not using require anymore.
	▪	To require a react file, type = import React from ‘react’ & import ReactDOM from ‘react-dom’
	▪	Export components - export default Hello (name of component) This export function is in the file where the actual function you’re exporting is.
	▪	import Hello from ‘./components/Hello’

Render props:
	•	components are designed to be composed
	•	every part of the webpage will be a component
	•	<Animal />  This will render inside of the Hello function
	•	defines props as attributes
	•	props is an object
	•	When we capitalise our components in our files, react will be able to identify what it’s responsible for rendering. Anything lowercase is built into a react. Every component must be capitalised.
	•	{props.name} one curly, not two curly’s as a handlebar.
	•	You can pass arrays, objects as props, not just strings


Transpiling with web pack:
	•	babel transpiles code. 
	•	transpiling is going from human readable code to what the javascript interpreter can read. From ES6 to an older version of javascript.
	•	Browsers understand ES3
	•	Babel will transpire our code into older code.
	•	build = transpire
	•	web pack is a bundler
	•	babel is a transpiler
	•	babel-loader = connects babel with webpack

webpack is a tool capable of running our code through a loader, such as Babel, and bundling all files into a single file. Using webpack is primarily about configuring the loaders and folder locations. In order to cover the basics, we'll work through the ES6 webpack tutorial.


Hide and show components (conditional components):
	•	<app/>
	•	&& = shortcut operator 
	•	The .jsx files have the things we’re going to see in the browser and index.js has inserts of the components.



For the map function, in the parenthesis, we put what ww want to be returned in the new array which will be returned.

Styling in jsx = {{}} use double curly braces 

Ternary operator:
? <Animal /> (if this is truethy, we see the animal component)
: <Colors /> (if not, return the colours component)

Ternary operator: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator

Class-based components:
class Animal extends React.Component {
	Render ( ) {

	}
}

	•	A functional component is just for rendering. It’s a subset of a class based component.
	•	In order to get the props, we can use this.
	•	this refers to the object that this class is going to create.
	•	In a class based component, we have to use this.props, in a functional component, we can access props directly.

Virtual DOM:
	•	When we make a change to a DOM, the browser has to recalculate
	•	react has a copy of the DOM (a map of the same thing). It can make changes and not affect them original DOM.
	•	is used for performance and making changes to the browser.

	•	key= 
Is used to make every item in a list unique

Play around with turinary operator, .map, key= etc…

Try things out and be curious. Not knowing what the outcome will be.

LOOK AT TODAYS CODE FROM CLASS AND LEARN HOW THE CODE IS CONNECTING AND RETURNING THE RESPONSE TO THE BROWSER!	



