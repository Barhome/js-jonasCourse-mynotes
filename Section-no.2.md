.....................................................................................................

# Section no.2 JavaScript Fundamental - Part 1

...............

## Lecture no.7 Address: Hello World!

### Type: Code

- writing your first program , we write it in the console. You can make math operation in the console

## Lecture no.8 Address: A Brief Intro to JavaScript

### Type: Theory

- Theory pdf pages 18-23
- JavaScript Definition
- Role of JavaScript
- JavaScript uses
- JavaScript versions modern java script vs Es5

## Lecture no.9 Address: Linking a JavaScript File

### Type: Code

- How to write code in JavaScript File and how to run it in the browser.
- Writing code in a script tag or linking JS file in a script tag inside the index.html file.

## Lecture no.10 Address: Values and Variables

### Type: Code

- what is value and what is varible?
- value is the smallest unit of information that we have in JS. we can store values into variables. this way we can use them over and over again.
- rules and conventions for naming variable in JS is camel case ex: firstName doesn't start with a numbers but it can containts numbers letters underscores and dollar sign.
- keywords are not allowed to be used as variable names.
- as a conventions do not put the first letter in uppercase as it used to name objects not variables.
- don't use name as a variable name as it is a keyword and it is legal to use it as a varible name but we don't recommed it.
- real life constants like `let PI = 3.1415` is written in uppercase letters convention
- make your varible names descriptive

## Lecture no.12 Address: Data Types

### Type: Theory

- Theory pdf pages 26-28
- in JS every value ie either an object or primitive value. So, a value is only a primitive when it's not an object.
- We will focous on primitive data types and talk about objects later.
- use `typeof` operator to know the data type of a value in a varible
- declare a variable and assign it to a value and reassign it to change its value
- declaring a varible without a value will give it undefined value and type.
- null type is object that is an error in JS it is supposed to return null type as it returns undefined type for undefined value.

## Lecture no.13 Address: let, const, var

### Type: Code

- use let to declare mutable variables, variable that we need to reassign
- use const to declare unmutable variables and you have to assign it at the same time you declare it.
- always use const and use let when you are sure that you need to change the value later in the code.
- var is avoided it's legacy now, for mutable variable , we will talk about it later when we talk about block and function scope as we will know why we should avoid it.
- assigning a varible without let or const or var will create a property to global object not a varible in the current scope. you will understand this later. the point is never declare a varible without the keywords let, const or even var.

## Lecture no.14 Address: Basic Operators

### Type: Code

- operators allow you to transform values or combine values. they do all kind of work or operations with values.
- operators catagories are many like mathematical operators , comparison operators, logical operators , assignment operators and many more.

## Lecture no.15 Address: Operator Precedence

### Type: Code

- Check MDN web site to get a table to show you operator precedence

## Lecture no.17 Address: Strings and Template Literals

### Type: Code

- building strings by concatinating them using template literals use backticts ``like this`string and variable inside ${variable or any expression}` more about expressions later in the future lectures.
- backticts let you write multiple lines easily just by hitting Enter key.

## Lecture no.18 Address: Taking Decisions: if / else statements

### Type: Code

- called controll structure
- check the code in the final folder in this section 1
- I installed emoji extension. Ctrl+Shift+p to get command palette and get your emoji.

## Lecture no.20 Address: Type Conversion and Coercion

### Type: Code

- Type conversion when we manually or explicitly convert types and Type coercion when JavaScript automatically or implicitly convert types for us behind the scenes.
- use Number function to convert a "string-like-a-number" into a number this will change the value not the varible that contains the string .
- it will give us NaN which mean invalid number still a nubmer but is invalid if the conversion of a string that is not a "string-like-a-number" to number.
- we normally get NaN when we have a numerical operation that doesn't return a number.
- use String function to convert a number to a string
- white values in console means it is a string value.
- JS only converts to strings and numbers and booleans when it comes to primitive values.
- only plus + operator makes type coersion from number to a string not the opposite and concatinates them
- - and astricks`*` and / operators make type coersion from "string-like-a-number" to number and substract the numbers or multiply or divide.

## Lecture no.21 Address: Truthy and Falsy Values

### Type: Code

- Falsy values are values that becomes false when we convert them into boolean the opposite definition is for Truthy values too.
- Falsy values are 5 values 0, '' empty string, undefined, null , NaN
- Truthy values are any value except the mentioned Falsy values, empty objects are truthy values.
- use Boolean function to convert.
- values are always converted into booleans implicitly 'type coersion' when using if conditions and logical operators.

## Lecture no. 22 Address: Equality Operators == and ===

### Type: Code

- === strict equality operators doesn't do type coersion,checks type and value
- == loose equality operator does type coersion , checks value only, always avoid it.
- learn about adding else if block
- !== strict different operator
- != loose different operator

## Lecture no.23 Address: Boolean Logic

### Type: Theory

- Theory pdf pages 29-32
- and &&, or || and not !
- and, or operators combine multiple boolean values , not works on one boolean value
- not is ! it inverts the logical value it has bigger precedence then and , or operators

## Lecture no. 24 Address: Logical operators

### Type: Code

- check the code in the final folder
- and is &&
- or is ||
- not is !

## Lecture no.26 The switch Statement

### Type: Code

- check the code in the final folder
- it does strict equality comparison and once it gets a true it applys all the code even the code in the other case statements after the case statement that satisfies the true so we need break keyword to avoid that.
- you can use multiple case values statement to the same code block as in the example in the final folder.
- check the if statement example it explain the logic in switch example above.

## Lecture no.27 Statements and Expressions

### Type: Code

- Expression is a piece of code that produces a value ex: 3+4 even 1991 is a value as it produces a value
- Statement is like a bigger piece of code that is executed which does not produce a value on itself. it performs a set of actions but it doesn't produce a value. think of it like a full sentence that translate our actions. The actions that we want our program to perform. it ends with a semi colon.
- Javascript expects expressions in some places like inside of a literal template.

## Lecture no.28 The Conditional (Ternary)

### Type: Code

- The conditional or ternary operator `condition? expressitionIfTrue:expressionIfFalse;`
- operator is an expression so it produce a value so we can use this to baiscally conditionally declare variables.
- can be used in a template literal

## Lecture no.30 JavaScript Releases: ES5, ES6+ and ESNext

### Type: Theory

- Theory pdf pages 33-38
- a look at the history of javascript
- listen again to the video if you are interested
