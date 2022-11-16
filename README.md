# Creating elements with React API
Basic use of React API for creating elements and rendering to the DOM

Using `React.createElement()` and `ReactDOM.createRoot()` to insert DOM element into the document and rendering.

* Get [React](https://unpkg.com/react@18.1.0/umd/react.development.js) and [ReactDOM](https://unpkg.com/react-dom@18.1.0/umd/react-dom.development.js) on the page using [unpkg](https://unpkg.com/)
* React exposes a Universal Module Definition (UMD) that allows the creation of a global variable in the browser that can be referenced inside of the code

React allows you to create elements. These React elements are simple objects that describe the UI that you want to create. ReactDOM renders this UI to the page.

Use `React.createElement()` to create an element.
The arguments that `React.createElement()` accepts are `type`, `props`, `children`
e.g. `React.createElement('div', {className="container"}, "Hello World")`
alternatively you can set `children` as one of the object properties on `props`
e.g. `React.createElement('div', {className="container", children: "Hello World"})`
The children argument can also be an array of other elements
e.g.
```
const span1 = React.createElement('span', {key = 1}, "Hello")
const span2 = React.createElement('span', {key = 2, children: [" ", "World"] })
const reactElement = React.createElement('div', {className="container"},[span1, span2])
```
The element is rendered to the page using ReactDOM
```
const rootElement = document.getElementById("root")
ReactDOM.createRoot(rootElement).render(reactElement)
```
