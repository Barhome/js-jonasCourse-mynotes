......................................................................................................

Section no.10 Address: A Closer Look At Functions

...............

## Lecture no.128 Address: Default Parameters

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.129 Address: How Passing Arguments Works: Value vs Reference

### Type: Code

- check the code examples in final folder, notes on code
- This part requires your complete understanding to primitive types and object or reference types video as it is related to the current video as it is a review to the previous but applied to functions. it is important to understand how primitives and objects work in the context of functions.

## Lecture no.130 Address: First-Class and Higher-Order Functions

### Type: Theory

- Theory pdf pages 124-126
- First Class function is a fundemental feature or property of JS language which enables us to write higher order functions.
- JS treats functions as first-class citizens which means that functions are simply values. Why does js work this way? becuse functions are really just another type of objects in JavaScript. Since objects are values so functions are values too. since functions are values there are punch of things we can do with them, like storing them in variables like function experssions or in object properties like an object method. We can also pass functions as arguments to other functions like adding event listeners or event handlers to dom object that will make the function as a listner waiting for an event to happen to that dom object then the event handler or function will be called. we clearly pass the function as a value in the addEventListner function. We can also return a function from another function.
- Remember that functions are objects and objects have methods so functions has methods that we can call on functions like the bind method which is an example of that. We will learn about these methods in this section.
- Higher order functions recieves a function as an argument , returns a new function or both and as we mentioned is because of the first class functions feature or property in JS
- Example of higher order function is the addEventListener as it receive another function as an input and we say that the function that is passed in is a callback function that is because the callback function will be called later by the higher order function which means that the addEventListner will call the callback function later as soon as the event happens. Another example of higher order function is the one that returns another new function.
- first class functions and higher order functions are not the same first class functions is a feature or concept whether a language have it or not they don't exist in practice, and higher order functions exist in practice so what allows having higher order functions in practice is the feature of first class functions in the JS language.

## Lecture no.131 Address: Functions Accepting Callback Functions

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.132 Address: Functions Returning Functions

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.133 Address: The call and apply Methods

### Type: Code

- check the code examples in final folder, notes on code
- in this lecture we go back to this keyword, we will learn about how to set it manually and why we would want to do that.

## Lecture no.134 Address: The bind Method

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.136 Address: Immediately Invoked Function Expressions(IIFE)

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.137 Address: Closures

### Type: Code

- Theory pdf pages 127-132
- check the code examples in final folder, notes on code

## Lecture no.138 Address: More Closures Examples

### Type: Code

- check the code examples in final folder, and watch the video again.
- we don't have to return a function from another function to create closure
