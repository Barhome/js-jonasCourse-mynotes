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
