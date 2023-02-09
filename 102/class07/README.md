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

## Things I want to know more about 
* Expressions and operations
* For and While loops