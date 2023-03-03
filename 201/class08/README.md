# CSS Layout

## Reading Q&A

* **Flexbox is designed for one-dimensional content. Explain what this means.** Flexbox can only align items in one dimension. If your content wraps to another line flex box creates a different flex row for each line. So, in this case you would not be able to line up item on line 2 with another item on line 1.

* **Explain the difference between the main axis and cross axis.** The main axis represents the axis that is in the same direction as the flex direction of the flex container. So if you your flex direction is the default row then the main axis would be horizontal. The cross axis represents the axis perpendicular to the the main axis.

* **How can using certain properties of flexbox negatively impact accessibility?** Any property that would change the ordering of your items will affects accessibility. If you change the ordering through css then the logical order of your items might not be the same as the ordering that shows up on the screen. A screen reader will use the logical order in your html to read the order of the items but if you tab through items with your keyboard you will follow the visual order.

* **What are some advantages of using flexbox over float?** Flexbox is more powerful and offers a lot more flexibility that using floats. It it easier and more manageable to work with. For example with flex box you make all the children of a parent container take up the same space regardless of their content. This can be very difficult with using just float and other layout techniques.

* **How does this topic connect with your long term goals?** I have a better understand of layouts in web applications. It will allow me to more easily build layouts for prototypes and quickly get projects up and running. If I want to build a prototype or wireframe to a potential client knowledge and understanding of flexbox will help me be efficient in building it.

## Things I want to know more about