.........................................................................................................

# Section no.3 JavaScript Fundamental - Part 2

..............

## Lecture no.32 Activating Strict Mode

### Type: Code

- Strict mode is a special mode that we can activate in JavaScript which make it easier for us to write secure JavaScript code.
- To activate just write `'use strict'` at the begining of the JS script in the JS file.
- we can activate the strict code for a specific function or block, no point the lecturer says.
- by secure we mean that strict mode make it easier to us developer avoid accidental errors as it helps us introduce the bugs into our code. That's for two reasons first, forbids us to do certain things second, it create visible errors for us in certain situation in which without strict mode Javascript will fail silently without letting us know that we did a mistake.
- check examples in video note in the udemy website 3:00. it shows strict mode and its list of reserved keywords for future features and it raises an error and assigning a variable without declaration error that won't show up if the strict mode deactivated.

## Lecture no.33 Address: Functions

### Type: Code

- Functions are the fundemental building block in Javascript. It's sort of a variable that holds lines of code to allow us to reuse it in different places in our program. helping us to write more maintainable code.
- how to define a function.
- how to call invoke or run a function.
- how a function recieve (parameters as local varibles inside the function and actual values called arguments) a data and how it returns it (return a statement or keyword).
- store return value of the function in a varible.
- functions that has no explicit return value returns implicitly undefined value.
- console.log is a built-in function

## Lecture no.34 Address: Function Declarations vs Expressions.

### Type: Code

- Function declaration is the one that starts with function keyword. we can call it before we declare it because of hoisting
- Function expression is the one that is stored in a varible used when we want to treat a function as a value stored in a varible.

## Lecture no. 35 Address: Arrow Functions

### Type: Code

- Arrow function is third type of funtion added to Javascript in ES6. It is simply a special form of function expression that is shorter and faster to write. usually used when we have one line code as no return keyword is necessary
- doesn't get this keyword, which is something we will learn about later.
- check code in Section 3

## Lecture no.36 Address: Functions Calling Other Functions

### Type: Theory

- Theory pdf pages 40-42

## Lecture no.37 Address: Reviewing Functions

### Type: Theory

- Theory pdf pages 43-46
- using the same parameters' names in different functions is acceptable because of the local scope of the functions. you can even have a varible outside the function with the same name of the function's parameter.
- return keyword terminates the function execution or immetiately return the function and we say the function returns.
- the rest of the lecture same as what was explained earlier. note that we call the function with parenthesis without parenthesis the function is just a value.

## Lecture no.39 Address: Introduction to Arrays

### Type:Code

- check code in final folder of section 3
- you can mutate arrays elements not whole array when they declared with const because of the way Java scripts stores things in memory and they are not primitive data type as only primitive data types are immutable
- it can hold different data types and you can put an array inside of an array.

## Lecture no.40 Address: Basic Arrays Operations(Methods)

### Type: code

- array is a data structure to store a multiple related values in the same variable
- array.push(value) at the end of the array and returns the new length
- unshift add at the begining returns the new length
- pop remove last element and returns that element
- shift remove first element and returns that element
- indexOf returens the index of the passed value
- include returns boolean value if element exit or not and checks with strict equality no type coersion

## Lecture no. 42 Address: Introduction to Objects

### Type: Code

- objects is another data sturcture to store multiple related values where each value has a name
- objects is like a list of key value pairs sparated by a comma
  instead of square brackets we use curly brackets.
- use arrays for ordered data to access them by their indices and objects for unstructure data as the order doesn't really matter.

## Lecture no.43 Address: Dot vs Bracket Notation

### Type: Code

- Learn how to retrieve and change data from objects using the dot and bracket notation.
- object.propertyname to retrieve data or object['key'] the main use of bracket notation is that you can extract the key out of an expression so inside the brackets we can put any expression to produce the desired name of the key. ex: objectname[keyExpression] doesn't work with dot notation.

## Lecture no.44 Address: Object Methods

### Type: Code

- define a function expression as a property of the object.
- calling the function from an object can be done with dot and bracket notation
- JavaScript gives us access to the special variable called this that allows us to read other properties directly from the object itself to be used inside the method.
- this keyword will be assigned to or refer to the object(referencing the object itself) that is calling the method you can check it with `console.log(this)`
- creating a new property using this inside a method requires to call the method at least once in your code

## Lecture no.46 Address: Iteration: The for loop

### Type: Code

- loop is a control structure that allows us to automate repetitive tasks.
- for( variablIinitialValueForTheCounter; logicalConditionRepeatsThecodeAsLongAsItIsTRUE; counterIncrement){lines of code}
- after each iteration of the loop (in which code runs) counter in Incremented at the end of the iteration

## Lecture no.47 Address: Looping Arrays, Breaking and Continuing

### Type: Code

- start initial value with 0 as arrays are 0 based.
- create a new array from exiting array
- continue keyword escape the current iteration to the next iteration when the if condition is true
- break keyword terminate the whole loop when the if condition is true

## Lecture no.48 Address: Looping Backwards and Loops in Loops

### Type: Code

- loopin starting from the last index
- loops in loops, check the code in final folder

## Lecture no.49 Address: The While Loop

### Type: Code

- define the repeatition variable while(condition){line of codes; incrementThe repeatition variable;}
- use cases is when the condition is the only requirement without a counter of repeatition variable as it loops as long as the condition is true and stops when condition is false.
- you can also use it to specifiy when a loop is about to finish as the conditon is checked after the iteration code run see example in lecture final folder.
