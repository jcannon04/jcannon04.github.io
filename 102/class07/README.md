# Programming with Javascript

## JavaScript Functions

In JavaScript, a function is a piece of reusable code that can be executed when it is called. Functions are defined using the "function" keyword, followed by the name of the function, a list of parameters in parentheses, and a block of code in curly braces. When the function is called, the values passed as arguments to the function are stored in the parameters, and the code within the function is executed.

Functions can also return a value using the "return" keyword, which ends the execution of the function and passes the specified value back to the code that called the function.

Here's an example of a simple function in JavaScript:

```javascript
function addNumbers(a, b) {
  return a + b;
}
```
In this example, the function "addNumbers" takes two parameters, "a" and "b", and returns the sum of those two values. The function can be called by passing in two arguments, like this:

```javascript
let result = addNumbers(2, 3);
console.log(result); // outputs 5
```

Functions are an important building block in JavaScript and are used to break down larger problems into smaller, more manageable parts. They can be used to encapsulate logic, making it easier to write and maintain complex applications.

## If..else.. statements

The if...else statement in JavaScript is used to make decisions in your code. It allows you to specify a block of code to be executed only if a certain condition is true. If the condition is false, an alternate block of code can be executed using the else clause.

Here's an example of how the if...else statement works in JavaScript:

```javascript
let num = 5;

if (num > 10) {
  console.log("The number is greater than 10");
} else {
  console.log("The number is not greater than 10");
}
```

In this example, the condition num > 10 is evaluated. If it is true, the code within the first set of curly braces ({}) is executed and the message "The number is greater than 10" is logged to the console. If the condition is false, the code within the second set of curly braces is executed, and the message "The number is not greater than 10" is logged to the console.

The if...else statement can also be nested, allowing for multiple levels of decision making in your code. Additionally, you can use multiple else if clauses to test for multiple conditions and choose which block of code to execute based on the first true condition.

Here's an example that demonstrates the use of else if:

```javascript
let num = 15;

if (num < 10) {
  console.log("The number is less than 10");
} else if (num < 20) {
  console.log("The number is between 10 and 20");
} else {
  console.log("The number is greater than or equal to 20");
}
```

In this example, the condition num < 10 is tested first. If it is true, the message "The number is less than 10" is logged to the console. If it is false, the next condition num < 20 is tested. If this condition is true, the message "The number is between 10 and 20" is logged to the console. If both of these conditions are false, the code within the else clause is executed, and the message "The number is greater than or equal to 20" is logged to the console.

## Operators

An operator is a special symbol that performs a specific operation on one or more operands (values or variables) and produces a result. There are various types of operators in JavaScript, including:

Arithmetic operators (e.g. +, -, *, /, %)
Assignment operators (e.g. =, +=, -=, *=, /=, %=)
Comparison operators (e.g. ==, ===, !=, !==, >, <, >=, <=)
Logical operators (e.g. &&, ||, !)
String operators (e.g. +)
Conditional (ternary) operator (e.g. ? :)
Unary operators (e.g. typeof, +, -)
The web page provides detailed information and examples for each type of operator in JavaScript.

## Events

Events are actions or occurrences that happen in the system you are programming in. The system fires a signal and provides a mechanism by which an action can be taken automatically. Events happen in the browser and are associated with a specific item or group of items. These items could include a single elements, a group of elements, an html document, or the browser window. Example include:

* The user selects, clicks, or hovers the cursor over a certain element.
* The user chooses a key on the keyboard.
* The user resizes or closes the browser window.
* A web page finishes loading.
* A form is submitted.
* A video is played, paused, or ends.
* An error occurs.

In order to react to an event a programming must create an **event handler** and register it to respond to the event.

### adding event listeners
Some different events that be used with 'EventTarget.addEventListener()` include: 

* click
* mouseover
* mouseout
* focus
* blur
* dblclick
* play (for video elements)

### removing event listeners

To remove an event listener use **EventTarget.removeEventListener()** and pass in the type of event and the callback being removed.

You can also use an AbortSignal to remove events

```javascript
const controller = new AbortController();

btn.addEventListener('click', () => {
  const rndCol = `rgb(${random(255)}, ${random(255)}, ${random(255)})`;
  document.body.style.backgroundColor = rndCol;
}, { signal: controller.signal });
```

To remove the event created in this manner use 

`controller.abort();`

By adding more than one event listener for the same event both handlers will run when the event is fired

## Event Bubbling

If you have the same type of event handlers (like 'click') on a parent and a child element. When clicking the child the event will bubble up through the parents and fire a click event on all it's ancestors as well.

you can use **Event.stopPropagation** to disable the event bubbling behavior

Event capturing is the opposite of event bubbling. The event is fired on the outer most element and goes inward toward the most nested element

Event capturing is disable by default but can be enabled by passing the capture option to addEventListener

**Event Propagation** allows us to create an event listener on a parent that will run when that event happens on any of its children

```javascript
function random(number) {
  return Math.floor(Math.random()*number);
}

function bgChange() {
  const rndCol = `rgb(${random(255)}, ${random(255)}, ${random(255)})`;
  return rndCol;
}

const container = document.querySelector('#container');

container.addEventListener('click', (event) => event.target.style.backgroundColor = bgChange());

```
`elem.addEventListener(e, callback, {capture: true})`

## Promises 

A promise represents an eventual completion or failure of an asynchronous operation. A promise is a returned object in which you attach callbacks instead of passing callbacks into a function.

`createAudioFileAsync()` is a function that creates an audio file give a config record, and two callbacks. One that is called incase of a successful creation and one that is called incase of a failure.

```javascript
function successCallback(result) {
  console.log(`Audio file ready at URL: ${result}`);
}

function failureCallback(error) {
  console.error(`Error generating audio file: ${error}`);
}

createAudioFileAsync(audioSettings, successCallback, failureCallback);

```

if `createAudioFileAsync` was rewritten to use promises it would look like

```javascript
createAudioFileAsync(audioSettings).then(successCallback, failureCallback);
```

## Chaining 

It's a common situation to have multiple asynchronous operations back to back, where each operation starts once the last operation succeeds. Before promises this would result in a callback pyramid of doom. With promises this problem is solved by because promises return a promise object and we can chain promises together with .then() method instead of passing a callback into a function.

```javascript
const promise = doSomething();
const promise2 = promise.then(successCallback, failureCallback);
```
Always return results from a promise. If you do not return the resulting promise there is no way to track the progress and this results in a floating promise

it is possible to chain after a failure. This can be useful to perform more actions even after one action in the chain has failed

## Nesting 

Nesting is a control structure to limit the scope of catch statements. Specifically, a nested catch only catches failures in its scope and below, not errors higher up in the chain outside the nested scope. When used correctly, this gives greater precision in error recovery:

## Error Handling

There are two types of rejected promises that occur when they are not handled `unhandledrejection` and `rejectionhandled`. In the web browser they bubble up to the global scope. An unhandled rejection is sent when a promise is rejected but there is no handler available. A rejection handled is attached to a rejected promise that has already caused an unhandled rejection event.

Both types of events have a promise property and a reason property. The promise property indicates the promise that was rejected and the reason property tells us the reason.

## Composition 

There are four composition tools for running asynchronous operations concurrently

* `Promise.all()`
* `Promise.allSettled()`
* `Promise.any()`
* `Promise.race()`

`promise.all()` immediately rejects the returned promise when it fails and aborts the other operations

`promise.allSettled` ensures that all operations are complete before resolving

You can also compose promises sequentially meaning that each operation will wait on the last before executing here are a few examples: 

```javascript
const applyAsync = (acc, val) => acc.then(val);
const composeAsync =
  (...funcs) =>
  (x) =>
    funcs.reduce(applyAsync, Promise.resolve(x));
```
The composeAsync() function accepts any number of functions as arguments and returns a new function that accepts an initial value to be passed through the composition pipeline:

## Wrap an old style callback function with a promise

you can wrap a a callback function from an old api like so 

```javascript
const wait = (ms) => new Promise((resolve) => setTimeout(resolve, ms));

wait(10 * 1000)
  .then(() => saySomething("10 seconds"))
  .catch(failureCallback);

```

## Things I want to know more about 
* Expressions and operations
* For and While loops