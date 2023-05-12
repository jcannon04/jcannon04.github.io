# Functional Programming 

* **What is functional programming?** Function programming is a paradigm or method of programming where computations are treated as evaluations of mathematical functions and changes or modifications of state are avoided.
* **What is a pure function and how do we know if something is a pure function?** A pure function is a function that always return the same results given the same input and does not cause any observable side effects.
* **What are the benefits of a pure function?** A pure function is consistent and encapsulated so it doesn't effect data in other parts of the program. This makes our code more modular and easier to test.
* **What is immutability?** If something is immutable is unchanging or unable to change over time
* **What is Referential transparency?** Referential transparency is the combination of pure functions and immutable data. That means a function called with the same parameters will always return the same result.
* **What is a module?** A javascript file that you can export data from and use it in other javascript files.
* **What does the word ‘require’ do?** It is used to import modules into a file to use the data in the required file.
* **How do we bring another module into the file the we are working in?** We call the require function with the path of the module as a string for the parameter, and save the returned value into a variable to reference in our code.
* **What do we have to do to make a module available?** Export the data we want to require in another file.