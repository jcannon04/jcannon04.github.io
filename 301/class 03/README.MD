# Passing Functions as Props

* **What does .map() return?** A new array where each item is the value returned from the callback function.

* **If I want to loop through an array and display each value in JSX, how do I do that in React?** With .map() you can iterate though the an array of data and transform each item into a react component

* **Each list item needs a unique ____.** key

* **What is the purpose of a key?** To give each react component in a list a unique id so that react can recognize it regardless of the order of components in the list

* **What is the spread operator?** The spread operator is a syntax feature that allows you to break down an array into it's individual elements.

* **List 4 things that the spread operator can do.** Concat items onto an array. Convert an array like collection into an array. Break down an array into a list of function arguments. Make a shallow copy of an array.

* **Give an example of using the spread operator to combine two arrays.** 
    ```javascript
    let array1 = [1, 2, 3];
    let array1 = [4, 5, 6];
    let combinedArray = [...array1, ...array2]
    ```
* **Give an example of using the spread operator to add a new item to an array.**
    ```javascript
    let array = [1, 2, 3];
    let item = 4;
    let combinedArray = [...array, item]
    ```
* **Give an example of using the spread operator to combine two objects into one.**
    ```javascript
    let name = {firstName: 'Josh', lastName: 'Cannon' };
    let position = {jobTitle: 'Software Engineer'};
    let person = {...name, ...position};
    ```
* **In the video, what is the first step that the developer does to pass functions between components?** He creates a function in the parent element that controls the state.

* **In your own words, what does the increment function do?** It maps over his array of people objects in the state and increments the count on the the person object with the name that was passed into function.

* **How can you pass a method from a parent component into a child component?** You can pass it to the child element as a prop.

* **How does the child component invoke a method that was passed to it from a parent component?** by calling the method that was passed to it as a prop