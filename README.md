# React interview questions

## Virtual DOM

### 1. Differentiate between Real DOM and Virtual DOM.

The Real DOM is always tree-structured. The DOM trees are huge nowdays because of large apps. We need to modify the DOM tree a lot of times. And this a real perfomance and development pain. 

The Virtual DOM is abstraction of the Real DOM. It is lightweight and detached from the browser-specific implimentation details. Its not invented by React but it uses it and provide it. ReactElements lives in Virtual DOM. They make basics nodes here. Once we defined the elements, ReactElements can be reder into Real DOM.

#### Real DOM
- Real DOM updates slow
- Can directly update HTML
- Creates new DOM elements if  elements updates
- DOM manipulations is very expensive
- To much memory wastage

#### Virtual DOM
- Virtual DOM updates fast
- Can't directly update HTML
- Updates JSX if elements updates
- DOM manipulations is very easy
- No memory wastage

## React 

### 2. How React works?

React creates a virtual DOM. When state changes in a component it firstly runs a "diffing" algoritm, which identifies was changed on the Virtual DOM. The second step is reconciliation, where it updates the DOM with results of diff.

### 3. What is JSX?

JSX is a syntax extension to JS and comes with the full power of JavaScript. JSX produces React elements. You can embed any JavaScript expresion in JSX by wrapping it in curly braces. After compilation, JSX expressions become regular JS objects. This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions. Eventhough React does not require JSX, it is recommended way to describing our UI in React app.

### 4. What is ReactDOM?

React DOM is the glue between React and the DOM. Often we use it for one single thing: mounting with ReactDOM. Another useful feature of ReactDOM is ReactDOM.findDOMNode() which we can use to gain direct access to DOM elements.

### 5. What the difference between state and props?

The state is data structure that starts with a default value when a Component mount.

Props are a Component's configuration. Props are how components talks to each other. They are received them is concerned. A Component cannot change its props, but it is responsible for putting together the props of its child Component. Props do not have just to be data - callback functions may be passed in as props.

### 6. What are controlled components? 

In HTML, form elememts such as input, select, textarea have their owen state and update it based user input. When user submits a form the values of this elements are sent with the form.
With React it works differently. The component containing the form will keep track of the value of the input in its state and will re-render the component each time the callback function is fired as the state will be update. A form element whose value is controlled by React in this way callend a "controlled component".

### 7. What is a higher order component?

A HOC is an advanced technique in React for reusing component logic. HOCs are not part of the React API. They are a pattern for reuse code, logic, and bootstrap astraction. They takes a component and returns a new component. The most common is Context and Redux's connect function.
