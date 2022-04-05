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
