# HTML Lists, Control Flow with JS, and the CSS Box Model

## Things I want to learn more about

## Reading Q&A

### When should you use an unordered list in your HTML document?

When you want to display a list of items that have no particular order that they need to follow

### How do you change the bullet style of unordered list items?

change the values of the list-style property on a selected `<ul>` element

### When should you use an ordered list vs an unordered list in your HTML document?

Ordered lists are used when you want your list items to be in numerical, alphabetical, or some other type of order. Unordered list are used to list general items that belong to the same category but order doesn't necessarily matter

### Describe two ways you can change the numbers on list items provided by an ordered list?

You can change which number to start ordering your list items with the `start` attribute on an `<ol>` tag. You can also order your list items with letters or roman numerals by changing the `type` attribute.

### Describe the CSS properties of margin and padding as characters in a story. What is their role in a story titled: “The Box Model”?

Padding is like a comfy and soft teddy bear surrounds the delicate content. Margin is like a security guard that makes sure all the other dangerous boxes keep there distance.
### List and describe the four parts of an HTML elements box as referred to by the box model

* content - the part of a box where actual content is displayed
* padding - this is the space around the content of a block.
* border - wraps around the padding style it with the border properties
* margin -  the space between a box and the boxes that surround it.

### What data types can you store inside of an Array?

You can store all data types that are part of javascript including objects and even other arrays

### Is the people array a valid JavaScript array? If so, how can I access the values stored? If not, why?
```
 const people = [['pete', 32, 'librarian', null], ['Smith', 40, 'accountant', 'fishing:hiking:rock_climbing'], ['bill', null, 'artist', null]];
```

This is a valid javascript array it is a multi dimensional array and you would need to access the members like `people[1][3]` this would get the 4th item of the second array inside the outer most array.

### List five shorthand operators for assignment in javascript and describe what they do.

* += adds the value on the right to the value stored in the variable on the left and assigns the new   value to the variable
* -= subtracts the value on the right from the value stored in the variable on the left and assigns the new value to the variable
* /= divides the value in the variable on the left by the value on the right and stores the new value in the variable 
* \*= multiplies the value in the variable on the left by the value on the right and stores the new value in the variable 
* %= stores the remainder from dividing the value stored in the variable on the left by the value on the right into the variable

### Read the code below and evaluate the last expression and explain what the result would be and why.

```
 let a = 10;
 let b = 'dog';
 let c = false;

 // evaluate this
 (a + c) + b;
```
This would evaluate to the string '10dog'. The `a + c` would be evaluated first because it is in the parentheses. Javascript would change false to 0 and add  it to 10. then it would turn 10 to a string and concatenate it with 'dog' the value stored in b.

### Describe a real world example of when a conditional statement should be used in a JavaScript program.

You want to check to make sure some user input a value string. You would run a different functions depending on if what they typed was valid

### Give an example of when a Loop is useful in JavaScript.

You want to continue prompting the user for a valid input if they type something invalid.

