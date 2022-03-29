# Notes Style

- Below is my notes style

# Section no.

## lecture no. and address

### Type: Code or concepts

- note points

....................................................................................................

# Section no.1

..............

## lecture all

### Type: Theory and Course instructions

- Theory Pdf pages 1-15
- Check "notes-about-the-course" file.

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
- you can mutate arrays elements not whole array when they declared with const because of the way Java scripts stores thing is memory and they are not primitive data type as only primitive data types are immutable
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

......................................................................................................

# Section no.4 How to Navigate This Course

..............

## Lecture no.51 Address: Pathways and Section Roadmaps

### Type: Code

- check the video in the website

......................................................................................................

# Section no.5 Address: Developer Skills & Editor Setup

..............

## Lecture no.55 Address: Setting up Prettier and VS Code

### Type: Code

- check notes about the course and the video in the website

## Lecture no.56 Address: Installing Node.js and Setting up a Dev Environment

### Type: Code

- check notes about the course and the video in the website

## Lecture no.57 Address: Learning How to Code

### Type: Theory

- Theory pdf pages 48-54 whenever you feel frustrated see this lecture.
- set a specific , measureable, realistic and time-based goal and write it down
- develop a plan on how to get your goal
- search the technologies you want to learn them one by one step by step.
- understand code and type it in your editor
- reinfore what was learned by using it immediately
- take notes
- challenge your self by small code exercise Codewars
- come up with projects and try to work on them to grow and over come obstacles
- leave tutorial hell and learn on your own
- don't get stuck with clean code , always refactor it, efficient code comes later after practice
- accept the fact that you will never know everything. like the legendary Kyle Simpson
- learn with other people , explain new concepts to other people, share goals to make yourself accountable and share learning progress with the web dev community #100DaysOfCode #CodeNewbie, #webdev etc.
- keep on working on projects
- last slide is important.

## Lecture no.58 Address: How to Think like a Developer Become a Problem Solver!

### Type: Theory

- Theory pdf pages 54-61
- make a plan and follow a logical approach.
- steps to follow:
  1. make sure you understand the problem by asking the right questions to get a clear picture of the problem
  2. divide and conquer by breaking a proble into smaller sub problems
  3. try your coding skills if fail search for a solution on google
  4. write a pseudo code before writing the actual code it is the code that is easily understood by human to help you write the actual code. It looks like a real code as we use similar structure of a programming language
- develop a genuine curiosity and passion for understanding how things actually work, not only in programming but really in the whole world around you.

## Lecture no.59 Address: Using Google, StackOverFlow and MDN

### Type: Code

- watch the video if you need a refresher

## Lecture no.60 Address: Debugging(Fixing Errors)

### Type: Theory

- Theory pdf pages 62-65
- what is a software bug? a defact or a problem in a computer program that causes unintended or unexpected behaviour in our program.
- debugging is about identifying, finding , fixing and preventing bugs
- debugging process first try to identify during development by running automated tests or the worst kind of bugs is identified through user reports during production also identify the context where the bug is happening whether in a specific browser or with specific users..etc
- go to code and find the bug in the code using developer console or debugger software
- fix
- prevent by searching same bug in similar code also writing tests using test softwares

## Lecture no.61 Address: Debugging with the Console and Breakpoints

### Type: Code

- watch video in case of refresher and check code in final folder
  -console.log,console.warn,console.error are the same function of printing the input on the console only with different formatting. console.table(objectName) shows the object in a nicely formatted tabel.
- At 7:20 we will learn how to use a debugger in google chrome.
- set breakpoints in sources tab in beside the console tab in developer tool in chrome by clicking the left bar on a specific line of code that will give us red point. When we reload and play button is hit execution stops at this break point.
- you can continue execution by hitting stop button here.
- clear the red point to prevent stopping the code at this breakpoint.

......................................................................................................

Section no.7 Address: JavaScript in the browser: DOM and Events Fundamentals

.............

## Lecture no.70 Address: Guess My Number

### Type: Code

- watch the video to know the project
- how to select an element from html to JS file: using document object and its methods to select an element ex: `document.querySelector('pass a selector as a string')` this is called dom manipulation use console.log(document.querySelector('selector')) to print the element in the console for check up

## Lectuure no.71 Address: What's the DOM and DOM Manipulation

### Type: Theory

- Theory pdf pages 67 to 71
- What is the dom?
- dom is created by the browser as soon as html page loads store in a tree structure in this tree each html elements is one object.
- dom tree is corresponding to an html document, dom tree is structured html element in a tree we use child element parent and sibiling element when talking about the dom and dom manipulation.
- for each element there is an element node in the dom tree.
- We can access and interact with each node using JS
- DOM Always starts with the document object, document is a special object that we have access to in JavaScript. This object serves as the entry point into the Dom. as in this ex: `document.querySelector('pass a selector as a string') we say document is the entry point object to select other children and grand children in the dom tree.
- The first child element is the html element, the root element in all html documents. it has two child elements head and body you will also find them in the dom tree. They are adjacent elements, and so they are siblings in the dom as well. as keep going in the nested html structure we keep adding children to the dom tree.
- Dom tree has more than just element nodes , they have nodes for the text and comments and other stuff, as the rule is whatever is in html document also has to be in the dom. so dom is a complete representation of the html document. so that we can manipulate it in complex ways.
- DOM Methods and properties for Dom manipulations is not part of JS. JS is a dialect of EchmaScript specification, and all this Dom stuff is not in there. we use JS in the browser not running code in console but manipulate webpages by using JS that are actually displayed and rendered in the browser, by using the web apis that Dom is part of it as web apis are like libraries that browsers implement and we can access them from our JS code. These are libraries that is written also in JS and we use them automatically they work behind the scenes with out the need to import them or do anything. There is a Dom specifications that browsers implement which is the reason why Dom manipulation works the same in all browsers. There are many other web apis such as Timers , the fetch Api , and many more.

## Lecture no.72 Address: Selecting and Manipulating Elements

### Type: Code

- document.querySelector('.classNameWithDot').textContent to get or set text from element for input element use .value

## Lecture no.73 Address: Handling Click Events

### Type: Code

- We can make our code react to something that happens(event)to an element in the Dom for that we use an Event Listenr, an event is something that happens on the page like mouse click , key press or mouse moving and many other events then with an event listener we wait for this event to happen and react once it happens
- first select the element that we wait for an event to happen to it.
- second call the addEventLisener method and pass the type of the event and pass the function value as an argument that represent the action taken when the event happens. This fuction called event handler
- JS engine will call this function when the event happens. Notice we pass the function name only with no parantheses or we define the function that's a proof of the JS engine is the one who calls the function when the event happens.
- whatever comes from an input is usually a string. If you need to compare it to a number you have to convert it to a number.

- if code works when the value of the condition is true.

## Lecture no.74 Address: Implementing the Game Logic

### Type: Code

- basic logic of the app
- we use Math.random() to generate random number
- we select each element that is affected and work on the logic.

- application states are set of variables that hold the application states where a state is a value that represents something in the application. The dom usually starts with inital values for the states and it good practice to save them in a variable in the application code this variable is called application state variable.

## Lecture no.75 Address: Manipulating CSS Styles

### Type: Code

- We need to access the style property of the element we want to change its style ex: document.querySelector('elementNameWithNoDot').style.propertyNameOfTheStyleWithCamelNameNotationNotWithHyphensAsInCSS
- We can set the style property with only a string
- these style values we change is set as inline style that is directly applied to the html style attribute of the element.

## Lecture no.77 Address: Implementing Highscores

### Type: Code

- just logic

## Lecture no.78 Address: Refactoring Our Code: The DRY Principle

### Type: Code

- get rid of duplicate code as when we change some functionality we will have to change it in multiple places which might lead to making mistakes and creating software bugs.
- we use refactoring is a technnique in which we restructure the code with out changing how it works. Basicly we do refactoring to improve the code and to eliminate duplicate code.
- how we do that by first identifying the duplicate code
- second rewrite the code without duplication
- another technique is to write a function to git rid of the duplication code.

## Lecture no. 79 Address: POJECT #2: Modal Window

### Type: Code

- explaining the project. it concentrates on selecting elements as nodelist using querySelectorAll as querySelector will select only the first element in nodelist and also concentrates on manipulating classes
- you can loop over the nodelist they work as an array

## Lecture no.80 Address: Working with Classes

### Type: Code

- we add, remove or even check if a class applied to an element using classList property and the add or remove method on that property with by passing class name only we pu Ex: selectElementVariableName.classList.remove('classNameWithOutDot') or .add('hidden')
- adding classes helps us aggregate many style properies in one class. so when we want to manipulate style of an element aggregate all style properities in classes and add and remove these classes as needed.
- instead of writing anonymous function in the addEventListner. We shoud store the function in a varible and pass the variable to addEventListner as function is a value so we are passing a value as an argument.

## Lecture no.81 Address: Handling an "Esc" Keypress Event

### Type: Code

- keyboard events are global event as they do not happen on one specific element. for global events like keyboard events we usually listen on the whole document. ex: document.addEventListner('keyBoardEventName',anonymousOrFunctionValue)
- 3 types of keyboard events keydown , keypress or keyup
- keyup happens when we lift our finger off the key board
- keypress is fired contiuously as we keep our finger on a certain key.
- keydown is fired as soon as we just press down any key. mostly used.
- to get the key code or key name: as an event happen JS generates an object and stores all the information about the event in that Object and we can access all the information in the event handler function and to access this event give this function a parameter named any name you like usually e or event again as the event happens JS call the handler with the event object as an argument. console.log(e) will show up all the info about the event from where key code or key name show up.
- use elementSelectedVariable.classList.contains('classNameWithoutDot') to see if the selectedElement has the class or not

## Lecture no.82 Address: PROJECT #3: Pig Game

### Type: Code

- Project logic in a flow chart representation. We start by the possible actions a user can take and then from there we see what happens in the application. use diagrams.net to drew flow charts.
- select elementId in querySelector('#elementIdNameWith#') in getElementById('elementIdNameWithOut#')
- setting textContent will save number as strings in the Dom

## Lecture no.83 Address: Rolling The Dice

### Type: Code

- Drewing flow charts is like dividing the problem into smaller problem, divide and conquer.
- write comments of what you are going to do is also problem solving technique
- we can change the attribute src of an image by selectingTheImage.src=`imagename.png`

## Lecture no.84 Switching The Active Player

### Type: Code

- game logic implemented check code in final folder
- use .toggle() method to toggle a class toggle means if you have it, it will be removed if you don't have it, it will be added.

## Lecture no.85 Holding Current Score

### Type: Code

- game logic implemented check code in final folder

## Lecture no.86 Resetting The Game

### Type: Code

- game logic implemented

......................................................................................................

Section no.8 Address: How JavaScript Works Behind The Scenes

.............

## Lecture no.89 Address: A High Level Overview of JavaScript

### Type: Theory

- Theory pdf pages 72-85
- 9 points to define JS Language by which we get the big picture before diving deep (this is a technique in learning):
  1. **High-level**: As you know every program that runs on your PC needs some hardware resouces like cpu and memory So, in languages like JS and Python programmers dosen't need to work on managing hardware resources because of all the abstactions that take all of that work away from us. on the other side other low level languages like C. that makes the language easy to use and learn but the downside, Programs won't be as fast or optimized as programs written in low level languages.
  2. **Garbage Collected**: one of the powerful tools that takes memory management away from developers. It is actually an algorithm inside JS engine that automatically cleans and removes old ,unused objects from the computer memory.
  3. **Interpreted or just-in-time compiled language**: computer processors just understand 0 and 1 and ultimately every single program needs to be written in 0s and 1s which also called machine code. since that we can't write machine code as human we write human readable code and which is abstraction over machine code, this code needs to be translated to machine code and that step can be either compiling or interpreting, in case of JS this happens inside the JS engine.
  4. **Multi-paradigm**: This is what makes it popular as paradigm is the approach and an overall mindset of structuring our code, which wil direct the coding style and technique in a project that uses a certain paradigm. There are 3 popular paradigms are (Procedural, Object-Oriented and Functional) JS does all that and that's make it flexible and versatile we can choose whatever we want. Also we can classify paradigms as Imperative and Declarative more on that later.
  5. **Prototype-based object-oriented**: this point explains the object oriented nature of JS. Everything in Js is an object except primitive values. because of prototypal inheritance we create an array from array blueprint called prototype which contains all array methods and the array we create,inherits the methods form the prototype.
  6. **First-class functions**: functions are treated as regular variables so, we can pass functions into other functions and we can even return function from functions. This is very powerful as it allows us use many powerful techniques and allows for functional-programming, which is a paradigm we mentioned before. we used it in addEventListnersas we pass function to a function.
  7. **Dynamic**: as we don't assign data types to variables. They only became known when JS engine excutes our code. Also, the type of variables can be changed when we reassign variables. that makes it loosly-typed language. use TypeScript as it is strongly-typed language.
  8. **Single-threaded**: very complex topics and we will talk about it in details later on. What is concurrency model? it means how JS engine handles multiple tasks happening in the same time. Why we need it? because JS itself run in one single-thread, which means it can only do one thing at a time. That's why we need a way to handle multiple tasks happening at the same time. By the way a Thread in computing is like a set of instructions that is executed in the computer's CPU. So basically, The thread is where our code is actually executed in a machine's processor. So, what if there is a long running task like fetching data from a remote server? well that would block the single thread where the code is running and we don't want that what we want is non-blocking behavior. How we achieve that by using The event loop as it takes long running tasks execute them in the background and then puts them in the main thread once they are finished. This is in a nutshell JS's non-blocking event loop concurrency model with a single thread. This is a huge over simplification that we will come back to.
  9. **Non-blocking event loop concurrency model** explained in the above point.

## Lecture no.90 Address: The JavaScript Engine and Runtime

### Type: Theory

- Theory pdf pages 86-92

- What is the JS engine and what is the Js Runtime? How JS code translated to a machine code?

- **JS Engine** is a computer program that execute JavaScript code. Every browser has an engine but the most known engine is google's V-Eight.The V-eight engine powers google chrome and also **Node.js** which is the JS runtime that we use to build server side applications with JS so outside of any browser. Other browser has their own JS Engines. You need to know JS engine components and how it works. Any JS Engine has a call stack and a heap. **The call stack** is where our code is actually executed using something called execution contexts. **The heap** is an unstructured memory pool which stores all the objects that our app needs.

- How the code is compiled to machine code so that it actually can be executed afterwards.

- first, what is the difference between **compilation and interpretation**. Computers only understand 0s and 1s therefore every single computer program ultimately needs to be converted into this machine code and this can happen using interpretation or compilation.

- **In compilation**, the entire source code is converted into machine code at once and then written to a binary portable file that can be executed on any computer. so we have two steps, first machine code is built then executed in the cpu so in the processor. execution happen way after the compilation which mean any app you are using on your computer has been compiled before and now you are executing it way after its compilation.

- **In interpretation**, there is an interpreter which runs through the source code and executes line by line. here we don't have two steps as in compilation. Instead the code is read and executed all at the same time. of course code is translated just right before execution not ahead of time. Js used to be purely interpreted language but the problem with the interpreted languages is that they are so much slower than compiled languages.

- with modren JS and fully fledged web apps that we built low performance is no longer acceptable. now JS uses a mix between compilation and interpretation which is called **just-in-time compilation**. This approach basically compiles the entire code into machine code at once and then executes it right a way which means still we have the two steps of regular ahead of time compilation but there is no portable file to execute and execution happens immediately after a compilation.

- example of how it works: As a piece of code enters the engine the first step is to **parse** the code which means to read the code. during **the parsing process** the code is parsed into a data structured called **the abstract syntax** tree or AST. this work by first splitting up each line of code into pieces that are meaningful to the language like const or function keywords, and then saving all these pieces into the tree in a structured way. This step also checks if there are any syntax errors. The resulting tree will later be used to generate the machine code. example of AST for one line of code declaring a const is in the pdf pages. AST has nothing to do with the dom, it is just a representation of the entire code inside the engine. The next step is compilation which takes the generated AST and compiles it into machine code then this machine code gets executed right away because remember modern JS engine use Just-in-time compilation. and remember execution happens in the JS engine's Call Stack this will be explained in next lecture.

- Modern JS engines have some pretty clever **optimization strategies**. What they do is to create a very unoptimized version of machine code in the beginning just so that it can start executing as fast as possible. Then in the background this code is being optimized and recompiled during the already running program execution and this can be done multiple time after each optimization after each optimization the unoptimized code is simply swept for the new more optimized code without ever stopping execution of course. this process makes modern engines so fast. all this parsing, compilation and optimization happens in some special threads inside the engine that we cannot access from our code. So completely separate from the main thread that is basically running into call stack executing our own code.

- Now different engines implements in slightly different ways, but in nutshell this is what modern just-in-time compilation looks like for JavaScript.

- **JavaScript runtime** and the most common one which is **the browser**. Runtime is like a container includes all the things we need to use JS in this case in the browser. The heart of any JS runtime is always a JS engine. The engine is not enough we need web apis which are all the things related to the dom, fetch Api and timers even the console.log and other apis that we use all the time. Essentially web apis are functionality provided to the engine but which are actually not part of th JS language itself. JS simply gets access to these apis through **the global window object**. but it still makes sense that the web apis are part of the JS runtime because a runtime is just like a box that contains all the JS related stuff that we need.

- the runtime also includes **callback queue**. this is a data structure that contains all **the callback functions** that are ready to be executed. for example we attach a handler function to a dom elements like a button to react to a certain events, and these events handler functions are also called callback functions as the event happens the callback functin will be called and here is how it actually work behind the scenes. so the first thing that actually happens after the event is that the callback function is put in the callback queue then when the call Stack is empty the callback function is passed to the call stack so that it can be executed and this happens by something called **the event loop** that takes callback functions from callback queue and puts them in the call stack so that they can be executed. And remember that event loop is how JS's nonblocking concurrency model is implemented and here how it works as mentioned above. We will go about how this makes JS nonblocking in a special lecture about the event loop later as it is very important to understand this deeply as a developer.

- We analyized JS runtime in the browser as this course deal with that only however JS can exit outside the browsers, for example in Node.js it is pretty the same without web apis as the browser who provides these instead we have multiple C++ bindings and a so called thread pool. these details don't matters as its beyond the scope of this course, just rememeber different JS runtimes do exist.
- in the next we will learn how js is executed in the call stack.

## Lecture no.91 Address: Execution Context and The Call Stack

### Type: Theory

- Theory pdf pages 93-97
- How the JavaScript code is executed? We know it is happening in the call Stack but we will dig deeper to know more.

- Supposing that the code was just finished compiling so the code is ready to be executed. A global execution context is created for the top level code which is basically code that is not inside any function which means only the code that is outside of functions will be executed. Functins should only be executed when they are called.

- What is the execution context? **Execution Context** is an abstract concept but we can define it basically as an environment in which a piece of JS is executed. It is like a box that stores all the necessary information for some code to be executed such as local variables or arguments passed into a function. So JS code always runs inside an execution context. There is only one global execution context it is always there as the default context, and it is where top level code will execute. Now, we have environment for top level code to be executed, it is executed and there is not a lot to say about the execution itself except it is a computer cpu processing the machine code that it received. once the top code level is finished executing function finally start to execute as well. it works for each and every function call a new execution context will be created containing all the information that is necessary to run exactly that function and the same goes tor methods as they simply functions attached to objects. All these execution contexts together makes the **call stack**. when all functions are done executing, the engine will basically keep waiting for callback functions to arrive so that it can execute these for example a callback function associated with a click event. And remember that it's the event loop who provides these new callback functions as we learned in the last lecture.

- What is the exection context made of? first thing inside any execution context is **variable environment** in this all our variables and function declarations are stored, and there is also a special argument object that contains all the arguments that were passed into the function that the current execution context belongs to because each funtion gets its own execution context as soon as the function is called. So basically all the variables that are somehow declared inside a function, will end up in its variable environment. However a function can access variables outside of the function. and this work because of something called **the scope chain**. We will talk about this later in details but what you need to know for now is that the scope chain basically consists of references to variables that are located outside of the current function. And to keep track of the scope chain, it is stored in each execution context. Finally each context also gets a special variable **The this keyword** we will talk about this later in details. The content of the execution context, variable environment, scope chain and the this keyword is generated in a so-called creation phase which happens right before execution. as small note Arrow functions don't get this keyword or arguments object instead they get them from their closest regular function parent. This is a very important detail about the Arrow function we will know why in the future. so these are the things that are necessary to run each function and the top level code. Now behind the scenes there is even more complex stuff but it is okey to know these points only for now.

- Example of creation phase for a piece of code in the video 8:10.
- how the engine keeps track of the order in which functions were called? and how will it know where it currently is in the execution? that's where **the call stack** comes in.
- What is the call stack? is a place where execution context get stacked on top of each other, in order to keep track of where we are in the programs exection so the execution context that is on top of the stack is the one that is currently running and when it's finished running it will be removed from the stack, and execution will go back to the previous execution context. code example int the video at 11:25 to show what happens inside the call stack after compiling the code.

## Lecture no.92 Address: Scope and The Scope Chain

### Type: Theory

- Theory pdf pages 98-104
- what is scope and scope chain?
- Scoping controls how our program's variable are organized and accessed by th JS engine. basically scoping asks the question, where do variables live? where can we access certain variable and where not?
- In JS we have lexical scoping which means that the way variables are organized and accessed is entirely controlled by the placement of functions and of blocks in the programs code. for ex: function written inside another funtion has access to the variables in the parent function. So Variable scoping is influnced by where exactly we write our functions and code blocks.
- Scope is the space or environment in which a certain variable is declared, simple as that. in case of a function that's essentially the variable environment which is stored in the function execution context. so the difference between scope and variable environment for the case of functions, they are the same.
- in JS we have global scope, function scope and block scope
- scope of a variable is basically the entire region of our code where a certain variable can be accessed.
- people use the word scope for all of the above concepts but it is good to know the small differences.
- three types of scope in Js:

  1. Global scope: for top level code all variables outside function or block.they are accessable everywhere.
  2. Function Scope: each function creates a scope and the variables declared inside that function scope are only accessable inside that function. This is also called local scope. this applys for all functions types.
  3. block scope: starting from ES6 blocks creates their own scope by blocks we mean everything between a curly braces such as the block of if statement or for loop. just like function scope , variable declared inside the block is only accessaible inside that block and not outside of it. this applys only for varibles declared with let and const so we say let and const are block scoped. variable declared with var inside a block is still accessible outside of the block and would be scoped to the current function and the global scope so we say var is function scoped.
  4. note: finally, also starting in ES6, all functions are now also block scoped, at least in strict mode which means functions declared inside of a block are only accessible inside that block.

- scope has access to variables and function arguments from all outer parent scopes. this is how scope chain works. in other words if one scope needs to access a certain variable but can't find it in the curent scope, it will look up in the scope chain and see if it can find a variable in one of the parent scopes. if it can, it will then use that varible and if it can't there will be an error. this process called variable lookup in scope chain. it is important to note that these variables are not copied from one scope to another instead scopes simply look up in the scope chain until they find the varibale they need and they use it. it is also impotant to note this doesn't work the other way around. A certain scope will never have access to the variable of an inner scope. again on scope can only look up in a scope chain, but it cannot look down basically. So only parent scope can be used, but no child scope.
- lexical scoping is the way we can access variables depends on where the scope is placed or where it is written in the code when none of the scopes is written inside of one another then they have sibling relationship not parent-child relationship and they can't access each other's variables. We can say scope chain works upwards not sideways.
- the difference between the scope chain and the call stack, we need to know how call stack , execution context , variable environment and scope are all related to one another. see example in the video 17:00.
- we can say that scope chain is equal to adding together all the variable environments of all the parent scopes.
- MY understanding of scope and scope chain(you might want to refine this understanding by rewatching and revising the last slide as it is very useful) if you want to define the scope and the scope chain and you need to know how it works, you need to understand the structure of your code inside the JS file. We can imagine that an empty JS file is the grand parent inside that grand parent empty file we declare variables,functions and we write blocks of code. We can imagine that these functions and the written blocks of code are children to the grand parent and they are themselves are parents to other functions and other blocks of code written inside of them. now, we want to access variables written inside of these many functions and blocks. it is simple children can access their parents and grand parents variables. but siblings can't access eachother's variables. functions, let and const variable defined in a function are block scoped which mean that their parent scope can't access them only children functions and blocks can access them, var variables are function scoped which means they end up in the closest function scope. variables declared inside the global or the grand parent scope before it was the empty js file is called global variables they are accessed everywhere.

## Lecture no.93 Address: Scoping in Practice

### Type: code

- watch the video to see live examples.

## Lecture no.94 Address: Variable Environment: Hoisting and The TDZ

### Type: Theory

- Theory pdf pages 105-108
- How variables are actually created in JS? Hoisting is mechanism that makes variables accessible before they are actually declared in the code. Wrong definition when they say that variables are lifted or moved to the top of their scope for example: in a function that's actually what looks like on the surface but behind the scenes that's in fact not what happens. instead behind the scenes, the code is scanned for variable declarations before it is executed during the creation phase of the execution context and for each variable a new property is created in the variable environment object and that's how hoisting really works.
- hoisting doesn't work the same for all variable types: function declarations, var variables, let and const variables, function expressions and arrows, Check how it works in the pdf slides.
- let and const variables are technically yes they are hoisted but in practice no they aren't they are placed in temporal dead zone TDZ which means we can't access the variable between the beginning of the scope and the place where variables are declared. so we get and error if we attempt to use them before their declaration in the code, and their initial value is uninitialized.
- function expresstions and arrows depends on creating them using var, let, or const so they behave as variables depending on that in regard of hoisting.
- why Tdz is introduced in ES6 because of it is behavior that makes it easy to avoid and catch error. because using a variable that is set to undefined before it is actually declared can cause serious bugs which might be hard to find. Accessing variable before declaration is simply bad practice and should be avoided so they make it show up errors thanks to TDZ so we can act and correct it. Another reason is about const variable as we can't reassign variable so it is impossible to set them to undefined first and then assign their real value later. const should never reassigned and they are only assigned when execution reaches the declaration and that make it impossible to use the variable before declaration if so it will be undefined as it is a const variable which is not the case.
- Why hoisting? in some program techniques it is essential to use functions before their actual declaration such as mutual recursion. some thinks it makes code more readable. Now, the fact it also works for var declarations that because that was the only way hoisting could be implemented at the time. so hoisting of var variable is basically just a byproduct of hoisting functions and it probably seemed like a good idea to simply set variables to undefined which is insight is not really a good idea. It wasn't planned that JS would be hugely programming language that it is today. also we can't remove the feature from the language _for backword compitability reasons_ (I guess) so we use let an const to work around it.

## Lecture no.95 Address: Hoisting and TDZ in Practice

### Type: code

- watch the video to see code examples.
- variables declared with var keyword added as a property to the global window object and that will have some implications in some cases and variables with let and consts are not added as properties to the window object.
- Write window in the console to explore it.

## Lecture no.96 Address: The this Keyword

### Type: Theory

- Theory pdf pages 109-110
- What is this keyword? is a special variable created for every execution context(every function), takes the value(points to ) the owner of the function in which the this keyword is used. It is one of 3 component of execution context.
- this values is not static. the owner is defined by how the function is actually called and its values is assigned when the function is actually called.
- we will analyze four different ways in which a function can be called.

  1. method --> this= object that is calling the method or it points to the object calling the method.
     it solve the issues in method borrowing which is when an object borrow other objects' methods
  2. simple function call --> this = undefined in strict mode and points to the global object if not in strict mode the global object in case of the browser is window object and that is very problematic which why we should use the strict mode.
  3. Arrow functions while arrow function is not a way of calling functions, It's important kind of function we need to consider, arrow function don't get their own this keyword but if used inside an arrow function --> this = will be the this keyword of the surrounding parent function or scope we call it technically the lexical this keyword because it gets picked up from the outer lexical scope of the arrow function.
  4. event listener --> this = points to the dom element that the handler is attached to.

  note: this will never point to the function we are using this keyword inside of it and will never point to the variable environment of the function.

  there are other ways to call a function using new , call, apply and bind methods we will talk about how this keyword work with them in later videos.

## Lecture no.97 Address: The this Keyword in Practice

### Type: Code

- watch the video for code examples.
- method borrowing to a regular function will give us error because of this keyword now is undefined.
- we will take examples for this keyword with event listener in the advanced dom section.
- this is defined by the owner of the function who is calling the function.

## Lecture no.98 Address: Regular Functions vs Arrow Functions

### Type: Theory

- No Theory pdf pages, just watch the video and read the notes for refreshment.
- we will show up some pitfalls related to this keyword with regular functions and arrow functions so we can learn when to use and avoid each of them.
  -using arrow function in object declaration will make this keyword value inncorrect or not logical as it doesn't refer to the object it was used inside and as this keyword inside arrow function takes the value of its outer parent scope. it gave us undefined in the example as the outer scope was the global scope and this value will be the window object that doesn't have the same property defined in the object containing the arrow function.
- object literal doesn't get block scope it is just the way we define an object looks like block scope but it is not.
- don't use var to declare variables as it creates a property in the global object.
- bottom line never use arrow function as a method inside an object.
- if we have a function defined inside a method inside an object this will be undefined as the rule of a simple function call applys here. we have a work around by creating a variable called self or that an assign this to it. or we can apply another solution instead of using simple function inside of a method inside of an object use arrow function inside of a method inside of an object as arrow funcion.

- Let's bring the topic of arguments keyword in a previous lecture about execution context, and the call stack, we learned that functions also get access to arguments keyword.Now just like the this keyword , the arguments keyword is only available in regular functions(function expressions and function declarations not in arrow functions) which means we can send more arguments than the ones defined in the regular function as arguments keyword is an array that we can loop over and do the math. This is not allowed for arrow functions. this is not important in modern js as we have better ways to deal with multiple arguments but it is good to know about it.

-

## Lecture no.99 Address: Primitives vs Objects(Primitives vs reference Types)

### Type: Theory

- Theory pdf pages 113-117
- We will learn the difference between the way primitive types and object are stored in the memory. This is a practical topic you need to check the code in this video as well.
- When talking about types primitive is called primitive types and object is called reference types this is based on the different way they are stored in the memory.
- primitive types stored in the call stack by that we mean they are stored in the execution context where they are declared but for simplicity we say they are stored in call stack where the execution contexts run and reference types stored in the heap. how all that work how they are stored?

- let's look at the primitive values example in the slide: when we declare a variable like age = 30 what actually happens inside the js engine and the computer's memory. First js will create a unique identifier with the variable name then a piece of memory will be allocated with a certain address so 0001 in this example and finally the value would be stored in memory at the specified address. this all happens in the call stack where primitive values are stored. It is extremely important to understand that the identifier actually points to the address not to the value itself. but in fact age is equal to the memory address 0001,which holds the value of 30. then we declare a oldAge variable to be equal to age variable knowing that the variable actually hold the memory address what should oldAge look like? it will simply point to the same memory address as the age variable and also it will look like oldAge, is simply 30 as well. now, we set age to 31 so what will happen then? the value at address 0001 will not be 31 that would change oldAge as well since they both point to the same address, Also the value at a certain memory address is immutable meaning it can't be changed. what happens here is that a new piece of memory is allocated or created and the age identifier now simply points to the new address, which is holding the new value of 31, so when we log both age and oldAge we get what was expected.

- Now, with reference values things work a bit differently, When a new object is created such as me object, it is stored in the heap such as before there is a memory address and value itself. in case of reference values like me object the me identifier does not point directly to the newly created memory address in the heap. so in this example D30F instead it will point to a new piece of memory address 0003 created in the call stack and this new piece of memory address 0003 in the stack will then point to the object in the heap by using the memory address D30F as its value stored in the stack. in other words the piece of memory in the call stack has a reference to the piece of memory in the heap which holds or me object, that's the reason why we call objects reference type. again when we declare a variable as an object, an identifier is created which points to a piece of mememory in the stack which in turn points to a piece of memory in the heap and that is where the object is actually stored. And it works this way because objects might be to large to be stored in the stack instead they are stored in the heap which is like an almost unlimited memory pool. and the stack just keeps a reference to where the object is actually stored in the heap so it can find it whenevr necessary. moving on the code we create a new variable called friend that we set equal to me object so what will happen here? just like with primitive values, the friend identifier will point to the exact same memory address as me identifier. And again that address contains the reference, which then points to the object itself and like this the friend is now essentially the exact same as the me object. So here comes the interesting part because now we are actually gonna change a property in the friend object by setting friend.age=27. so what happens then is that the object is found in the heap and the 30 is changed to 27. and by the way even though we defined the friend variable as constant , we actually still manipulate the object with out problems and when we think about that , it makes sense because we are actually not changing the value in memory for the friend identifier , it is still D30F so the reference to the object.All we did was to change the value in the heap, and that's not a problem so it is misconception that all variables declared with const are immutable. in fact that is only true for primitive values, but not for reference values. now we understand the wiered behavior in the code example. as me an friend point to the exactly same object in the heap. as they are only two differenct identifiers pointing to the same exact value and that value is the memory address D30F which points to the reference in the memory heap. And one important implication of this whenever you think you are copying an object, you are really just creating a new variable that points to the exact same object. this is how reference values work in JS and to make copys of the object we will learn about this later.

## Lecture no.100 Address: Primitives vs objects in Practice

### Type: Code

- watch the video or review the code to learn how to make a shallow copy of an object not a deep clone.
- shallow copy makes a new copy with the first level of data other deep levels will be the same for the original object and the copy so if we change the deep levels it will affect both objects .
- deep clone makes a new copy with all deep levels so if we change the new copy the original won't change. We use library like lo dash to do the deep cloning thing as it has tons of helpful tools and one of them is deep cloning.
- in the example family property has the value of memory reference that points to the same array object in the memory heap that's why when we change someting in the object by family memory reference it will be changed for old object jessica2 and jessicaCopy.

......................................................................................................

Section no.9 Address: Data Structures, Modern Operators and Strings

...............

- split the script.js as code starts from the bottom of the scripts and it depends on an object at the top of the script

..............

## Lecture no.103 Address: Destructuring Arrays

### Type: Code

- Check the code examples from the bottom up , notes on code
- Destructuring is an ES6 feature. a way to break complex data structure into smaller data structure.

## Lecture no.104 Address: Destructuring objects

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.105 Address: The spread Operator(...)

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.106 Address: Rest Pattern and Parameters

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.107 Address: Short Circuiting (&& and ||)

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.108 Address: The Nullish Coalescing Operator(??)

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.109 Address: Logical assignement Operators

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.111 Address: Looping Arrays: The for-of Loop

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.112 Address: Enhanced Object Literals

### Type: Code

- Check the object code in the top of the file to see all these things
- an object is called object literal when we basically write it literally in our code using the curly braces syntax.
- Es 6 introduced 3 ways to easily write an object literal like restaurant object in our code:
  1. no need to assign an object inside the object litteral if the property name is same as the object name like openingHours property
  2. when it comes to declaring a method inside of the object you can remove the semi colon : and function keyword.
  3. we can compute the property names if we want instead of writing them manually with the use of square brackets we can write inside of it any expression to compute the property name ex: [exp to compute the propertynam]: property value,

## Lecture no.113 Address: Optional Chaining (?.)

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.114 Address: Looping Objects: Object Keys, Values, and Entries

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.116 Address: Sets

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.117 Address: Maps: Fundamentals

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.118 Address: Maps: Iteration

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.119 Address: Summary: Which Data Structure to Use?

### Type: Theory

- Theory pdf pages 118-120
- we have 4 built in data structures in JS we will talk about the pros and cons of each data structure to help you when to choose one of them
- getting data from a web apis comes as a json which is just text or long string but we can easily converted into a javaScript object because the original text uses the same js objects formatting as js objects and arrays

## Lecture no.121 Address: Working With Strings - Part 1

### Type: Code

- Why strings have methods as they are primitive data types not object data types? The answer is whenever we call a method on a string JS will automatically behind the scenes will convert that string primitive to a string object with the same content and then on that object the method will be called.
- This process is called boxing because it takes the string and puts it in a box which is the object.
- check the code examples in final folder, notes on code

## Lecture no.122 Address: Working with Strings - Part 2

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.123 Address: Working With Strings - Part 3

### Type: Code

- check the code examples in final folder, notes on code
- to see the rest of string methods google mdn string methods

## Lecture no.125 Address: Destructuring Arrays

### Type: Code

- review the video if you want more working with the strings exercises

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

......................................................................................................

Section no.11 Address: Working With Arrays

...............

## Lecture no.142 Address: Simple array method

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.143 Address: The new at Method

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.144 Address: Looping Arrays: forEach

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.145 Address: forEach With Maps and Sets

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.146 Address: PROJECT: "Bankist" App

### Type: Code

- Check the video as it talks about the project and flow chart in final folder
- later we will learn about how to create a flow chart

## Lecture no.147 Address: Creating DOM Elements

### Type: Code

- We will use some of DOM Manipulation techniques and learn about new ones.
- check the video to learn more
- used innerHTML='' to reset the html movement container and used insertAdjacentHTML to add elements with data from the account1 object in the html movement container.

## Lecture no.149 Address: Data Transformations: map,filter , reduce

### Type: Theory

- Theory pdf pages 134-136
- map, filter, reduce is like forEach method in concept
- map does an operation to all elements and returns a new array with the new results.
- filter it requires a test condition and it returns a new array with the elements passed this condition
- reduce boils down all array elements down to one single value, you need to specify the operation and accumulator variable for example addition to add all elements to the accumulator. and it returns the final accumulated value.

## Lecture no.150 Address: The map Method

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.151 Address: Computing Usernames

### Type: Code

- check the video to see the code examples on map and forEach methods

## Lecture no.152 Address: The filter Method

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.153 Address: The reduce Method

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.155 Address: The Magic of Chaining Methods

### Type: Code

- check the video and the code examples in final folder, notes on code
- Never over use chaining as chaining many methods can cause performance issues if we have huge arrays
- it is bad practice to chain method that mutate the original array like splice method or reverse method

## Lecture no.157 Address: The find Method

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.158 Address: Implementing login

### Type: Code

- check the video to see project logic where previous skills is implemented
- as clicking a form button reloads the page we need to prevent that by passing event object to the callback function in the addEventListent and add event.preventDefault() to prevent form from resubmitting
- hitting enter keyboard inside an input in a form triggers the click event.

## Lecture no.159 Address: Implementing Transfers

### Type: Code

- check the video to see project logic where previous skills is implemented

## Lecture no.160 Address: The findIndex Method

### Type: Code

- check the video and the note about findIndex in final folder, notes in code

## Lecture no.161 Address: some and every method

### Type: Code

- check the code examples in final folder, notes in code

## Lecture no.162 Address: flat and flatMap

### Type: Code

- check the code examples in final folder, notes in code

## Lecture no.163 Address: Sorting Arrays

### Type: Code

- check the code examples in final folder, notes in code
- revise the video to get more understanding

## Lecture no.164 Address: More Ways of Creating and Filling Arrays

### Type: Code

- check the code examples in final folder, notes in code

## Lecture no.165 Address: Summary: Which Array Method to Use?

### Type: Theory

- Theory pdf pages 137-139

## Lecture no.166 Address: Array Methods Practice

### Type: Code

- you didn't finish that , practice what you learned

..........................................................................................................

Section no.12 Address: Numbers, Dates, Intl and Timers

.............

## Lecture no.170 Address: Converting and Checking Numbers

### Type: Code

- check the code examples in final folder, notes in code

..........................................................................................................

Section no.13 Address: Advanced DOM and Events

.............

## Lecture no.184 Address: PROJECT: "Bankist" Website

### Type: Code

- check the video to see the project explaination

## Lecture no.185 Address: How the DOM Really Works

### Type: Theory

- Theory pdf pages 141 - 144
- What is the DOM? interface between JS code and the browser or more specifically HTML documents that are rendered in and by the browser. we use it to write code in js to interacting with the browser or without using DOM. We will learn to work with webpages and therefore with tha DOM and we learn so much about the DOM and how to create amazin dynamic effects.
- what we can do with DOM? we can create, modify, and delete elements, set style and classes and attributes and listen and respond to events. This works as a Dom tree is generated from any html document.
- A DOM tress is a tree like structure made out of nodes. See a representation in the pdf file. We can interact with this tree as we already did a couple of times in this course.

- How this interaction actually works? Dom is a very complex API which remember stands for application programming interface which is the interface we use to programmatically interact with the Dom. In practice that means DOM contains a ton of methods and properties that we use to interact with the DOM Tree such as querySelector addEventlistner or createElement methods or also innerHTML , textContent or children properties.

- In DOM, There are differenct types of nodes for example some nodes are HTML elements but other are just text, you need to know about types of DOM objects as Dom methods and properties are organized into these differenct types of objects.

- How the DOM API is organized behind the scenes? every single node of the DOM tree is of the type, node. And such as or just like everything else in JS, each node is represented in JS by an object. This object gets access to special node methods and properties, such as textContent, childNodes, parentNodes clondeNode and many others. We already know there are differenct types of nodes. So, how should these be represented? Well, this node type has a couple of child types so to say. And these are the element type, the text type, comment type and also the document type. So, whenever there is text inside any element, we already know that it gets its own node. And that node will be of the type, text. And the same actually happens for HTML comments and that's because the rule is that everything that's in the HTML has to go into the DOM as well. Now for the element itself there is the element type of node. And this type of nodes gives each HTMl access to a ton of useful properties such as innerHTML classLis, children or parentElement. There are also many useful method like append , remove , insertAdjacentHTML, querySelector, closest and that's just to name a few(check slide). So again, each, element will be represented internally as an object. Now just to make this complete, the element type has internally an HTML element, child type. And that element type itself has exactly one child type for each HTML element that exists in HTML. So we have special type for buttons , special type for images, for links and so on and so forth. And that's important because each of these HTML elements can have differenct unique properties. For example an image has a source attribute in HTML which no other element has. Or the anchor element for links has the Href attribute which also no other element has. and so the DOM needs a way of storing these differenet attributes and therefore different types of HTML elements were created in the DOM API. And just to make sure that we're all oist a DOM API is broken up into these different types of nodes. I also want you to understand that each of these types of nodes has access of different porperties and methods and some of them even inherit more properties and methods from their ancestors in this organization.
- So, we didn't talk about the documents node type. So document, which we use all the time in DOM manipulation is in fact just another type of node so it contains important methods, such as querySelector, createElement getElementById and note how querySelector is available on both document and element types so, keep this in mind because it will be important later on.
- There is one final missing piece here because the DOM API actually needs away of allowing all the nodes types to listen to events. And remember we usually listen for events by calling the addEventListner method on an element or the document. So, why this actually work well it is because there is a special node type called EventTarget which is a parent of both the node type and also the window node type and so with this, thanks to inheritance, we can call addEventListner on every single type of node in the DOM API because all elements as well as document and window, and even text and comment will inherit this method and therefore we will be able to use addEventListner on all of them just as if it was their own method.
- To be clear we never manually create eventTarget object. This is just an abstract type that we do not use in practice. this all happens behind the scenes to make all the functionality work as we expect it to work.
- so, in a nutshell this is how the DOM API is strctured behind the scenes. There are still some simplifications here but this all that really matters. Check the diagram of how the DOM API is organized as it help you structure all this information in your mind. if want to get deeper check MDN Documentation but again all that you need to know is here in this lecture.
- Now, let's check the other practical parts in this section to see all these concepts in action.

## Lecture no.186 Address: Selecting, Creating and Deleting Elements

### Type: Code

- check the code examples in final folder,notes on code.

## Lecture no.187 Address: Styles, Attributes and Classes

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.188 Address: Implementing Smooth Scrolling

### Type: Code

- check the code examples in final folder,notes on code
- review the video if you want to learn about manual calculations to scroll to a specific position

## Lecture no.189 Address: Types of Events and Event Handlers

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.190 Address: Event Propagation: Bubbling and Capturing

### Type: Theory

- Theory pdf file pages 145-147
- JS events have a very important property. They have capturing phase and bubbling phase.
- example demonestrated on an html document along with a dom tree, but only for the anchor element in red, check the pdf file, we will explain what happens when someone clicks on that link.
- when a click happens on the link , the dom generates a click event right away however this event is not generated at the target element (the element where the event happened the anchor or link element) instead the event is actually generated at the root of the document so at the very top of the dom tree.
- From there, the so called capturing phase happens, where the event then travel all the way down from the document root to the target element and as the event travels down the tree, it will pass through every single parent element of the target element. As soon as it reaches the target, the target phase begins, where events can be handled right at the target and as we already know, we do that with event listners so event listners wait till a certain event to happen on a certain element, and as soon as the event occurs, it runs the attached callback functions. in this example it simple create this alert window and this happens in the target phase.
- now, after reaching the target, the event actually travels all the way up to the document route again, in the so-called bubbling phase, so we say the events bubble up from the target to the document root and passes through all its parent elements, just parent elements not sibling elements.
- The importance of knowing this process is that it is as if the event also happened in each of the parent elements. so as the event bubbles through a parent element, it is as if the event had happened right in that very element. what this means is that if we attach the same eventlistner also for example to the section element in the example then we get the exact same alert window for the section element as well so we would have handled the exact same event twice, once at its target and once at one of its parent elements. and this behavior allow us to implement really powerful patterns.
- by default events can only be handled in the target and in the bubbling phase. however we can set up event listner in away that they listen to events in the capturing phase instead.
- Also not all types of events do have capturing and bubbling phase. Some of them are created right on the target element, and so we can only handle them there.
- we also say events propagate which is really what capturing and bubbling is. It's events propagating from one place to another.
- my reflect: Event propagation means that an event has capturing,target and bubbling phase in which we can catch and handle the event by default events that propagates are handled in the target and bubbling phase we can reset the addEventListner default to catch events to be handled on the capturing phase by adding a third parameter to the addEventListner function to be true so the event handler will no longer listen to bubbling events but this is not necessary as bubbling phase is useful for something called event delegation. event propagting means like moving from one place to another in the dom tree and these places are with elements in a parent child relationship in the dom tree.

## Lecture no.191 Address: Event Propagation in Practice

### Type: Code

- Watch the video as the explaination of the previous theory lecture gets more clear in the practical
- bubbling phase is very useful in the event delegation that we will learn about in future lecture

## Lecture no.192 Address: Event Delegation: Implementing Page Navigation

### Type: Code

- check the code in page navigation section and watch the video examples in final folder, notes on code
- an important good use case of event delegation is when we are working with elements that are not yet on the page on runtime so by the time the page loads and a great example are buttons that are added dynamically while using the application. so it is not possible to add event handlers to elements that do not exist but we will still be able to handle events on elements that don't exist at the beginning by using event delegation one more time.

## Lecture no.193 Address: DOM Traversing

### Type: Code

- check the code examples in final folder,
- Dom traversing means walking through the DOM, which means we can select an element based on another element. This is important when we need to select an element relative to a certain other element for example, a direct child or a direct parent element.or sometimes, we don't know the structure of the DOM at runtime and in all these cases we need DOM Traversing.

## Lecture no.194 Address: Building a Tabbed Component

### Type: Code

- check the video to learn more and the code examples in final folder, notes on code

## Lecture no.195 Address: Passing Arguments to Event Handlers

### Type: Code

- check the code fade section examples in final folder, notes on code

## Lecture no.196 Address: Implementing sticky navigation: The Scroll Event

### Type: Code

- check Sticky navigation section in examples in final folder.
- sticky navigation is an effect to make the naviagation bar attached to the top of the page after we scroll to a certain point.
- avoid scroll event as it is not efficient and cause perfomance issues

## Lecture no.197 Address: A Better Way: The Intersection Oberver API

### Type: Code

- check the code examples in final folder, notes on code
- implementing the same sticky navigation using the new intersection oberver API
- What is intersection observer API and why is it so helpful? this api allows our code to basically observe changes to the way that a certain target element intersects another element, or the way it intersect the viewport. and this is will be very useful implementing the sticky navigation.
- first create a new IntersectionObserver(pass a callback, object of options) and store it in a varible
- watch the video to learn more needs practice

## Lecture no.198 Address: Revealing Elements on Scroll

### Type: Code

- check the video and practice, The code examples in final folder, notes on code
- we are using the intersection API to reveal Elements as we scroll close to them to learn implementing these kind of effects without using external library

## Lecture no.199 Address: Lazy Loading Images

### Type: Code

- check the video needs practice and the code examples in final folder, notes on code
- lazy loading images is a strategy to optmize loading images by having a very low resolution image which is really small and which is loaded right in the beginning as we scroll to one of these low resolution images we will then replace this low resolution image with the high resolution one.

## Lecture no.200 Address: Building a Slider Component Part 1

is

- check the code and the videos needs practice examples in final folder, notes on code

## Lecture no.201 Address: Building a Slider Component Part 2

### Type: Code

- check the code and the videos needs practice examples in final folder, notes on code

## Lecture no.202 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.203 Address: Efficient Script Loading: defer and async

### Type: Theory

- Theory pdf pages 148-151
- We will learn about different ways to load JS script in HTML.
- We always used the regular way which is including the script tag without any attribue at the end of the body tag in the HTML file to make sure that DOM tree is created before executing any of the JS code, the other ways is to include async attribute or defer attribute in the script tag. These attributes influence the way JS File is fetched which basically means downloaded and the executed.
- We can write the script tag in the document head or usually at the end of the body. These are the two situation showing the comparison among including the script tag without any loading attribue or with defer attribute or async attribute in the slide.
- the comparison, what the page loading process will look like over time in the following cases:
- first, without any attribute, adding the script tag in the head, as user loads the page and receives the html, the html code will start to be parsed by the browser and parsing the html is basically building the dom tree from the html elements. then at a certain point it will find the script tag, start to fetch the script, and the execitontentLoadet event will finally get fired, and this is not ideal at all we don't want the browser setting there doing nothing cause this can have huge impact on the page performance plus in this case, the script will actually be executed before the DOM is ready and so again that's not ideal. so never do this never include the script in the head like this. That's whay we put the script tag at the end of the body , so that all the html is already parsed, when finally reaches the script tag. see in the slide the figure that shows how the page loading process looks like in case of adding script tag at the end of the body tag as it shows that the html is parsed then script is found at the end of the document then the script is fetched and then finally the script is executed then DOMConentLoaded Event is fired. then resources like images and css files are loaded then you the window load event is executed if you add any in the script file. now you know why we put it at the end of the body how ever this is stilll not perfect because the script could have been downloaded before, while the html was still being parsed.
- second, with async, see the figure showing how the page loads if we put the script tag with async attribute at the head tag, the different is that the script is loaded at the same time as the html is parsed so in asychronous way how ever the html parsing still stops for the script execution so the script is actually downloaded asynchronously but then it is executed right away in a synchronous way so the html code has to wait for being parsed. but anyway as we can see from the length of the diagrams, this still makes page loading time shorter.
- third, with defer, with putting the script tag in head tag with defer attribute. The script is loaded a synchronosly but the execution of the script is deferred until the end of html parsing. So in practice, loading time is smililar to the async attribute but with the key difference that would defer the html parsing is never interrupted, because the script is only executed at the end and many times this is exactly what we want.
- adding defer and async in the body doesn't make sense, because in the body fetching and executing the script always happens after parsing the html anyway and async and dever have no practical effector. as they don't have practical effect of adding them at the end of the body at all. They will make no difference.
  Now, there are, of course use cases for all these strategies, so let's compare them execpt the regular loading in the head, which is completely ruled out.

- So comparing regular way at the body end , async in head and defer in head:
- with async in head, DOMContentLoaded event is fired off as soon as the html finishes parsing. it doesn't wait for async script to finish executing. this happens when a big script takes long time to load.
  it is alse not guaranteed that async script will be executed in the exact order that they are declared in the code. so the script that arrives first gets executed first.
- with defer in head, it forces the DOMContent Loaded event to only get fired after executing the whole script is downloaded and executed. Also it is guaranteed that the script is executed in order the order they are declared or written in the code and that's usually what we want to happen. So as a conclusion, using defer in the head is the best solution. So, you should use it for your own scripts where the order of execution is important. for example if your script relies on some third party library that you need to include, you will include that library before your own script, so thay your own script can use this library's code. and in this case use defer not async as defer guarantee the correct order of execution. for third party scripts that the order doesn't matter for example analytics software like google analytics, or an ad script or something like that, then in this case, you should totally use async. so for any code that your own code will not interact with use async.
- only modern browser support async and defer. they will get ignored in old browsers. So, if you need to support old browsers use script tag in the body end not in the head, as defer and async is html5 feature so you can't work around this limitation in case of supporting old browsers like you can do with modern javascript features by transpiling or polyfiling.
- check video at 9:00 to see an example of using defer and regular way in the body end.

..........................................................................................................

Section no.14 Address: Object-Oriented Programming (OOP) With JavaScript

.............

## Lecture no.206 Address: What is Object-Oriented Programming?

### Type: Theory

- Theory pdf pages 153-161
- in this lecture we are going to take a high level look at the oop paradigm. We will learn what is oop and how it works in general and its 4 fundemental principles.
- oop is a programming paradigm based on the concept of objects. Paradigm means the style of the code, how we write and organize code. we use objects to model(describe) aspects of real world like a user or todo list or more even abstract features like html component or some kind of data structure.
- objects may contain data( we call them properties) and code(we call them methods). By using objects we pack data and the corresponding behaviour all into one block. That's make it easy to act directly on the data.
- in oop, objects are self-contained pieces/blocks of code like small applications on their own. then we use these objects as building blocks of our applications and make objects interact with one another. Interactions happen through a public interface api this interface is a punch of methods that the code outside of the objects can access and use to communicate with the object.
- The goal of oop is to organize code and make it more flexible and easier to maintain. before oop we had code gatherd across multiple functions, or even in the global scope without any structure. We call that call spaghetti code which make maintaining large code bases hard and adding new functionality even harder. so oop made up to solve this issue and now it is used in large scale software engineering.
- we have been using oop and objects as loose collection of data without making them interact with one another. Also, We dind't have a way to generate objects programmatically all we used is object literals, but in oop, we need a way to generate so to create, new objects from our code. to do that in traditional oop we use classes.
- you can think of a class as a blueprint which we can use to create a new objects based on the rules described in the class. it's like an architecture where the architect develops a blueprint to exactly plan and describe a house but a blueprint is just an abstract plan, like a set of rule but no thing tangible that you can actually touch however from this blueprint many real houses can the be built in the real world and with classes it is just the same.
- a user class example in the pdf not writen in javascript but it shows this class having everything related to a user data and behaviour all packed into one nice self contained block. so we can use this class and create a new object. The object will contain real data about the user in the object and not just a description of the data like we have in the class. We call objects created of the class instances of the class. So, an instance is a real object that we can use in our code which was created from a class, and the class it self is not an object. so, this instance is like a real house based on the house blueprint analogy which was created from the abstract blueprint created by the architect. we can use the class to create as many instances as we need in our application. these instances can have different data in them but they all share the same functionality which id login and send messages methods in the user class.
- how to design a class? or how to model real data into classes. it is like a question an architecture student asking how to design and plan a house. The answer is there is not a single correct way to design classes. There are however, four fundemental principles that can guide us toward a good class implementation. These princibles are abstraction, encapsulation, inheritance, and polymorphism. These are actually techniques that can also be used outside of oop but they are especially relevant in this context.
- see the pdf to get more info about these princibles.
- abstraction is to be concerned about what you really need in your application which means hiding the unnecessary details that don't matter. This principle blends with the next one encapsulation.
- encapsulation, keeping some properties and methods private inside the class so they are not accessible outside the class, some methods can be exposed as a public interface API. and this API is used to allow interactions between objects throught this public interface API. by having some properties private we are preventing external code to accidently manipulate the internal state. The term state simply refers to an object data. this is important as allowing external code to accidently manipulate internal data cause bugs espically in large projects and with many developer teams. So, public interface is all the properties and methods that are not private so that are not encapsulated. making methods private makes it easy to change internal code without breaking external code which might rely on these methods. this helps avoiding bugs and spaghetti code. so nicely encapsulate most of our state and methods and only leave essential methods public for the reasons that was explained.
- Inheritane, used to avoid duplicate code, so when we have two classes closely related we can have one class inherit from the other which means one parent class and one child class where child extends the parent and the child will take all properties and methods (inherit them) and use them. so inheritance makes the properties and methods of parent class available to child class and the point is to use the same logic that is common to both of the classes and to model real world relationships. that makes the parent class global and the child class more specific as they can have their own properties and methods not shared with the global class so we can say the child class an extended class with some added functionality.
- polymorphism, it means in greek many shapes, in context of oop, it means that a child class can overwrite a method that it inherited from the parent class. simply by giving the child class the same methods name with different implementation.

## Lecture no.207 Address: OOP in JavaScript

### Type: Theory

- Theory pdf pages 162-165
- We will learn about oop in JS, how is different form the traditional oop, and different ways to implement this paradigm in JS.
- Last lecture was about classical OOP: classes which a blueprint used to create objects that are called instances and this process is called instantiation so objects(instances) are instantiated from a class which functions like a blueprint. We talked about the class instance model as we have similar concepts in javascript plus the terminology used in this concept is used in JS and JS syntax itself uses some of these terms for example, instances. so you need to know what a class is and what an instance is .
- So, how oop works in JS? in JS we have something called prototypes, and all objects in JS are linked to a certain prototype object, so we say that each object has a prototype. the prototype object contains methods and properties that all the objects that are linked to that prototype can access and use and this behaviour is usually called prototypal inheritance. So, prototypal inheritance means that all objects linked to a certain prototype object can use the methods and properties that are defined on that prototype. so basically, objects inherit methods and properties from the prototype object which is the reason why this mechanism is called prototypal inheritance. just note, this inheritance is different form the inheritance we talked about in the last lecture which was that class iheriting from another class. but in prototypal inhereitance it is basically an instance inheriting from a class. so that's very different and keep that in mind. Now, we can say that object delegate behavior to the linked prototype object. and behaviour is just another term for methods here. beside prototypal inheritance we also call this mechanism, delegation. and that's why the arrow in the pdf slide between object and prototype is pointing upwards because technically objects delegate their behavior to the prototype. on the other hand in classical oop with classes the behaviour or the methods are actually copied from the class to the objects and that is completely different.
- when we use a method on array and when we check the mdn docs online we see that Array.prototype.method() which means that all arrays that we create in our js code inherits this method. This Array.prototype includes all array methods including map this is this is where they are actually defined. so an array defined in code named num is linked to Array.prototype or linked to that array prototype and then it has access to the method defined in the Array.prototype object. so in a sense our array inherits the map method or we can say that the array delegated the behavior of mapping to its prototype. so, what matters is the map method is actually not defined on the num array itself, but on its prototype.
- how we create a prototype and how we link objects to prototypes and how we create new objects, without having classes from which we can instantiate objects? in summary how we implement oop in JS in practice?
- in JS we have three different ways of doing this: The constructor function technique,ES6 classes and also The Object.create() function.
- Constructor functions Technique to create objects programmatically using a function which also set the new object's prototype and this is actually how built-in objects like arrays, maps or sets are implemented.Also this is how OOP has been done in JS basically since the beginning.
- ES6 release introduced Classes in JS and now Es6 classes are actually the more modern way of doing OOP in JavaScript. Keep in mind this is not the kind of classes that we talked about. in the last lecture and in the last slide about traditional oop. They are called synthetic sugar over constructor functions. so this means that Es6 classes are basically just a layer of abstraction over constructor functions. it is just a nice syntax to make it easy on newcomers to do OOP in JS. but behind the scenes Es6 classes are actually implemented with constructor functions and so they also use prototypal inheritance just like we learnt in this lecture.
- Object.create() which is the easiest and most straightforward way of linking an object to a prototype object. however it is not as much used as the other two methods.
- we have to keep in mind that abstraction, Encapsulation inheritance and polymorphism are still valid and important concepts with prototypal inheritance. and we will learn how to use an implement these principles.

## Lecture no.208 Address: Constructor Functions and The new Operator

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.209 Address: Prototypes

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.210 Address: Prototypal Inheritance on Built-In Objects

### Type: Theory

- Theory pdf pages 166-169
- let's summerize what we learned in the past two lectures
- a constructor function has a prototype property which is an object and inside that object we define the method calcAge
- Person.prototype has a reference back to Person which is the constructor property
- so Person.prototype.constructor is gonna point back to Person itself.
- Person.prototype is not the prototype of person but it is the prototype of all the objects that are created through the person function.
- let's analyze creating the object with new keyword and calling the constructor function for example: const jonas = new Person ('Jonas',1990);
- check the 4 steps in code file in last lecture. with the 4 steps a new object is created programmatically stored in the jonas variable. This is how it works with function constructor and ES6 classes but not with Object.create way of prototypal oop keep it mind once we reach Es6 classes and Object.create lectures.
- The reason why this technique is powerful. as we define a method or a property with prototype property the created object doesn't have this method or property on them. when we call that method or property on the created object js doesn't find it in the created object so it searches for it into its prototype and find it and this called prototypal inheritance or delegation. so for example jason object inherited the calcAge method from its object prototype or it delegated the calcAge functionality to its prototype.
- now, we can create as many objects as we like and then they will inherit this method calcAge. and we can call that method on all created objects and call the method without having it in all created objects and that is very powerful for code performance. imagine we have 1000 method in code and 1000 object that would affect dramatically on the code performance if we attched these 1000 method to each object in the 1000 objects we have.
- the fact of that the created object jonas is connected to a prototype and the ability of JS to look up methods and properties the constructorFunctionName.prototype is what we call prototype chain. so the crated object jonas and its prototype basically form a prototype chain and actually the prototype chain doesn't end here we need to know and understand more about it by looking at the whole picture explained in the second slide.
- constructorFunction.prototype is the prototype of the created objects from that constructor function it is also an object which createdd by the Object() constructor function and this object has a prototype which is Object.prototype which and the Object prototype value is stored in its **proto** which is null which means the end of the prototype chain.
- the prototype chain is the same as the scope chain whenever js can't find a variable in the current scope it look up to the next parent scope till it finds it and same as for prototype chain so whenever JS can't find a certain property or method in certain object it will search the next parent prototype in the prototype chain till it finds it and run it.
- example of using prototype chain is hasOwnPropery method which the method in the Object.prototyp first, when we call it on jonas like this: jonas.hasOwnProperty('name') js searches for this method in jonas but it can't find it then it searches for it in Person.prototype but it won't find it either then it searches for it into Object.prototype then it finds it, in case, we can't find in the top prototype chain then it will return an error.
- remember that methods are not copied to the object calling them instead it is inherited from objectConstructorFunctionName.prototype through the prototype chain.

## Lecture no.211 Address: Prototypal Inheritance on Built-In Objects

### Type: Code

- check the code examples in final folder, notes on code
- try to watch it again as it will make you understand alot of things.

## Lecture no.213 Address: ES6 Classes

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.214 Address: Setters and Getters

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.215 Address: Static Methods

### Type: Code

- check the code examples in final folder, notes on code , note that the example used in the code is in the code of the first lecture
- let's check an example to understand static methods , first run Array.from method in the console which is a built-in method that converts any array like structure (iterator) to a real array, example: run Array.from(document.querySelectorAll('h1')) in the console, this method Array.from is a method that is attached to the Array constructor not to the the prototype property of the constructor Array which can't be called on an array like this [1,2,3].from() it will give us an error and that's because all arrays don't inherit this method again because its not on their prototype its simply attached to the constructor itself. so Array.from() here is just a simple function that's attached to the Array constructor so as developer there are methods related to the Arrays constructors and there are methods related to Arrays prototype, we also say that the Array.from() method is in the array namespace we also used this term for some methods in the number in and in the internationalization name space for example Number.parseFloat(12) this method is another static method and it is static on the number constructor it is not available on numbers but only on this very constructor. We use these as a kind of helper that should be related to a certain constructor.
- we also can implement static methods on the constructor function as in the code example. we also can add it to class by adding static keyword before the method name in the class. see code example in ES6 lecture
- instance methods are the ones added to the instance objects and static methods are the ones added to the constructor object classes or function constructors.
- keep in mind that these static methods are not available on the instances, and they are useful to implement helper functions about the class or the constructor funtion.

## Lecture no.216 Address: Object.create

### Type: Theory and Code

- Theory pdf pages 170-172
- check the code examples in final folder, notes on code
- This is the third way to implement prototypal inheritance or delegation using a function called Object.create
- this way works in a different way than constructor functions and classes work. There is still the idea of prototypal inheritance however, there are no prototype properties involved and no constructor funtions and no new operator instead we use Object.create to essentially manually set the prototype of an object to any other object we want, so if we can set the prototype to any object, let's create an object that we want to be the prototype of all person objects. so let's recreate the person.
- this is the least used way to create prototype inheritance and this is only needed to know about Object.create will be used in inheritance between classes and constructor functions.

## Lecture no.218 Address: Inheritance Between "Classes": Constructor Functions

### Type: Theory and Code

- Theory pdf pages 173-178
- check the code examples in final folder, notes on code
- needs more understanding of prototype chain as in the end you manipulate the prototype chain manually.

## Lecture no.220 Address: Inheritance Between "Classes": ES6 Classes

### Type: Code

- check the code examples in final folder, notes on code
- note that the lecturer mentioned something about a mechanism of inheritance explored here that can actually be very problematic and dangerous in the real world when we are designing software and we will talk about that in functional programming which is kind of alternative to object oriented programming.

## Lecture no.221 Address: Inheritance Between "Classes": Object.create

### Type: Theory

- Theory pdf pages 179-181
- check the code examples in final folder, notes on code
- code and slides are straightforward

## Lecture no.222 Address: Another Class Example

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.223 Address: Encapsulation: Protected Properties and Methods

### Type: Code

- check the code examples in final folder, notes on code
- we have implemented a class in need for data encapsulation as explained its importance in last lecture code notes. In this lecture we will implement some data encapsulation to this class to fulfill its need.
- encapsulation means to keep some properties and method private inside of a class as needed. This means that these properties and methods are accessable only inside of the class and they are not accessible from ouside of the class and the rest of the methods are being expossed as a public interface which we call API.
- Two reasons we need encapsulation and data privacy. First, we prevent code from outside of the class to accidentally manipulate data inside the class and implement public interface so we can prevent manual mess with the properties and only by the public interface we can access and manipulate data inside of the class. Second, when we expose only a small interface so a small Api consisting only of a few public methods then we can change all the other internal methods with more confidence because we can be sure that external code does not rely on these private internal methods. So our code will not break when we do internal changes. And that's what encapsulation and data privacy are and the reason for it.
- However, Javascript classes actually doesn't yet support real data privacy and encapsulation. Now, there is a proposal to add truly private class fields and methods to the language, but it's not completely ready or official yet. We will explore this in the next lecture but even when these features ship in the browser it will take some time until you can use it with confidence.
- So, in this lecture we will fake encapsulation by simply using a convention.

## Lecture no.224 Address: Encapsulation: Private Class Fields and Methods

### Type: Code

- check the code examples in final folder, notes on code
- we will implement truly class fields and methods to make them private using the language tools not just a convention as we saw in last lecture.
- private class fields and methods are actually part of a bigger proposal for improving and changing JS classes which is simply called Class fields. This class fields proposal is currently at stage 3 so, right now it's actually not yet part of the JS language. however, once it becomes at stage 4 it will be part of The JS language. This will be soon in the future. so it is good to know about it also as in fact some of this proposal is working on google chrome.
- why this proposal called Class fields? as in traditional languages like java and c++ properties are usually called fields, so, with this idea JS is moving away from the idea that classes are just syntatic sugar over constructor functions. as with these features classes will have the ability we didn't have previously with constructor functions. This is a big issue for many developer. (I don't get why it is an issue , is the issue lacking these features or using classes which will hide the true nature of js prototypal inheritance nature.)
- in this proposal there are four kinds of fields and methods, and actually they are 8 but we are going to focus on these four (public fields, private fields , public methods, private methods)

## Lecture no.225 Address: Chaining Methods

### Type: Code

- Check the code examples in final folder, notes on code
- we will learn in this lecture to implement chaining ability to the method of our own class.
- This is easy to do all you have to do is to return the object itself in the method to make it chainable.
- just by returning this keyword which is the current object.
- notice that all methods in the code returns this keyword to make them chainable. This makes sense with all methods that sets a value to the object property.

## Lecture no.226 Address: ES6 Classes Summary

### Type: Theory

- Theory pdf pages 182-184
- check the video in the course to see class summary syntax example with explaination.
- very important to rewatch in case you need to summarize everything about classes.

..........................................................................................................

Section no.16 Address: Asynchronous JavaScript : Promises, Async/Await, and AJAX

.........

## Lecture no.246 Address: Asynchronous JavaScript, AJAX and APIs

### Type: Theory

- Theory pdf pages 197-203
- we will learn what asynchronous JS is and popular use cases of asynchrronous JS which is to make ajax calls to APIs.
- first we learn about synchronous code before learning about asynchronous code.
- most of code we wrote was synchronous code. synchronous means code is executed line by line, in exact order of execution that we define in our code so first line of code is reached execution, it is simply executed in the execution thread. execution thread is part of the execution context which actually executes the code in the computer's cpu. Then the next line of code is executed then the next all in sequence so each line waits for the previous line to finish execution. This can create a problem when one line takes a long time to run. for example in the slide we have an alert statement, which creates this alert window which will completely block the code execution so, nothing will happen on the page till we click the ok button and then the code can continue executing. Alert statement is a good example of a long running operation that block the code execution. and this illustrates the problem of synchronous code. most of time synchronous code is fine and make perfect sense but imagin that the execution would have to wait for like five second timer to finish that would be terrible as mean while nothing on page will work during these five seconds.
- so we need asynchronous code to solve the synchronous code issue when needed.
- in the example of asynchronous code slide , we have the setTimeout function. this function starts a timer in an asynchronous way that doesn't block the code. which means the timer will run in the background without preventing the next lines of main code from execution. we also registered a callback function that will not be executed now but it will be executed after the timer is finished running. This callback function is asynchronous JS. it is asynchronous as it will be executed after a task is running in the background finishes execution in this case that is the timer. so this callback is now registered for execution after the timer finishes and it doesn't block the next lines to be executed and execution does not wait for the asynchronous timer to finish its work. so this code in the timer function is nonblocking and we call it asynchronous and once the timer finishes the callback will be executed as well. this action is deferred to future here in order to make the code non-blocking.
- asynchronous programming is all about coordinating the behaviour of our program over a certain period of time. I say (this period of time might be undefined in some cases and this essential to understand to implement code depends on an undefined period of time) so literly asynchronous means not occuring at the same time and I say (not occuring at the same sequense as written in code and we might not know when it will finish over time).
- we need to know that we want a callback function to implement this asynchronous behaviour. however this doesn't make call back functions asynchronous. we have function accepts a callback function like map and that doen't make it asynchronous. only certain functions makes the code asynchronous like setTimeout function. then we have to know which ones do and which ones don't.
- another example of asynchronous code is loading a pic as resetting the src attribute of an image element. as images might be big ones setting src attribute was implemented in JS to be asynchronous code. once the image finishes loading a load event will automatically emmitted by JS on that image so we can listen for that event in order to act on it as in the example in the slide. we provide a callback function to be executed once the image finishes loading.
- instead of blocking in the image example execution moves on the next line. and once the image finishes loading and as we listen to that loading event callback function will be executed and once more we deferred an action into future making a code asynchronous and non-blocking.
- again event listners and callback funtion alone doesn't make code asynchronous notice that setting src attribute affected the behaviour of the callback and the eventlistner and made the code asynchronous as loading asynchronously in the background so what matters is the asynchronous behaviour of a task makes code asynchronous like running a time or loading an image. Also waiting for events like click event to happen doesn't make the event listener asynchronous it is just waiting for the click event to happen.
- there are more examples of asynchronous behaviour of tasks in JS like Geolocation API and AJAX calls.
- AJAX calls are probably the most important use case of asynchronous JS.
- What is AJAX? see slides, in practice we use it to request data from remote web servers dynamically which means without reloading the page so that we can use the data in our app dynamically.
- how does AJAX works? imagine we have our application running in our browser and we want data from a remote server. With AJAX we can do http request to the server, and the server will send us a response with the data and all that works in the background without blocking any code. we can make get request to receive data and post request to send data to the server and we will get these types of requests later in other lectures. When we ask the server to send us data the server contains a web API which has the data we need.
- what is an API and what web APIs actually are. see slides, the definition in the slide is in general term and on a very high level of abstruction definition. They allow apps to talk to each other and exchange information and that is true not only for web development an JS but also for programming in general. There are many types of apis like DOM API and Geolocation API we call them apis as they are self contained piece of software that allow other pieces of software to interact with them like the mapty app communicating with geolocation api. Also we can always implement a small and simple api in a class where we make some methods available as a public interface so objects made from a class can be seen as a self-contained encapsulated piece of software that other pieces of software can interact with and so that fits the definitin of API.
- The Important type of API we are actually interested in when we use AJAX and that the lecturer likes to call it online APIs which is an application running on a server that receives requests for data then retrieves the data from some database and send back as response to the client in practice we simply calls these online apis just API, or other people name it web API we came up with the name of online api as the term web apis are also used to describe other things. building online apis requires back-end development. so development with servers and databases and all that, check nodejs course it talks about that building online apis topic in details. for now, we are interested in using 3rd party apis. so apis that other developers make available for us most of the times for free.
- example of third party apis, let's now imagine we are building a traveling application, and you have a database with a different destinations and tours that you're offering so on your own server you could build your own API that can receive requests from your front end application in JS and send back the results so that would be your own API hosted on your own server but that's alone wouldn't be enough to build a complete application so you could use some 3rd-party APIs and there are really APIs for everything in our example of building traveling app. We can use a third party api to get weather data in our destinations, data about the destinations countries themselves, data about flights , about currency conversions data or you could use apis to send emails or text messages or embed google maps into your applications and the possibilities are endless with apis and we can say that apis is what modern web possible in the first place.
- APIs data format , the x in AJAX stands for xml which is a data format which used to transmit data on the web how ever these days no apis uses xml data anymore, the term ajax is just an old name and was popular back in the day but we still use the term even though we don't us xml format anymore. Most apis use the json data format so json is the most popular data format today because it's basically just a JS object but converted to a string so it is very easy to send across the web and also to use in JS once the data arrives.

## Lecture no.248 Address: Our First AJAX Call: XMLHttpRequest

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.249 Address: How the Web Works: Requests and Responses

### Type: Theory

- Theory pdf pages 204-207
- This lecture provides a high level overview of how the web works behind the scenes in regards of Requests and Responses
- a url consists of httpProtocol//address/resources , http is the protocol that allows two parties the web client and server to communicate , address is an easy name for the server, what happens when we use the url to communicate with a server is that the browser make a request to a dns server to get the real ip address of the server we communicate with plus the service port on the server that has the resources we want, this process happens through the internet service provider.
- once we have the real ip address A TCP/IP connection is established between the client and the server this conncection follows the rules of TCP/IP which are a communication protocols that defines the rules of how data travel over the web TCP responible of breaking and reassembling the requests and responces into small packets this is necessary so each packet can take a different route through the internet so the message arrives as quick as possible. IP protocol is responsible for sending and routing these packets to throught the internet it ensures they arrives at the right destination they should go to using ip addresses on each packet

## Lecture no.250 Address: Welcome to Callback Hell

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.251 Address: Promises and Fetch API

### Type: Code

- Theory pdf pages 204-207
- we will use the modern way of making AJAX calls with fetch API
- Calling fetch function returns a promise, const request = fetch('url');
- see definition and the advantages of using promises in the first slide in pdf
- see promises states over time or life cycle second slide
- two states pending and settled and settled states has two type of settled promises fulfilled and rejected
- we build our code logic around the states of the promise
- note a promise is settled once so the state will remain unchanged forever once the promise is settled so it is impossible to change the fulfilled or the rejected state.
- consume a promise is to use the promise to get a result and we depend on the states when doing so.
- before consuming the promise we need to build it. in our example above the fetch function is the one that builds the promise and returns it for us to consume.
- we don't have to build the promise to consume it as most of the time we consume the promise directly like we did with fetch.

## Lecture no.252 Address: Consuming Promises

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.253 Address: Chaining Promises

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.254 Address: Handling Rejected Promises

### Type: Code

- you need to work on all handling errors lectures in this section by writing code and deepen you
- check the code examples in final folder, notes on code
- in this lecture we will learn how to handle errors in promises in case something wrong went with them during the AJAX Calls.
- remember when a settled promise in which an error happens is a rejected promise. so we will learn how to handle promise rejections.
- The only way a promise rejects is when the user loses his internet connections. and for now, this is the only error we are handling for now, in this lecture.
- we need to simulate the losing internet connection using google chrome development tool, by going to Network tab and inside the Network bar change online to offline from the dropdown menu that you will find.
- rewatch this lecture along with code notes

## Lecture no.255 Address: Throwing Erros Manually

### Type: Code

- check the code examples in final folder, notes on code
- Errors that comes in the Response, where the promise is fullfilled with erros in the response.
- rewatch the lecture to understand it more clearly as a alot of code refactroring.

## Lecture no.257 Address: Asynchronous Behind The Scene: The Event Loop

### Type: Theory

- Theory pdf pages 212-215
- let's review what we learned about JS Runtime, JS Runtime is like a container which includes all the pieces necessary to execute JS code.
- The heart of every JS runtime is the engine, this where code is actually executed in the call stack and where objects are stored in memory in the heap.
- We have to put in mind a very important note which is JS has only one thread of execution so it can only do one thing at a time. There is absolutely no multitasking happening in JS itself. despite the fact that other language like Java can execute multiple pieces of code at the same time but not JS.
- we have web APIs environment, these are APIs provided to the engine, but which are actually part of the JS language itself. These are things like DOM , timers, fetch API , Geolocation API and so on and so forth.
- we have the callback queue, This is a data structure that holds all the ready to be executed callback functiond that are attached to some event that has occurred. Whenver the call stack is empty the event loop takes callbacks from callback queue and puts them into call stack so that they can be executed.
- The event loop is the essential piece that makes asynchronous behaviour possible in JS, it is the reason why we can have a non blocking concurrenecy model in JS.
- A concurrency model is simply how a language handles multiple things happening at the same time. But now, How the non blocking concurrency actually work? and why the event loop is so important? that's what we learn next in this lecture.
- To answer the above questions we need to focus on the essential parts of the runtime here. and they are the call stack, the event loop, the callback queue, and the web APIs.
- as we know that the JS engine is built around the idea of a single thread but if there was only one thread of execution in the engine then how asynchronous code be executed in a non blocking way? we will how JS concurrency model really works behind the scenes using all of the parts of the JS runtime we already know. And as always we will do this by looking at a real code example in the second slide.
- we walk through the code line by line and we keep updating the call stack as we go, we already know how the call stack works we need to focus on the web APIs and callback queue.
- first , we select the image element and then we set the sourse attribute of that image to dog.jpg as we know this will start to load the image asynchronously in the background in the background in this time we will understand what that mysterious background actually is, so as you already know everything related to the DOM is not really part of the JS, but of the web APIs and so it's in a web APIs environment where the asynchoronus tasks related to the DOM will run and in fact the same is true for timers AJAX calls and really all other asynchronous tasks so againg these asynchronous task will all run in the web APIs environement of the browser. Now, If the image would be loading in a synchronous way it would be doing so right in the call stack blocking the execution of the rest of the code but as we already learned, that would be terrible and that's why loading images in JS is asynchronous so, it is not happening in the call stack so not in the main thread of execution, but really in the web APIs environment as we mentioned before. Now, if we want to do something after the image has finished loading, then we need to listen to the load event and that's what we are doing exactly in the next line of code. So here we attach an event listener to the load event of that image and pass in a callback function as always. In practice this means to register this callback in the web APIs environment exactly where the image is loading and the call back will stay there till the load event is emitted So, we are handling asynchronous behavior here with a callback just as we learned before, but anyway, moving to the next line we make an ajax cal using fetch API and as always the asynchronous fetch operation will happen in the web APIs environment and again that's because otherwise we would be blocking the call stack and create a huge lag in our application. Finally we use the then method on the promise returned by the fetch function and this will also register a callback in the web API environment so that we can react to the future resolved value of the promise. So this callback is associated with the promise that is fetching the data from the 3rd party API in this example and that's gonna be important later on. So with this, we have now executed all the Top level code So, all the code that is not inside any callback function in asynchronous way. We also have the image loading in the background and some data being fetched from an API (multi tasks happening in the same time). now, it's time for this to get really interesting. Let's say the image have finished loading and therefore the load event is emitted on the image so what happens next is that the callback for this event is put into the callback queue and the call back queue is basically an ordered list of all the callback functions that are in line in the callback queue to be executed. you think of a callback queue as a todo list you write for yourself with all the tasks that you have to complete so the callback queue is like a todo list with tasks that the call stack will eventually have to complete. Now in this example , there are no other callbacks in the queue yet but there could be of course so if there were already other callbacks waiting in line, then this new callback would of course go straight to the end of the queue and there it would simply sit patiently for its turn to finally run and this actually has big implications so, imagine that you set a timer for five seconds and so after the five seconds that timer's callback will be put on the callback queue, and let's say there were already other callbacks awaiting and let's also say that it took one second to run all of those callbacks then in that case your timers callback would only run after six seconds and not after five. so. these six seconds are the five seconds that passed for the timer plus the one second that it took to run all the other callbacks that were already waiting in line in front of your timer so what this means is that the timers duration that you define is not a guarantee. The only guarantee is that the timers callback will not run before five seconds, but it might very well run after five seconds have passed. So it all depends on the state of the callback queue and also another queue that we are gonna learn about in a second. Now. another thing that's important to mention here is that the callback queue also contains callbacks coming from Dom events like clicks or key presses or whatever. Now, we learned before that DOM events are not really asynchronous behaviour, but they still use the callback queue to run their attached callbacks so if a click happens on a button with addEventListener then what will happen is just like what happend with the loading event in this lecture (like what was illustrated here).
- Now, it is time to learn about the event loop, What the event loop does is that it looks into the call stack and determines whether it empty or not execept of course the global context, then if the call stack is empty which means that there is currently no code being executed then it will take the first callback function from the callback queue and put it on the call stack to be executed and this is called an event loop tick so each time the event loop takes a callback from the callback queue We say that there was an event loop tick. So, as we can see here the event loop has the extremely important task of doing coordination between the call stack and to callbacks in the callback queue. So, the event loop is basically who decides exactly when each callback is executed. We can also say that the event loop does the orchestration of this entire JS runtime. Another thing that becomes clear from this whole explaination is that the JS language itself has actually no sense of time that's because everything that is asynchronous doesn't happen in the engine it's the runtime who manages all the asynchronous behaviour and it is the event loop who decides which code will be executed next but the engine itself simply executes whatever code it has been given to it.
- To recab: The image started loading asynchronously in the web APIs environment and not in the call stack we then used addeventlistener to attach a callback function to the image load event and this callback is basically asynchronous code , a code that we defereed into the future because we only want to execute it once the image has loaded and in the meantime, the rest of the code kept running. Now, addeventlistner did not put the callback directly in the callback queue it simply registered the callback, which then kept waiting in the web APIs environment untill the load event was fired off only then the environment put the callback into the queue then while in the queue the callback kept waiting for the event loop to pick it up and put it on the call stack and this happened as soon as the callback was first in line in the callback queue and the call stack was empty. So all this happened so that the image did not have to load in the call stack, but in the background in a nonblocking way. So, in a nutshell, the web APIs environment, the callback queue and the event loop , all together, make it possible that asynchronous code can be executed in a non blocking way event with only one thread of execution in the engine.
- That's alot to understand but we are not done yet, because we still have to fetch function getting data from the ajax call in the background and this is basically happening with a promise. Remember now, with promises things work in a slightly different way which is why I included this promise example as well.
- So, let's say that the data has now finally arrived and so the fetch is done. Now, callbacks related to promises like the one we registerd with the promises then method doesn't actually go into the callback queue. instead, callbacks of promises have a special queue for themselves, which is called microtasks queue.
- What is special about the microtasks queue is that it basically has priority over the callback queue. So, at the end of an event loop tick, so after a callback has been taken from the callback queue, the event loop will check if there are any callbackes in the microtasks queue and if there are, it will run all of them before it will run any callback from the regular callback queue and by the way we call these callbacks from promises microtasks and therefore the name microtasks queue and ther are actually other microtasks but that's not relevant here.
- So, going back to our example, currently we have a microtask setting in the microtask queue, the call stack is also empty and therefore the event loop will now take this callback and put it in the call stack just like it does with callbacks from the callback queue and it doesn't matter if the callback queue is empty or not. So, this would have worked the exact same way even if there were some callbacks in the callback queue and again that's because microtasks always have priority. In practice, this means that microtasks can basically cut in line before all other regular callbacks. Now, if ne microtask adds new microtask then that new microtask is also executed before any callbacks from the callback queue and this means that the microtasks queue can essentially starve the callback queue because if we keep adding more and more microtasks, then callbacks in the callback queue can never execute. Now, this is usually never a problem but I just wanted to mention this possibility here anyways, who knows this could be an interview question someday and if so, you would now know the answer.
- Anyway, as you can hopefully see the idea of running asycnchronous code with regular callbacks and with microtasks coming from promises is very similar. The only difference is that they go into differenct queues and the event loop gives microtasks priority over regular callbacks. All right, and thats finally it. This all you need to know about how asynchronous JS really works behind the scenes. This is really important becuse you will be very confident when you write asynchronous code now. And Also you will ace any job interview question about asynchronous JS. And actually so many JS developers don't know anything about this so this will put you into the top 10% or event top 5% of JS developers.

## Lecture no.258 Address: The Event Loop in Practice

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.259 Address: Building a Simple Promise

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.260 Address: Promisifying The Geolocation API

### Type: Code

- You need to work on the geolocation project first.
- check the code examples in final folder, notes on code

## Lecture no.262 Address: Consuming Promises with Async/Await

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.263 Address: Error Handling With try...catch

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.264 Address: Returning Values from Async functions

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.265 Address: Running Promises in Parallel

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.266 Address: Other Promise Combinators: race, allSettled and any

### Type: Code

- check the code examples in final folder, notes on code

..........................................................................................................

Section no.17 Address: Modern JavaScript Development: Modules, Tooling, and functional

.........

## Lecture no.270 Address: An Overview of Modern JavaScript Development

### Type: Theory

- Theory pdf pages 217-219
- We will start this section with a general overview of modern JavaScrip development. Basically of how we write JS today.
- When we build applications, we don't just write all of our code into one big script and send that script as it is to the browser, it used to be like this but this way has changed. we used to write JS applications in one script or multiple scripts.
- Today, we divide our projects into multiple modules and these modules can share data between them and make our code more organized and maintainable.
- One great thing about modules is that we can also include 3rd party modules into our own code as there are thounds of open source modules which we also call packages that the developers share on the NPM repository and then we can use these packages for free in our own code. For example, the popular React framework or jQuery, or event the Leaflet library, that we used before in our Mapty project. All of these packages are available through NPM.
- NPM,stands for Node Package Manager as it was originally developed together with Node.js and for Node.js however NPM has established itself as the go to repository for all kinds of packages in Modern JS developement.
- In order to download and use and share packages, we use the NPM software installed on our computer which is just a simple commannd line interface that allows us to do all that.
- So, basically NPM, is both the repository in which packages live and a program that we use on our computers to install and manage these packages.
- Let's say that we are done writing our project code so, we divided it into multiple modules and we included some 3rd party modules as well and so now the development step is complete.
- However, usually that's not the end of the story at least not when we are building a real world application. Instead, our project now needs to go through a build process, where one big final JS bundle is built and that's the final file, which we will deploy to our web server for production. So, basically it is the JS file that will be sent to browsers in production.
- Production simply means that the application is being used by real users in the real world.
- A build process can be something really complex, but we are gonna make it simple here and only include two steps. First step, we will bundle all our modules together into one big file. This is a pretty complex process which can eliminate unused code and compress our code as well. This step is super important for two big reasons. First, older browsers don't support modules at all and so code that's in a module could not be executed by any older browser. Second, it's also better for performance to send less files to the browser, and it's also beneficial that the bundling step compresses our code. Second step we do something called transpiling and polyfiling, which is basically to convert all modern JS syntax and features back to old ES5 syntax, so that even older browsers can understand our code without breaking. and this is usually done using a tool called BABEl. We talked earlier about converting modern JS to ES5. In this section we will do this. So these the two steps of our build process.
- After these two steps, we end up with that final JS bundle, ready to be deployed on a server for production.
- These steps are not done by ourselves. we use a special tool to implement this build process for us. The most common build tools available, are probably Webpack and Parcel. These are called JS bundlers because as the name says they take our raw code and transform it into a JS bundle. Now, WebPack is the more popular one, but it can be really hard and confusing to set it up. That's because there are alot of stuff that we need to configure manually, in order to make it work properly. Parcel, on the other hand is a zero configuration bundler, which simply works out of the box and with this bundler we don't have to write any set up code, which is really amazing. That's the JS bundler we are going to use in this section.
- These development tools are also available on NPM just like packages that we include in our code, we will download and manage tools using NPM as well. These tools include the live-server that we have been using all along, Parcel bundler that we just talked about or Babel to transpile code back to ES5.
- This is how we develop Modern JS application today. This is how professional developers actually write JS today and in the rest of the section, you will take a big step in the direction of becomeing a professional developer too.

## Lecture no.271 Address: An Overview of Modules in JavaScript

### Type: Theory

- Theory pdf pages 220-224
- We will learn about modules in more depth and how they work behind the scenes as they play a very important role in modern software development.
- module definition is in pdf. it sounds a bit like a function or a class but is usually a standalone file. it's not always the case but mostly when we think of a module we think of a separate file.
- it has imports and exports and module code. With exports we export values out of a module. for example simple values or even entire functions. Whatever we export from a module is called the public API. This is like classes where we can also expose a public API for other code to consume.
- Now, in case of modules, this public API is actually consumed by importing values into a module. so, just like we export values in modules, we can usually also import values from other modules. and these other modules from which we import are called dependencies because the code in our module can't work without the code that is in the external module we are importing from. This pattern is in all programming languages.
- the reason why we use modules are in pdf pages plus these reason starts to appear when we are working on large projects as the code base starts to grow more and more.
- Modules specifically in JS in second slide in pdf file.
- as of ES6 JS has a native built-in module system. we used to have modules before ES6 but we had to implement them ourselves or use external libraries. See ES6 modules definition in pdf files.
- compare between ES6 modules and scripts as they are both type of files to understand the differences.
- Top level variables in cas of ES6 modules are scoped to modules which means they are private to the module by default and the only way to access their values are by exporting that value as we learned in first slide. if we don't export no one from the outside can see the variables. in scripts top level variables are always global this could lead to problems like global namespace pollution, where multiple scripts try to declare variables with the same name and then these variables collide. so private variables are the solution for this problem and that's why ES6 modules implemented it like this.
- Next default mode, strict for ES6 modules and sloppy for scripts so there is no need to declare strict mode for ES6 modules.
- Top level This keyword, is alway undefined while in scripts it points at the window object.
- import and exports are only used in ES6 modules, no way to use them in scripts and note they always happen at the top level so as you know outside of any function and or any if block and we will know why in a second. Also all imports are hoisted So, no matter where in a code your importing values will be moved to the top of the file. in Practice importing values is always the first thing that happens in a module.
- Now, in order to link a module to an HTML file, we need to use the script tag with type attribute set to module, instead of just a plain script tag.
- Finally, about downloading module files themselves, this is automatically happens in an asynchronous way this is true for modules loaded from html as well as for modules that are loaded by importing one module into another using the import syntax. on the other hand regular scripts are downloaded by default in a blocking synchronous way, unless we use the async or differ attributes on the script tag.
- In the 3rd slide, we will learn how modules actually import other modules behind the scenes.
- we will analyze the code example in the 3rd slide, here we are importing a value called rand from math.js module and showDice from the dom.js module, Now, as always when a piece of code is executed, the first step is to parse that code which means to just read the code, but without executing it and this is the moment in which imports are hoisted and in fact, the whole process of importing modules happens before the code in the main module is actually executed. So in this example the index.js module imports the dom and math modules in a synchronous way which means that only after all imported modules have been downloaded and executed, the main index.js module will finally be executed as well. This is possible because of the top level imports and exports that's because if we only export and import values outside of any code that needs to be executed then the engine can know all the imports and exports during the parsing phase so while the code is still being read before being executed. now, if we were allowed to import a module inside of a function, then that function would first have to be executed before the import code happened and so in that case, modules could not be imported in a synchronous way so the importing module would have to be executed first.
- So, you might ask why we want modules to be loaded in a synchtonous way? the answer is that this is the easiest way in which we can do things like bundling and dead code elimination so basically deleting code that's actually not even necessary. and this is very important in large projects with hundreds of modules and that includes third party modules from which we usually only want small piece of code not the entire module. So, by knowing all dependencies between modules before execution, bundlers like webpack and Parcel can then join multiple modules together and eliminate that code. And essentially this is the reason why we can only import and export outside of any code that needs to be executed so like a function or an if block.
- So, moving on after the parsing process has figured out which modules it needs to import, then these modules are actually downloaded from the server and this downloading happens in an asynchronous way it is only the importing operation itself (figuring out which modules we need) that happens synchronously. Then after a module arrives, it's also parsed and the modules exports are linked to the imports in index.js.
  for example the math module exports a function called rand and this export is then connected to the rand import in the index.js module. and this connection is actually a live connection so exported values are not copied to imports. instead the import is basically just a reference to the export value like a pointer. so when the value changes in the exported module, then the same value also changes in the importing module. This important to understand as it's unique to ES6 modules as other module systems do not work like this but JS modules do So, you need to keep that in mind.
- next up, the code in the imported modules index.js is executed and with this the process of importing is finally finished.

## Lecture no.272 Address: Exporting and Importing in ES6 Modules

### Type: Code

- check the code examples in final folder, notes on code
- we will use modules in practice, to make sure that we understand how they work and to import and export values between them.
- first scenario, importing a module without importing any value, we will create a shoppingCart.js module it is convention to use camel case names.
- inside script.js which is the importing module and shoppingCart.js the exporting module. we need to specify the type attribute to be module in html file where we link script.js.
- notice that code in shoppingCart.js is executed first before script.js as code is parsed in script.js and the code in the exporting module is executed first before the importing module.
- to use variables defined in shoppingCart we use exports and there are two types of exports named exports and default exports
- named exports by adding export keyword before the definition of any variable export const addToCart then we go to script.js and import it `import {addToCart} from './shoppingCart.js';`
- the use case of named exports is to make multiple exports at the same time `export{variable names , };`
- use as keyword to change the name of the imported variable or exported variable
- `import * as ShoppingCart from './shoppinCart.js';` this will import everything that is exported from the module and create an object called ShoppingCart containing everything exported from the module shoppingCart.js and this will then create a namespace for all of the values exported from that module.
- you can access it like this ShoppingCart.addToCart('bread',5);
- we note that shoppingCart is creating a kind of a public API which is all the exported values and the object ShoppingCart is like an object created from a class which now has methods and properties (exported values)
- how to talk about default exports, we use default exports when we only want to export one default thing per module, that's the reason they are called default. check video 15:14
- `export default and the function value the code` then when we import it we can give it any name we want
- we can mix importing named and default exports but we don't do that in practice.
- make sure to put in mind that imports are not copies of the exports they are alive connection that means they point to the same place in memeory.

## Lecture no.273 Address: Top-Level await ES2022

### Type: Code

- check the code examples in final folder, notes on code
- Let's go back shortly to asynchronous JS, in ES2022 we can now use await keyword outside of async functions, at least in modules so, that's why this is here in the module section. and this why we call it Top-Level await and it fails in normal script.

## Lecture no.274 Address: Module Pattern

### Type: Code

- check the code examples in final folder, notes on code
- the one we used before ES6 for implementing modules in JS.

## Lecture no.275 Address: CommonJS Modules

### Type: Code

- check the code examples in final folder, notes on code
- Beside the native ES6 Modules and the module pattern, there are also other module systems that have been used by JS in the past. but again, they were not native JS so they relied on some external implementations. Two examples are AMD Modules, and CommonJS modules.
- CommonJS modules are worth taking a look at and we will do that in this lecture.
- CommonJS Modules are important for us because they have been used in Node.js for almost all of its existance. So, only very recently, ES Modules have actually been implemented in Node.js and rememeber Node.js is away of running Javascript on a web server, outside of a browser.
- The big consequence of this is that almost all the modules, in the npm repository that we talked about in the beginning of this section, still use the CommonJS module system. The reason for that is that npm was originally only intended for node. Which as they said uses CommonJS. Only later npm became the standard repository for the whole JS world. so we need to learn about as you will see a lot of CommonJS still around.

## Lecture no.276 Address: A Brief Introduction to the Command Line

### Type: Code

- check the video to learn more.
- Before using a tool like Parcel, we first need to learn a little bit about Command Line as all the built tools available on NPM only work in the Command Line. so we need to learn the basics of The Command Line.

## Lecture no.277 Address: Introduction to NPM

### Type: Code

- check the code examples in final folder, notes on code
- NPM stands for node package manager and it is both a software on our computer and a package repository.
- Why we need NPM? Why do we need a way of managing packages or dependencies in our project? Before we have NPM we used to include external libraries right into our HTML using the script tag and this would expose a global variable that we could use, and actually that's exactly what we did earlier in mapty project. Opening Mapty html file we can see a script tag including leaflet.js and did that before our own script so that our script could then use the global variable that was exposed by leaflet library here.
- this could create some problem especially in big projects may be not in this small one. But in a huge project and huge team this is just not manageable. First, it doesn't make much sense having the HTML loading all of our JavaScript, that is just really messy. Also many times we would actually download a library file to our computer directly, for example, jQuery JS file. and the whenever a new version come out we would have to manually go to the site, download the new version, change the file in our file system manually, and then include it here again, maybe with some other name, with some other version number and that was just a huge pain. and a third reason is that before NPM, there simply wasn't a single repository that contained all the packages that we might need and this made it even worse and more difficult to manually download libraries and manage them on our computers. in summary that was huge pain and huge mess.
- the reason of using NPM is to manage our dependencies in a better and modern way and NPM is exactly how we do that so let's use the NPM software now.
- So , get our terminal ready and check if the NPM is installed just type `npm -v`. if you didn't get a number install node.js and run the command and you will get npm version number.
- now, in a project we want to use npm we need to start by initializing it. by writing `npm init` this will ask us a couple of questions in order to create a package.json file if you keep on pressing enter you will accept the defaults.
- Then we get a file called package.json which will store all the entire configuration of our project.
- so, now we can install leaflet library we used it before but this time using npm. you need to check the documentation of this library to see how to install it with npm. checking the documentation we see that we write this commant `npm install leaflet` so we write npm to run NPM program then install command in the NPM program then the name of the package leaflet.
- We notice after doing that a new field here was created for the dependencies and the dependency that we have here now is leaflet then we notice a new folder called node_modules and this one contain leaflet folder inside the code of this library that we need to include in our page or project.
- the more packages we install they will get stored into the node module folder.
- so we installed leaflet but if we wanted to use it that wouldn't be easy without a module bundler and that's because this library actually uses the CommonJs module system so therefore we cannot directly import it into our code. We could only do that if later we used a module bundler, but for now we are not doing that. So, let's not use leaflet for now. So, this was just to show you how to install it. So, instead, let me show you how we can install and import one of the most popular JavaScript libraries, which is lodash so lodash is a collection of a ton of useful functions for erase, objects, functions, dates and more. so, it is alot of like functions that could or should be included in JS, but are not. And people simply implemented them in Lodash and now we can use them. The instructor didn't use the normal Lodash version as the normal one uses the commonJS and so we can't use commonJS modules without a module bundler so he looked for a special version. and that one called Lodash-es and es is because of ES modules. runing `npm install lodash-es` and here we now have one file for each of the methods that are available in Lodash, and the one we want to include is for cloning objects cloneDeep.js
- see comments on code.
- now, if I want to share my project with the use of package.json file and the terminal we can move our project anywhere and use command `npm i` to install all the dependencies in the new place or in the new computer as npm will reach to package.json file and install the dependencies for me.
- now, we know how to work with npm and download packages and also include them in our code. However importing packages like we did here for example by specifying this entire path is not practical at all. and in the next video, it is time to finally use Parcel to fix this.

## Lecture no.278 Address: Bundling With Parcel and NPM Scripts

### Type: Code

- Check the code examples in final folder, notes on code
- The module bundler we are gonna use in this course is called Parcel. It is fast and easy to use and it works out of the box without any configuration.
- There is another bundler called webpack which is the most popular bundler especially in react world. However, it's way too complex to use in a course like this so we learn how to use Parcel.
- Parcel is basically just another built tool which is also on NPM so we will use NPM to install it running `npm install parcel --save-dev` as this is a differenct dependency so we have to write --save-dev
- A dev dependency is like a tool that we need to build our application but it is not a dependency that we actually include in our code. so it is simply a tool so that's way it's called devDependency because we can use it to develop our project and therefore it appears here in a new field, in our package.json file. so dependencies are for libraries that we include in our code.
- now, we can use parcel the command line interface however we can't simply run parcel like this `parcel index.html` this is not going to work because the command is not found and the reason for that is simply that this doesn't work with locally installed packages and parcel was installed locally. so only on this project and that's way it showed up in the package.json file of this exact project so, there are also global installations but more about that by the end of this video. In order to be able to use parcel here in the console , we have two options so, we can use something called npx or we can use npm scripts.
- we start with npx which is basically an application built into npm `npx parcel index.html` the option we pass into parcel is the entry point index.html becuse it is where we included our script.js which is the file that we want to bundle up.
- In script.js we are including cloneDeep module from Lodash, and shoppingCart.js module. so the goal of using Parcel is to bundle these three modules together(script.js,shoppingCart.js and cloneDeep).
- So running `npx parcel index.html` will take sometime to build and starts a new development server on a new url. Opening this url will starts up our app. so, besides bundling, it also does exactly the same job as our live server. The difference is live server on port 8080 and and this one is on port 1234.
- if you face some issues trouble shoot in video at 5:40
- we don't need to put the type module attribute in the script tag as parcel simply creates a script and so, now we are actually no longer using a module but we are just using a regular script. This is important as modules doesn't work in older browsers. so we delete type module and save so parcel can rebuild our application.
- What parcel did, it created a folder called dist folder because this is the folder that we will send for production. opening it you will find a new index.html and other js files including the new script file created by parcel with our code from the modules. We notice that unused code is still there as removing the unused code is in the build step but now we are in the development step. So changing the code and save will reload and give us the changes just like live server. We can activate something even better which is called hot module replacement.
- see the if block in code
- what hot module reloading means is that whenever we change one of the modules, it will then, of course trigger a rebuild like this but that new modified bundle will then automatically like magic get injected into the browser without triggering a whole page reload.
- Also we can just write the library name in the import from statement and parcel will search for the imported value in that library. Review video at 10:00 till 16:00
- Using npm script is another way of running a locally installed packages in the command line, they also allow us to basically automate repetitive tasks and then we don't have to use npx command in the command line.
- we define a script by giving it a name "start" then value "parcel index.html" then in the command line we can write the command "npm run start" command as start is the name of the script that we defined in the package.json then we have a simple command that we can execute whenever we want to start parcel and start developing.
- when we are done developing it is time to build the final bundle. so the bundle that is compressed and has the dead code elimination and all that. then we write a script with name "build" and value "parcel build index.html" and run "npm run build" in the command line.
- we can install packages globally by running command `npm install parcel -g` -g stands for global. this was the way we installed live server package before and because of that we were able to use live server in every directory on our computer so the big difference between globally and locally installed packages and espacially these tools like parcel or live server is that we can use the global tools directly in the command line without the intermediate step of an npm script inside the package.json. However, most of these tools actually advise the developers to always install the tools locally so that they can always stay on the latest version.

## Lecture no.279 Address: Configuring Babel and Polyfiling

### Type: Code

- check the code examples in final folder, notes on code
- In this lecture we will configure babel to transpile our modern code to ES5 code. Parcel automatically uses Babel to transpile our code. we need to configure Babel to support some browsers but this is alot of work thta Parcel make it easy with its default decisions for transpiling with Babel.
- We will take a quick overview of how Babel work. When you check Babel documentation. We will see that Babel uses plugins and presets that can both be configured. A plugin is a specifically JS feature that we want to transpile. So, let's say we want to convert arrow functions back to ES5 but leave everything else usually we don't do that as we want to transpile everything then we use arrow functions. presets is a set of plugins that we use to transpile set of features instead of transpiling one feature using one plugin.
- Parcel uses a preset @babel/preset-env which will automatically select which JS feature should be compiled based on the browser support. this is automatic by parcel.
- the preset parcel uses doesn't support classes in video 5:00 we will learn how to transpile it.
- we add a plugin to class properties.
- note that features like pormises and arrays method like find are not transpiled. we only transpile syntax like const and let. So, we need to polyfill these features.
- Babel used to do polyfilling but recently they started to recommend other libraries. and we import these libraries.
- import 'core-js/stable' and parcel is smart enough to install this polyfilling library for us we just need to import it. we might need to install it ourselves in case we used another bundler rather than parcel.
- In video we needed to install it ourselves `npm install core-js` and the lecturer found installing the polyfilling library is strange as parcel is supposed to install it for us.
- checking the code we find that the features is the same as promise and the array method find is still the same . so, it doesn't transform their syntax. so the polyfilling redefine and recreate the method in away ES5 understand it and make it available in this bundle so the code can use it.
- searching Array.prototype.find you will get the method that's a proof of recreating find method.
- this polyfilling library add code that we might not need. If you want to reduce the size of the bundle you can import only what you need `import 'core-js/stable/array/find'` that would be alot of work that we usually ignore for now we only do it if you are worried about your bundle size.
- we also need to import another polyfilling library that polyfill a feature that is not in the above mentioned library core-js we first install it `npm install regenerator-runtime` and import it. `import regenerator-runtime/runtime` this is for polifiling async functions.
- this is like a recepie you have to follow we don't have to understand it in details enough knowing the difference between transpiling and polyfilling.
- with this we have finished learning about modern js development basically with learning about tooling such as parcel and babel and modules.
- in next lecture we will learn about modern JS coding, more on the actual programming side of things

## Lecture no.280 Address: Review: Writing Clean and Modern JavaScript

### Type: Theory

- Theroy pdf pages 225-228
- we will review on clean and modern js coding style in this lecture.

## Lecture no.281 Address: Let's Fix Some Bad Code: Part 1

### Type: Code

- Watch the video again

## Lecture no.282 Address: Declarative and Functional JavaScript Principles

### Type: Theory

- Theory pdf pages 229-232

## Lecture no.283 Address: Let's Fix Some Bad Code: Part 2

### Type: Code

- Watch the video again

....................................................................................................

# Section no.18 Address: Forkify App: Building a Modern Application

..............

## Lecture no.286 Address: Project Overview and Planning (1)

### Type: Code

- watch the video

## Lecture no.287 Address: Latest Code Updates (Parcel v2 and more)

### Type: Code

- watch the video

## Lecture no.288 Address: Loading a Recipe from API

### Type: Code

- watch the video

## Lecture no.289 Address: Rendering the Recipe

### Type: Code

- Watch the video

## Lecture no.290 Address: Listening for load and hashchange Events

### Type: Code

- Watch the video

## Lecture no.291 Address: The MVC Architecture

### Type: Theory

- Theory pdf pages 240-246
- In this lecture we will talk about project architecture and software architecture more in general.
- The reason why we need architecture, the architecture will give our project the structure in which we can write the code.Just like a house software also needs a structure.
- In software, structure means how we organize and divide the code into different modules, classes and functions. All these ways will hold the code toegether and give it a structure.
- The next reason for needing architecture is maintainability as we need to think about the future and keep in mind that the projct is never really done. we will always need to change things in the future and we will need to maintain the project and that only works if the project is nicely structured.
- Another reason is expandability, we also need to easily add new features to the project and that will be easy with a good structure and a good overall architecture.
- The perfect architecture is the one that allows for all the three mentioned aspects of structure, maintainability and expandability.
- To achieve that perfect architecture we need to create our own architecture from scratch and that what we did in our mapty project however this only works for small project like that one and when the project grows that would be hard to achieve a good architecture on our own so instead we can opt for a well established architecture pattern that developers hve been using for years or even for decades example for that Model view controller MVC architecture or model view presenter , flux or many other architectures.
- We can use a framework like react, angular , vue or svelte to take care of the architecture and in this case we don't have to think of the architecture on their own. This sound like a good idea especially for large scale applications however before using a framework you should really know JS very well. and that includes how to implement an architecture by yourself and that's what we are going to learn in this project. This will make it easier for me to learn react or vue or any framework.
- No matter where the architecture comes from and who develops it, there are some components that any architecture must have and they are: business logic, state , http library , application logic and presentation logic.
- Business logic: see presentation pdf for more info.
- State: application state is essentially stores all the data about the application that is running in the browser so the data about the application frontend basically. so state should store any data that you might fetch from an API or data that the user inputs or what page the user is currently viewing and so on and this data should be the so called single source of truth, which should be kept in sync with the user interface. So that means that if some data changes in the state then the user interface should reflect that. and the same is true the other way around so if something changed in the ui so the state should also change. storing and displaying data and keeping everythin in sync is one of the most difficult tasks when building web application that's way there are actually many state management libraries lik redux of Mobx. But in this project we will keep it simple and use a simple object to store our entire state.
- http library is simply responsible for making and receiving AJAX requests. and we have been doing that using fetch function. Most web applications need some interaction with the web and that't why this is an aspect to keep in mind.
- Application logic is about the code that is only concerned about the implementation of application itself.so it is more the technical aspects of the application, which are not directly related the underlying business problem. for example application logic includes handling of UI events and navigation on the page. that's the reason why this component is many times also called a router so basically mapping actions to the users navigation.
- Finally, the presentation logic, which also called the UI layer is all about the visible part of the application so essentially, we can say that the presentation logic is responsible for displaying the application state on the user interface in order to keep everything in sync.
- Any good architecture has a way to separate all these components so instead of mixing everything together in one big file and in one big mess.
- Now, let's take a look of some well esatablished architecture pattern that we are going to use.
- The Model-View-Controller(MVC)architecture, basically, it contains three big parts. View for the presentation logic, the part where the application is interacting for the user. Model is about the application data so that's why it usually contains the state and also the business logic that manipulates the state the model also contains http librarry that might get some data from the web like from API and some backend and this is also about the data so it is also goes to the model. Finally the controller is what it contains the application logic and it is kind of a bridge between the model and the view which in fact should know nothing about each other. So the model and the view will exist completely independent from one another, and not event knowing that the other one exist, so basically the big goal of the MVC pattern is to actually separate business logic from application logic which makes developing the application so much easier but as a consequence we need something to connect these two parts and that is the controller.
- see example at 10:30 in the video

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code

## Lecture no.227 Address: Lifecycle DOM Events

### Type: Code

- check the code examples in final folder, notes on code
