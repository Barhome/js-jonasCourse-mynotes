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