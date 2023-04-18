# State and Props

* **Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?** render. The render method happens second in the mounting stage, and componentdidmount is second to last 

* **What is the very first thing to happen in the lifecycle of React?** The mounting is they first cycle and it begins with the constructor of the component

* **Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates** constructor, render, componentDidMount componentWillmount, React Updates

* **What does componentDidMount do?** componentDidMount is called right after the component gets mounted. It is a good place to make network/api calls or initialize the DOM.

* **What types of things can you pass in the props?** Any javascript value, arrays, object, string etc.

* **What is the big difference between props and state?** State is handled inside of a component and can be changed inside of the component. Props is handled outside of the component and must be changed outside the component.

* **When do we re-render our application?** Whenever the state of a component changes.

* **What are some examples of things that we could store in state?** Something that needs to be changed and re-rendered through the life of a component. A counter or a score is a good example.

## Things I would like to learn more about