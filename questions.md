Please prepare an auto-complete component in React TypeScript.
	https://github.com/gustabin/autocomplete_api.git

1. What is the difference between Component and PureComponent? give an
example where it might break my app.
	If you use React.Component , the child component also re-renders if the parent component re-renders itself, but in React.PureComponent the child component only re-renders if the props passed to it changed.

2. Context + ShouldComponentUpdate might be dangerous. Can think of why is
that?
	Using libraries that use context might get you into trouble when combined with other libraries likewhen combining with your own shouldComponentUpdate.

3. Describe 3 ways to pass information from a component to its PARENT.
	One way is to pass a function as prop to the child component and have the child component call this function passing as an argument the value that the parent component needs.
Another option would be to use some state handler for React like redux.
And using Lifting, which is a technique that consists of passing functions to the children and letting them be in charge of executing them when necessary, causing an upward change in the parents.
We can send data from a child React component to the parent component by passing a function from the parent to the child. Then, in the child component, we can call it with the arguments we want to pass the values of the arguments to the parent component. 

4. Give 2 ways to prevent components from re-rendering.
	You can include expressions in JSX by wrapping them in braces. This includes the JavaScript logical && operator. It can be useful to conditionally include an element.
Another method for conditional rendering of elements in a line is to use the conditional operator condition ? true : JavaScript false.
It is also rendered depending on the value of the prop. If the value of the prop is false, then the component is not rendered.
if (!props.warn) {
    return null;
}

5. What is a fragment and why do we need it? 
	Fragments allow you to bundle a list of children without adding extra nodes to the DOM.
It is needed whenever there are multiple elements and they must be wrapped in an attached tag.

6. Give 3 examples of the HOC pattern
	Loader
	Fetch
	ContentList


7. what's the difference in handling exceptions in promises, callbacks and
async...await.
	Promises handle code that will be executed in the future just like callbacks. However, the difference is in the promise mechanism.
Await pauses until the promise resolves. It literally makes the execution of the async function wait until the promise resolves and returns a value, although this does not stop the language engine.

8. How many arguments does setState take and why is it async.
	Can take 2 arguments.
The setState function is asynchronous. Since setState calls are batch, this allows you to chain updates together.

9. List the steps needed to migrate a Class to Function Component.
	Separate the state for each concept.
Encapsulate user-related functionality in a custom hook.
Define a parent component.
Define a child component that will display user information.
By using hooks we can group all this functionality into a single function and use useEffect.

10. List a few ways styles can be used with components.
	Directly putting the object inside the style attribute or the other is to create a variable and assign it to the style attribute.
The styles in a constant, which is passed to the elements.
Importing a CSS file is another way to add styles to your app.
Another option is to generate a style sheet for each component.

11. How to render an HTML string coming from the server.
	In our app's index.js file, we'll use ReactDOM's hydrate method instead of render to tell the DOM renderer that we're rehydrating the app after a server-side render.

