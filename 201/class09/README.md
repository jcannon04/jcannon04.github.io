# Forms and JS Events

## Reading Q&A 

* **Why are forms so important in web development?**
Forms are the main way users send data to websites. They are used to send data to servers for validation and storage. They also be used to input data client side and change settings directly on the front end.

* **When designing a form, what are some key things to keep in mind when it comes to user experience?** Accessability is important, you want to make sure that the form interacts correctly with screen readers and that the form makes sense visually for sighted users as well. You also want to make sure that forms are not too long or complicated. This can lead to users giving up on filling them out. You should only ask the user for information that you absolutely need.

* **List 5 form elements and explain their importance.**
`<input>` the default type is text but can also be used to add more interactivity by accepting passwords and emails.
`<textarea>` used for long lines of texts like messages and notes.
`<fieldset>` encapsulates related inputs in your form and gives them a label with `<legend>`
`<lable>` labels your input with text and also groups together with your inputs when read with a screen reader.
`<select>` creates a drops with different `<option>`s allows users to select one option from many choices.

* **How would you describe events to a non-technical friend?** Events are like wedding invitations. Whenever someone is getting married they send you an invitation to know that the wedding is taking place, what time its taking place and where it is happening. The webpage does the same thing whenever you click or button or hover over an item. The site gets the invitation and decides whether or not to take action and what action to take.

* **When using the addEventListener() method, what 2 arguments will you need to provide?** You need to provide the type of event you are listener for as a string. And a function to execute when the event occurs. This callback function takes the event object as a parameter and can be used within the callback

* **Describe the event object. Why is the target within the event object useful?** The event object contains methods and properties of the event that has occurred. Including methods that can be useful for changing default ways that the event is handled by the browser. It also contains the target which is the element of the page where the event originated. It must be a descendent of the element that the event listener for that event was attached to.

* **What is the difference between event bubbling and event capturing** Event bubbling is the idea that events that happen on a child element are sent up the dom hierarchy to all of the ancestors of the original target. Event capturing is the idea that since event bubbling occurs you can put a listener on a single ancestor of multiple descendants instead of having to put an event handler on each descendant element

## Things I want to learn more about