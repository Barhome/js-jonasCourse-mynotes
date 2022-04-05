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
