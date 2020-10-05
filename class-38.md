# Read:38 Summary
## React part.2
* In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them, depending on the state of your application.
* `Conditional rendering` in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create 
elements representing the current state, and let React update the UI to match them.
* Just like in JavaScript, it is up to you to choose an appropriate style based on what you and your team consider more readable. Also remember that whenever
conditions become too complex, it might be a good time to extract a component.
* Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements 
a stable identity
* The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys
* When you don’t have stable IDs for rendered items, you may use the item index as a key as a last resort
* Keys only make sense in the context of the surrounding array.
* Keys used within arrays should be unique among their siblings. However they don’t need to be globally unique. We can use the same keys when we produce 
two different arrays
* HTML form elements work a little bit differently from other DOM elements in React, because form elements naturally keep some internal state.
* n most cases, it’s convenient to have a JavaScript function that handles the submission of the form and has access to the data that the user entered 
into the form. The standard way to achieve this is with a technique called “controlled components”.
* In HTML, form elements such as <input>, <textarea>, and <select> typically maintain their own state and update it based on user input. In React, mutable
state is typically kept in the state property of components, and only updated with setState().
* We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what 
happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.
* With a controlled component, the input’s value is always driven by the React state. While this means you have to type a bit more code, you can now
pass the value to other UI elements too, or reset it from other event handlers.
* It can sometimes be tedious to use controlled components, because you need to write an event handler for every way your data can change and pipe all of
the input state through a React component. This can become particularly annoying when you are converting a preexisting codebase to React, or integrating 
a React application with a non-React library. In these situations, you might want to check out uncontrolled components, an alternative technique for
implementing input forms.
* Often, several components need to reflect the same changing data. We recommend lifting the shared state up to their closest common ancestor.
* There should be a single “source of truth” for any data that changes in a React application. Usually, the state is first added to the component
that needs it for rendering. Then, if other components also need it, you can lift it up to their closest common ancestor. Instead of trying to
sync the state between different components, you should rely on the top-down data flow.
* Lifting state involves writing more “boilerplate” code than two-way binding approaches, but as a benefit, it takes less work to find and isolate 
bugs. Since any state “lives” in some component and that component alone can change it, the surface area for bugs is greatly reduced. Additionally,
you can implement any custom logic to reject or transform user input.
* React has a powerful composition model, and we recommend using composition instead of inheritance to reuse code between components.

* Composition works equally well for components defined as classes
* At Facebook, we use React in thousands of components, and we haven’t found any use cases where we would recommend creating component inheritance hierarchies.

* Props and composition give you all the flexibility you need to customize a component’s look and behavior in an explicit and safe way. Remember that
components may accept arbitrary props, including primitive values, React elements, or functions.
* If you want to reuse non-UI functionality between components, we suggest extracting it into a separate JavaScript module. The components may 
import it and use that function, object, or a class, without extending it.
* React is, in our opinion, the premier way to build big, fast Web apps with JavaScript. It has scaled very well for us at Facebook and Instagram.

* One of the many great parts of React is how it makes you think about apps as you build them. In this document, we’ll walk you through the thought
process of building a searchable product data table using React.
* To build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data
using props. props are a way of passing data from parent to child. If you’re familiar with the concept of state, don’t use state at all to build 
this static version. State is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, 
you don’t need it.
* To make your UI interactive, you need to be able to trigger changes to your underlying data model. React achieves this with state.

* To build your app correctly, you first need to think of the minimal set of mutable state that your app needs. The key here is DRY: Don’t 
Repeat Yourself. Figure out the absolute minimal representation of the state your application needs and compute everything else you need on-demand.
For example, if you’re building a TODO list, keep an array of the TODO items around; don’t keep a separate state variable for the count. Instead, when 
you want to render the TODO count, take the length of the TODO items array.
* For each piece of state in your application:
  
  * Identify every component that renders something based on that state.

  * Find a common owner component (a single component above all the components that need the state in the hierarchy).

  * Either the common owner or another component higher up in the hierarchy should own the state.

  * If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it 
  somewhere in the hierarchy above the common owner component.

  * React makes this data flow explicit to help you understand how your program works, but it does require a little more typing than traditional two-way data binding.

















































