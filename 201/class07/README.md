# Object-Oriented Programming, HTML Tables

## Reading Q&A

* **Explain why we need domain modeling.** Domain modeling helps us to really understand a problem before you start just coding away. It help you map real world ideas into programming objects. With domain modeling we describe various entities, and their properties and behaviors. So, that we can create objects that are a model or our problem.

* **Why should tables not be used for page layouts?** HTML tables are not made to be responsive and mobile friendly by default. They make the output for screen reader more complex and make your site less accessible for blind or visually impaired users

* **List and describe 3 different semantic HTML elements used in an HTML table** `<th>`, `<tr>`, `<td>` are three semantic elements that you can use in HTML `<table>` element. Th stands for table header, tr stands for table row and td stands for table data.

* **What is a constructor and what are some advantages to using it?** A constructor is a function that create objects, binds the this keyword to the new object so you can use it in the constructor, runs the code in the constructor, and returns a new object. It is useful when you need to create a large (or even a small) number of similar objects. The constructor function helps us define the shape of an object and create many objects with that same shape and then change them as needed.

* **How does the term this differ when used in an object literal versus when used in a constructor?** Inside of an object literal the this keyword refers to the object it is inside. Inside of a constructor function it refers to the object that you are creating with the new keyword.

* **Explain prototypes and inheritance via an analogy from your previous work experience** The prototype chain in javascript is like the chain of command at my current job. There are functions of my job that I may not know how to perform. In that case I ask my boss. If my boss doesn't know how to handle the situation and I ask his boss, and so on until I find the person who knows how to perform the action.

## Things I want to know more about