# Read: 37 Summary
## React
* React : A JavaScript library for building user interfaces
* JSX produces React “elements”. 
* React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and 
how the data is prepared for display.
* Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units
called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, 
this talk might convince you otherwise.

* React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React
to show more useful error and warning messages.
* Elements are the smallest building blocks of React apps.

* Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.
* React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie:
it represents the UI at a certain point in time.
* React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.
* Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. This page provides an introduction to 
the idea of components. You can find a detailed component API reference here.
* Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing 
what should appear on the screen.
* Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form,
a dialog, a screen: in React apps, all those are commonly expressed as components.
* This component can be tricky to change because of all the nesting, and it is also hard to reuse individual parts of it. Let’s extract a few components from it.

* All React components must act like pure functions with respect to their props.

#### Converting a Function to a Class
* You can convert a function component  to a class in five steps:

  * Create an ES6 class, with the same name, that extends React.Component.
  * Add a single empty method to it called render().
  * Move the body of the function into the render() method.
  * Replace props with this.props in the render() body.
  * Delete the remaining empty function declaration.

* Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

  * React events are named using camelCase, rather than lowercase.
  * With JSX you pass a function as the event handler, rather than a string.














