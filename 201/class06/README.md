# Problem Domain, Objects, and the DOM

## Reading Q&A

* **How would you describe an object to a non-technical friend you grew up with?** An object in programming like a model for an object in real life. It groups to together properties and functions of a certain idea. For example a bird object might have properties like feathers, a beak, a name, and number of legs. It will also have functions like fly, eat, and speak.
* **What are some advantages to creating object literals?** object literals are convenient and reuseable. You can create a kind a name space and pass it around inside of functions
* **How do objects differ from arrays?** Objects are unordered and they're elements are referenced by their name instead of their index. 
* **Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.** IF you wanted to evaluate a variable to access a certain property you would need to put it in brackets. The dot operator only accepts the name of the name value pair and doesn't evaluate the name after the dot before accessing
* **Evaluate the code below. What does the term this refer to and what is the advantage to using this**? this allows you to refer to the current object that you are inside. It makes code reusable as you don't have the specify the exact name of the object inside of itself. This refers to the current object
    ```
    const dog = {
        name: 'Spot',
        age: 2,
        color: 'white with black spots',
        humanAge: function (){
            console.log(`${this.name} is ${this.age*7} in human years`);
        }
    }
    ```
* **What is the DOM?** The dom is a model of am html document that is stored in memory and accessible to javascript to be manipulated in real time.
* **Briefly describe the relationship between the DOM and JavaScript.** The dom can used by javascript to access, change, and manipulate the current elements and properties of an html document

## Things I want to know more about