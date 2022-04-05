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

- Watch the video again.
