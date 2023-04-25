# Putting it all together

* **What is the single responsibility principle and how does it apply to components?** The single responsibility principle states that a piece of code (object or function) should only do one thing. If the object or function grows past this it should be broken down in to smaller pieces. The same principle applies to components in react.

* **What does it mean to build a ‘static’ version of your application?** A static version of an application is just a UI that used your data to draw the components but doesn't use state to make the project interactive

* **Once you have a static application, what do you need to add?** You need to add interactivity by adding state and event listeners to your application.

* **What are the three questions you can ask to determine if something is state?** Does the data remain unchanged overtime? It's not state. Is it passed from a parent via props? It's not state. Can you compute it based on existing state or props? It's not state.

* **How can you identify where state needs to live?** Find the all components that are dependent on the state. Find their common parent. Choose where the state should live

* **What is a “higher-order function”?** Functions that operate on other functions by taking them as arguments or returning them.

* **Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?** returning an arrow function that takes in an argument m and returns the result of m < n where n is the argument passed into the outer function.

## Things I want to know more about 