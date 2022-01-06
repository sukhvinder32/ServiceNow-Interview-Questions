# ServiceNow-Interview-Questions

***SERVICENOW***
- What is ServiceNow?
- What is the business model / how do you pay for the service?
- What is IT service management (ITSM)?
- What is cloud computing?
-  Advantages of cloud computing?
- What is SaaS? IaaS? PaaS?
- What is ITIL?
- What is incident management?
- Problem mgmt?
- Change mgmt?
- Asset mgmt?
- Release mgmt?
- What are Application & modules?
- What are workflows? How do you troubleshoot a workflow?
- How to setup notifications (SMS, email, etc)?
- What are events / event registry?
- What are event logs / debug events?
- What is CMDB (config mgmt database)?
- What is CMDB baseline?
- How does Asset and CI's are linked to each other?
- What is Business Service Map in CMDB?
- What is a record?
- What is Record Producer?
- Difference between Data Policy and UI Policy?
- What is the difference between async and after Business Rules?
- How do you upload multiple records?
- What is data lookup and record matching?
- What is a CI (configuration item)?
- How do you enable/disable an application in SNOW?
- What does it mean to impersonate a user?
- What are script includes?
- What is diff betw choice list and choice action?
- What are data dictionaries?
- What does coalesce mean?
- What are UI policies?
- What is a data policy?
- What is a client script?
- What is a business rule? How do you call it from client script?
- What is the Task table?
- What is UI action?
- What is a UI macro? How do you use it?
- What is a glide record?
- What is diff betw client script and catalog client script?
- What is diff betw global business rule and script include?
- What is ACL?
- What is table.none?
- What is table.*?
- What is table.field?
- How to create new tables/columns?
- What is diff betw parent / base table / core table / extended table?
- What is an update set? How do you merge/validate them?
- What is service catalog?
- What is diff betw service request and request item?
- What is diff betw task table and sc_task table?
- What is variable set?
- What is the diff betw before insert and after insert in business rule?
- What is diff betw onload and onchange client scripts?
- What does ServiceNow recommend to use - client script or UI policy? Which is better/ more efficient?
- What is Flow Designer?
- Difference between Asset and CI?
- UI Actions?
- Discovery integration with MID Server?
- Different steps involved in LDAP integration?
- SOAP and REST Webservices?
- Integration Hub using a Flow Designer?
- Asset Management (Entire Life Cycle)?
- Process and Data Flows in Domain Seperation?
- Difference betweeen Override and Dictionary Override?
- Difference between SLA, OLA and Underpinning Contract?
- What is Script Include?
- What is Server side and Client Side Script?
- Difference between GlideAJAX and GlideRecord?
- What is the difference between g_form.setdisplay and g_form.setvisible?
- What is Automated Tested Framework and what it is used for?
- What are Views in Forms?
- What is Form Section?


***Service Portal***
What is diff betw Service Portal and CMS system?
Can we domain separate Service Portal pages?
What are the basic components of a service portal?
What is a widget and what are its components?
What are pages?
How to secure service portal page?
What are features not supported in Service Portal?

***JAVASCRIPT***
- What is JavaScript?
- What is the DOM? How to manipulate the DOM?
- What are the JavaScript data types?
- What is the use of isNaN function?
- What are undeclared and undefined variables?
- How can you add new elements dynamically?
- What are the data types in JS?
- How can you use functions / different types of functions?
- What is hoisting?
- What are the new features of ES6?
- What are the scopes in JS?
- What are global variables? How are these variable declared and what are the problems associated with using them?
- Explain the working of timers in JavaScript? Also discuss the drawbacks of using the timer, if any?
- What is === operator? Compare with == operator?
- What is type coercion?
- Explain how can you submit a form using JavaScript?
- What is an undefined value in JavaScript?
- What are some common JavaScript events?
- Can we add more than one "document.ready()" function in a page?
- What are the four parameters used for jQuery.ajax method?
- What is Ajax?
- What are the advantages of Ajax?
- What are the disadvantages of Ajax?
- What are all the controls of Ajax?
- What are all the technologies (ie. think: protocol) used by Ajax?
- What is JSON?

***ANGULARJS***
Note: We did not learn AngularJS which is different from Angular.
I am currently learning AngularJS at https://www.codecademy.com/learn/learn-angularjs

The answers are from various sources/ will update.

## What is AngularJS? 
AngularJS is an open-source JavaScript framework used to build rich and extensible web applications. It is developed by Google and follows the MVC (Model View Controller) pattern. It supports HTML as the template language and enables the developers to create extended HTML tags which will help to represent the application's content more clearly. It is easy to update and receive information from an HTML document. It also helps in writing a proper maintainable architecture which can be tested at a client-side.

## How is it different from Angular 2+?
AngularJS is a JavaScript-based open-source front-end web framework. It doesn't support the features of a server-side programming language, nor dynamic loading of the page.
Angular is a complete rewrite of AngularJS. 
AngularJS was completely based on controllers and scopes whereas, Angular uses component hierarchy as its main architecture!

Angular uses the TypeScript language, which has features like :
Static Typing
Object-Oriented Programming based on classes
Support for reactive programming using RxJS

![image](https://user-images.githubusercontent.com/12488769/148313384-be126011-ea0c-4f8a-8e63-306a36df18a9.png)


## What is scope in AngularJS?
-A $scope is an object that represents the application model for an Angular application.
Each AngularJS application can have only one root scope but can have multiple child scopes.


## What are directives? Mention some of the most commonly used directives in AngularJS application.
- Directives are the markers on DOM element which are used to specify behavior on that DOM element. All AngularJS directives start with the word "ng". There are many in-built directives in AngularJS such as "ng-app", "ng-init", "ng-model", "ng-bind", "ng-repeat" etc.
###	ng-app
The ng-app directive is the most important directive for Angular applications. It is used to locate the beginning of an Angular application for AngularJS HTML compiler. It marks the HTML elements that Angular intends to make the root element of the application. The custom attributes use spinal-cases, whereas the corresponding directives follow the camelCase. If we do not use this directive and try to process other directives, it gives an error.
###	ng-init
The ng-init directive is useful for initializing the data variable's inline statement of an AngularJS application. Therefore, those statements can be used in the specified blocks where we can declare them. A directive ng-init is like a local member of the ng-app directive, and it may be a single value or a group of the values. It directly supports JSON data.
###	ng-model
The ng-model directive binds the values of HTML elements such as input, select, textarea to the application data. It provides two-way binding behavior with the model value. Sometimes, it is also used for databinding.
###	ng-bind
The ng-bind directive is used to bind the model/variable's value to HTML controls of an AngularJS application. It can also be used with HTML tags attributes like: <p/>, <span/> and more but it does not support two-way binding. We can only check the output of the model values.
###	ng-repeat
The ng-repeat directive is used to repeat HTML statements. It works the same as for each loop in C#, Java or PHP on a specific collection item like an array.


## What is injector?
An injector is referred to as a service locator. It is used to receive object instances as defined by the providers, invoke methods, instantiate types, and load modules. Each Angular application consists of a single injector which helps to look upon an instance by its name.

## What is the difference between link and compile in Angular.js?
Link is used for combining the directives with a scope and producing a live view. The link function is used for registering DOM listeners as well as updating the DOM. The linking function is executed as soon as the template is cloned.
There are two types of linking function:
### Pre linking function
Pre-linking functions are executed before the child elements are linked. This method is not considered as a safe way for DOM transformation.
### 	Post linking function
Post-linking functions are executed after the child elements are linked. This method is a safe way for DOM transformation


## What are the styling form that ngModel adds to CSS classes ?
The ng-model directive binds the values of HTML elements such as input, select, textarea to the application data. It provides two-way binding behavior with the model value. Sometimes, it is also used for databinding.

## Explain what is DI (Dependency Injection ) and how an object or function can get a hold of its dependencies?
Dependency Injection- It specifies a design pattern in which components are given their dependencies instead of hard-coding them within the component.

## Benefits of AngularJS?
Some of the main advantages of AngularJS are given below:
o	Allows us to create a single page application.
o	Follows MVC design pattern.
o	Predefined form validations.
o	Supports animations.
o	Open-source.
o	Cross-browser compliant.
o	Supports two-way data binding.
o	Its code is unit testable.


## Explain the MVC design pattern
AngularJS is based on MVC framework, where MVC stands for Model-View-Controller. MVCperforms the following operations:
o	A model is the lowest level of the pattern responsible for maintaining data.
o	A controller is responsible for a view that contains the logic to manipulate that data. It is basically a software code which is used for taking control of the interactions between the Model and View.
o	A view is the HTML which is responsible for displaying the data.
For example, a $scope can be defined as a model, whereas the functions written in angular controller modifies the $scope and HTML displays the value of scope variable.


## What is the DOM?
AngularJS is a JavaScript framework with key features like models, two-way binding, directives, routing, dependency injections, unit tests, etc. On the other hand, JQuery is a JavaScript library used for DOM manipulation with no two-way binding features.
o	Directive- It specifies behavior on the DOM element.
Directives are the markers on DOM element which are used to specify behavior on that DOM element. All AngularJS directives start with the word "ng". There are many in-built directives in AngularJS such as "ng-app", "ng-init", "ng-model", "ng-bind", "ng-repeat" etc.


## How to traverse/manipulate the DOM? Where in AngularJS do we do this?

Compiler is an AngularJS service which traverses the DOM looking for attributes. The compilation process happens in two phases.

Compile: traverse the DOM and collect all of the directives. The result is a linking function.

Link: combine the directives with a scope and produce a live view. Any changes in the scope model are reflected in the view, and any user interactions with the view are reflected in the scope model. This makes the scope model the single source of truth.

Some directives such as ng-repeat clone DOM elements once for each item in a collection. Having a compile and link phase improves performance since the cloned template only needs to be compiled once, and then linked once for each clone instance.
https://docs.angularjs.org/guide/compiler#!

## What is scope?
A $scope is an object that represents the application model for an Angular application.
Each AngularJS application can have only one root scope but can have multiple child scopes. 
Some of the key characteristics of the $scope object are given below:
o	It provides observers to check for all the model changes.
o	It provides the ability to propagate model changes through the application as well as outside the system to other associated components.
o	Scopes can be nested in a way that they can isolate functionality and model properties.
o	It provides an execution environment in which expressions are evaluated.


## What are directives? Can you name some?
AngularJS provides support for creating custom directives for the following type of elements:
o	Element Directive
Element directives are activated when a matching element is encountered.
o	Attribute
Attribute directives are activated when a matching attribute is encountered.
o	CSS
CSS directives are activated when a matching CSS style is encountered.
o	Comment
Comment directives are activated when a matching comment is encountered.

## What is the injector?
An injector is referred to as a service locator. It is used to receive object instances as defined by the providers, invoke methods, instantiate types, and load modules. Each Angular application consists of a single injector which helps to look upon an instance by its name.

## What is the diff betw link and compile?

Angular's HTML compiler allows us to teach the browser, new HTML syntax. It also allows the developer to attach new behavior or attributes to any HTML element known as directives. AngularJS compilation process automatically takes place in the web browser. It does not contain any server-side or pre-compilation procedure.
AngularJS uses <$compiler> service for the compilation process of an Angular HTML page. Its compilation process starts after the HTML page (static DOM) is completely loaded.

It occurs in two phases:
o	Compile
It checks into the entire DOM and collects all of the directives.
o	Link
It connects the directives with a scope and produces a live view.
The concept of compile and link has been added from C language. The code is compiled and then linked.

## What is dependency injection?
Dependency Injection (also called DI) is one of the best features of AngularJS. It is a software design pattern where objects are passed as dependencies rather than hard coding them within the component. It is useful for removing hard-coded dependencies and making dependencies configurable. To retrieve the required elements of the application that need to be configured when the module is loaded, the "config" operation uses Dependency Injection. It allows separating the concerns of different components in an application and provides a way to inject the dependent component into the client component. By using Dependency Injection, we can make components maintainable, reusable, and testable.

## What does ngModel do?
The ng-model directive binds the values of HTML elements such as input, select, textarea to the application data. It provides two-way binding behavior with the model value. Sometimes, it is also used for databinding.

## What are pipes?
A filter is used to format the value of the expression to display the formatted output. AngularJS allows us to write our own filter. Filters can be added to expressions by using the pipe character |, followed by a filter.

## What does ngRepeat do?
The ng-repeat directive is used to repeat HTML statements. It works the same as for each loop in C#, Java or PHP on a specific collection item like an array.

## ngIf?
The ngIf directive removes or recreates a portion of the DOM tree based on an {expression}. If the expression assigned to ngIf evaluates to a false value then the element is removed from the DOM, otherwise a clone of the element is reinserted into the DOM.

ngIf differs from ngShow and ngHide in that ngIf completely removes and recreates the element in the DOM rather than changing its visibility via the display css property. A common case when this difference is significant is when using css selectors that rely on an element's position within the DOM, such as the :first-child or :last-child pseudo-classes.

Note that when an element is removed using ngIf its scope is destroyed and a new scope is created when the element is restored. The scope created within ngIf inherits from its parent scope using prototypal inheritance. An important implication of this is if ngModel is used within ngIf to bind to a javascript primitive defined in the parent scope. In this case any modifications made to the variable within the child scope will override (hide) the value in the parent scope.

Also, ngIf recreates elements using their compiled state. An example of this behavior is if an element's class attribute is directly modified after it's compiled, using something like jQuery's .addClass() method, and the element is later removed. When ngIf recreates the element the added class will be lost because the original compiled state is used to regenerate the element.

Additionally, you can provide animations via the ngAnimate module to animate the enter and leave effects.
https://docs.angularjs.org/api/ng/directive/ngIf

## What is ngclick?
The ngClick directive allows you to specify custom behavior when an element is clicked.

## What are expressions?
Expressions in AngularJS are the code snippets that resolve to a value. AngularJS expressions are placed inside {{expression}}. Expressions are included in the HTML elements.
AngularJS expressions can also contain various valid expressions similar to JavaScript expressions. We can also use the operators between numbers, including strings, literals, objects, and arrays inside the expression {{ }}.

## What is a single page application? How to achieve this in AngularJS?
Routing is one of the main features of the AngularJS framework, which is useful for creating a single page application (also referred to as SPA) with multiple views. It routes the application to different pages without reloading the application. In Angular, the ngRoute module is used to implement Routing. The ngView, $routeProvider, $route, and $routeParams are the different components of the ngRoute module, which help for configuring and mapping URL to views.

## What is data binding? one-way / two-way? give the syntax?
Data Binding is the automatic synchronization of data between model and view.
In AngularJS, it performs the automatic synchronization process between the model and view.

## What is a module?
- It defines an application.

## What is bootstrapping? How do you bootstrap your application?
AngularJS will detect if it has been loaded into the browser more than once and only allow the first loaded script to be bootstrapped and will report a warning to the browser console for each of the subsequent scripts. This prevents strange results in applications, where otherwise multiple instances of AngularJS try to work on the DOM.
https://docs.angularjs.org/api/ng/function/angular.bootstrap#!

## What is a service?
 It stores and shares data across the application.
 
 Services are objects that can be used to store and share data across the application. AngularJS offers many built-in services, and each of them is responsible for a specific task. They are always used with the prefix $ symbol.
Some of the important services used in any AngularJS application are as follows:
o	$http- It is used to make an Ajax call to get the server data.
o	$window- It provides a reference to a DOM object.
o	$Location- It provides a reference to the browser location.
o	$timeout- It provides a reference to the window.set timeout function.
o	$Log- It is used for logging.
o	$sanitize- It is used to avoid script injections and display raw HTML in the page.
o	$Rootscope- It is used for scope hierarchy manipulation.
o	$Route- It is used to display browser-based path in browser's URL.
o	$Filter- It is used for providing filter access.
o	$resource- It is used to work with Restful API.
o	$document- It is used to access the window.Document object.
o	$exceptionHandler- It is used for handling exceptions.
o	$q- It provides a promise object.
o	$cookies- It is used for reading, writing, and deleting the browser's cookies.
o	$parse- It is used to convert an AngularJS expression into a function.
o	$cacheFactory- It is used to evaluate the specified expression when the user changes the input.


## What is a provider?
AngularJS provides the following core components which can be injected into each other as dependencies:
o	Value
o	Factory
o	Service
o	Provider
o	Constant

## How to make an AJAX call in AngularJS?
Angular provides two different APIs to handle Ajax requests. They are
•	$resource
•	$http

## What is interpolation?
Interpolation markup with embedded expressions is used by AngularJS to provide data-binding to text nodes and attribute values.

An example of interpolation is shown below:

<a ng-href="img/{{username}}.jpg">Hello {{username}}!</a>
https://docs.angularjs.org/guide/interpolation#!
