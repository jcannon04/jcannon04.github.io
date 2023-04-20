# React and Forms

* **What is a ‘Controlled Component’?** A controlled component in react is a form element that receives its value from it's parent and uses a callback function to update the parents state whenever the value of the controlled component changes.

* **Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.** Generally you want to update the state as soon as they enter their feedback. React is built to make this simple and it allows you to give user realtime feedback

* **How do we target what the user is entering if we have an event handler on an input field?** the event object that is passed to an event listener behind the scenes has access to the element that the event occurred on and the value stored in it e.target.value

* **Why would we use a ternary operator?** When you want to store value of the expression in a variable or you just want to make your code more concise

* **Rewrite the following statement using a ternary statement:**
    ```javascript
    if(x===y){
    console.log(true);
    } else {
    console.log(false);
    }
    ```
    '''javascript
    console.log( x===y ? true : false )
    '''
## Things I want to know more about