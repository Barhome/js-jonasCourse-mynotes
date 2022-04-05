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
