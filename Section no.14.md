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
