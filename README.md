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


# ***Service Portal***
## What is diff betw Service Portal and CMS system?
Service Portal is a compelling alternative to the Content Management System (CMS) with a refined user experience.
 It does not duplicate CMS or platform UI functionality. Users who have sophisticated experiences delivered through CMS may need to invest time into transitioning to Service Portal, especially if the CMS implementation includes complex and customized Service Catalog forms.
Service Portal compatibility with existing CMS sites
ServiceNow continues to support CMS in current and upcoming releases. If you have existing CMS sites and activate Service Portal on your instance, your CMS sites will continue to work, as CMS and Service Portal are separate applications.
Differences between Service Portal and CMS
Service Portal is an alternative to CMS based on more modern technologies. Major differences include:
Underlying technology
CMS uses Jelly, which is not a widely used technology. 
Service Portal instead uses AngularJS, server-side JavaScript, HTML, and CSS. Any scripts that use Jelly do not work in Service Portal. Building widgets in Service Portal requires knowledge of AngularJS.
Visual layer
CMS uses iFrames which can be difficult to work with, limited in terms of styling, and susceptible to upgrade issues.
 Alternatively, Service Portal is a self-contained application that accesses data from other tables on the platform. This enables fine-tuned control over style and responsive design.
Mobile first
Unlike CMS, Service Portal is optimized for a mobile environment. For this reason, the following apply to the Service Portal environment:
•	Any scripts used in Service Portal can only use APIs supported in a mobile environment. For example, some APIs used in your Service Catalog client scripts may not be supported. For a list of supported APIs, see Service Portal and client scripts.
•	Service Portal forms support a maximum of two-columns. As a result, any highly customized Service Catalog forms, such as catalog items and record producers that use containers and variable sets, must be simplified to work in a two-column layout.
If transitioning to Service Portal, review the following resource: Mobile client GlideForm (g form) scripting and migration.

## Can we domain separate Service Portal pages?
NO.

## What are the basic components of a service portal?
You should have a basic understanding of all the following components that make up a portal:
•	Themes: Themes define the look and feel of the whole portal, but can be overridden by other style configurations.
•	Pages: Pages control where and how you store portal content. Pages do not have a defined relationship to portal records, they simply exist.
•	Widgets: Components in Service Portal are called widgets. You can use HTML templates, CSS, client scripts, server scripts, and any JavaScript dependencies to define what a widget does. From an AngularJS standpoint, widgets are essentially a superset of an Angular directive.
•	Most of the data in Service Portal is managed in different locations throughout the system.
For example, if you are building a knowledge portal, the data exists in Service Portal, but the knowledge articles are authored and managed in the Knowledge application. The same is true for any other type of content you plan to leverage. Take time to understand which tables contain and control the data you are working with in Service Portal.

## What is a widget and what are its components?
Widgets include both mandatory and optional components.
HTML Template
The widget's HTML accepts and displays data.
•	Renders the dynamic view a user sees in the browser using information from the model and controller
•	Binds client script variables to markup
•	Gathers data from user inputs like input text, radio buttons, and check boxes
HTML is mandatory.
Client Script
The widget's Client Script defines the AngularJS controller.
•	Service Portal maps server data from JavaScript and JSON objects to client objects
•	Processes data for rendering
•	Passes data to the HTML template
•	Passes user input and data to the server for processing
A Client Script is mandatory.
Server Script
The widget's Server Script works with record data, web services, and any other data available in ServiceNow server-side scripts.
•	Sets the initial widget state
•	Sends data to the widget's Client Script using the data object
•	Runs server-side queries
A Server Script is mandatory.
Link Function
The Link Function uses AngularJS to directly manipulate the DOM.
A Link Function is optional.
Option Schema
The Option Schema allows a Service Portal Admin (sp_admin role) to configure a widget.
•	Specifies widget parameters
•	Allows admin users to define instance options for a widget instance
•	Makes widgets flexible and reusable
An Option Schema is optional.
Angular Providers
An Angular Provider:
•	Keeps widgets in sync when changing records or filters
•	Shares context between widgets
•	Maintains and persists state
•	Creates reusable behaviors and UI components then injects them into multiple widgets
Angular Providers are optional.

## What are pages?
Use pages to organize content, ensure responsive mobile optimization, and design meaningful portal user experiences for your customers. A page houses containers and rows, which then contain widgets. By manipulating the layout of the page, and the widgets within it, you can construct your desired user experience.
•	Pages are referenced using the page ID.
•	Pages can be referenced in more than one portal.
•	Use base system pages as templates.
Containers
Containers are markup artifacts that are put on a page to contain the layouts that house the widgets.
You can view containers and how they make up a page in the Service Portal Designer (Service Portal > Service Portal Configuration > Designer). 

## How to secure service portal page?
Control user access to a portal.
Control who accesses your portal and what they can see in the following ways:
•	Authentication: Configure login and single sign on for users
•	Limit page access by role: Use roles to limit the users who can see a page.
•	Public pages: Use the public check box on a page record to make the page publicly accessible.
Note: A number of portal pages that are installed by default are marked public. Filter your list of Service Portal pages for Public [is] true to identify these pages. Setting the Public value to false will prevent these pages from being publicly available.
•	User criteria: For a more advanced way of limiting user access, create and apply user criteria to pages, widgets, widgets instances, and search sources.
•	Multifactor authentication: If an instance is configured to require multifactor authentication, users are automatically directed to set up multifactor authentication upon initial login. For setup instructions, see Setup multi-factor authentication upon initial login. If multifactor authentication is optional, users can still enable or disable authentication from their user profile. For setup instructions, see Setup multi-factor authentication on your user profile.
Single sign-on, logins, and URL redirects
Service Portal uses a combination of system properties and script includes to determine how the system handles URL redirects for users logging in to the portal.
Configure page security by role
Set up pages to be public or filter them by role.
Configure widget security
Configure widget security to ensure that your widget is being accessed only by the intended audience.
User criteria for Service Portal
User criteria enables you to allow access to users based on role, department, group, location, or company. Administrators can control access to pages, widgets, widget instances, announcements, and search sources in a portal by creating and applying user criteria.
Enable e-signature for Service Portal
You can configure e-signature in Service Portal to require re-authentication from approving users.
Enable external user self-registration for Service Portal
Enable external users to register to a ServiceNow app through Service Portal.
Register your PIV/CAC card for Service Portal login
Register your Personal Identity Verification (PIV) or Common Access Card (CAC) card so that you can log in to your organization's portal without entering a password.

## What are features not supported in Service Portal?
Domain separation
https://docs.servicenow.com/bundle/rome-servicenow-platform/page/script/client-scripts/reference/r_MobilePlatformMigrationImpacts.html

# ***JAVASCRIPT***
## What is JavaScript?
JavaScript is a scripting language that enables you to create dynamically updating content, control multimedia, animate images, and pretty much everything else. 
With the HTML DOM, JavaScript can access and change all the elements of an HTML document.

## What is the DOM? How to manipulate the DOM?
The HTML DOM (Document Object Model)
When a web page is loaded, the browser creates a Document Object Model of the page.
The HTML DOM model is constructed as a tree of Objects:

With the object model, JavaScript gets all the power it needs to create dynamic HTML:
•	JavaScript can change all the HTML elements in the page
•	JavaScript can change all the HTML attributes in the page
•	JavaScript can change all the CSS styles in the page
•	JavaScript can remove existing HTML elements and attributes
•	JavaScript can add new HTML elements and attributes
•	JavaScript can react to all existing HTML events in the page
•	JavaScript can create new HTML events in the page
________________________________________________________________________________


The DOM is a W3C (World Wide Web Consortium) standard.
The DOM defines a standard for accessing documents:
"The W3C Document Object Model (DOM) is a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document."
The W3C DOM standard is separated into 3 different parts:
•	Core DOM - standard model for all document types
•	XML DOM - standard model for XML documents
•	HTML DOM - standard model for HTML documents
________________________________________
What is the HTML DOM?
The HTML DOM is a standard object model and programming interface for HTML. It defines:
•	The HTML elements as objects
•	The properties of all HTML elements
•	The methods to access all HTML elements
•	The events for all HTML elements
In other words: The HTML DOM is a standard for how to get, change, add, or delete HTML elements.

HTML DOM methods are actions you can perform (on HTML Elements).
HTML DOM properties are values (of HTML Elements) that you can set or change.
The getElementById Method
The most common way to access an HTML element is to use the id of the element.
In the example above the getElementById method used id="demo" to find the element.
________________________________________
The innerHTML Property
The easiest way to get the content of an element is by using the innerHTML property.
The innerHTML property is useful for getting or replacing the content of HTML elements.
The innerHTML property can be used to get or change any HTML element, including <html> and <body>.


## What are the JavaScript data types?
## What are the data types in JS?
The set of types in the JavaScript language consists of primitive values and objects.
•	Primitive values (immutable datum represented directly at the lowest level of the language)
o	Boolean type
o	Null type
o	Undefined type
o	Number type
o	BigInt type
o	String type
o	Symbol type
•	Objects (collections of properties)


## What is the use of isNaN function?
In JavaScript NaN is short for "Not-a-Number".
The isNaN() method returns true if a value is NaN.
The isNaN() method converts the value to a number before testing it.

## What is an undefined value in JavaScript?
## What are undeclared and undefined variables?
Undeclared − It occurs when a variable which hasn’t been declared using var, let or const is being tried to access.

Undefined − It occurs when a variable has been declared using var, let or const but isn’t given a value.


## How can you add new elements dynamically?
The document.createElement() creates a new HTML element.
The document.createTextNode() creates a text node.
The appendChild() method appends dynamic element to body or target element.
The document.querySelector() allows to select desired element using any valid selector.

## How can you use functions / different types of functions?
Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.

## What is hoisting?
JavaScript Hoisting refers to the process whereby the interpreter appears to move the declaration of functions, variables or classes to the top of their scope, prior to execution of the code.
Hoisting allows functions to be safely used in code before they are declared.
Variable and class declarations are also hoisted, so they too can be referenced before they are declared. Note that doing so can lead to unexpected errors, and is not generally recommended.

## What are the new features of ES6?
Let
Const
For…of
Template literals
Default values for function parameters
Arrow functions
Ciasses
Modules
Rest parameter
Spread operator
Destructuring assignment


## What are the scopes in JS?
Before ES6 (2015), JavaScript had only Global Scope and Function Scope.
ES6 introduced two important new JavaScript keywords: 
let and const.
These two keywords provide Block Scope in JavaScript.
Variables declared inside a { } block cannot be accessed from outside the block:

Variables declared with the var keyword can NOT have block scope.
Variables declared inside a { } block can be accessed from outside the block.
Local Scope
Variables declared within a JavaScript function, become LOCAL to the function.
Local variables have Function Scope:
They can only be accessed from within the function.
JavaScript has function scope: Each function creates a new scope.
Variables defined inside a function are not accessible (visible) from outside the function.
Variables declared with var, let and const are quite similar when declared inside a function.
They all have Function Scope:


## What are global variables? How are these variable declared and what are the problems associated with using them?


Global JavaScript Variables
A variable declared outside a function, becomes GLOBAL.
A global variable has Global Scope:
All scripts and functions on a web page can access it. 

Global Scope
Variables declared Globally (outside any function) have Global Scope.
Global variables can be accessed from anywhere in a JavaScript program.
Variables declared with var, let and const are quite similar when declared outside a block.
They all have Global Scope:

## Explain the working of timers in JavaScript? Also discuss the drawbacks of using the timer, if any?
Timers are used to execute a piece of code at a set time or also to repeat the code in a given interval of time. This is done by using the functions setTimeout, setInterval and clearInterval.
The setTimeout(function, delay) function is used to start a timer that calls a particular function after the mentioned delay. The setInterval(function, delay) function is used to repeatedly execute the given function in the mentioned delay and only halts when cancelled. The clearInterval(id) function instructs the timer to stop.
Timers are operated within a single thread, and thus events might queue up, waiting to be executed.
The setTimeout() and setInterval() are both methods of the HTML DOM Window object.

## What is === operator? Compare with == operator?
=== equal value and type
== equal value / may not be same type

## What is type coercion?
Type coercion is the process of converting value from one type to another (such as string to number, object to boolean, and so on). Any type, be it primitive or an object, is a valid subject for type coercion. To recall, primitives are: number, string, boolean, null, undefined + Symbol (added in ES6).

## Explain how can you submit a form using JavaScript?

Set the name attribute of your form to "theForm" 
JavaScript provides the form object that contains the submit() method. Use the ‘id’ of the form to get the form object.
For example, if the name of your form is ‘myform’, the JavaScript code for the submit call is:
document.forms["myform"].submit();
But, how to identify a form? Give an id attribute in the form tag
Here is the code to submit a form when a hyperlink is clicked:
<form name="myform" action="handle-data.php">
Search: <input type='text' name='query' />
<a href="javascript: submitform()">Search</a>
</form>
<script type="text/javascript">
function submitform()
{
  document.myform.submit();
}
</script>




## What are some common JavaScript events?
An HTML event can be something the browser does, or something a user does.
Here are some examples of HTML events:
•	An HTML web page has finished loading
•	An HTML input field was changed
•	An HTML button was clicked


## Can we add more than one "document.ready()" function in a page?
You can have multiple ones, but it's not always the neatest thing to do. Try not to overuse them, as it will seriously affect readability. Other than that , it's perfectly legal. See the below:
http://www.learningjquery.com/2006/09/multiple-document-ready


## What are the four parameters used for jQuery.ajax method?
The ajax() method is used to perform an AJAX (asynchronous HTTP) request.
All jQuery AJAX methods use the ajax() method. This method is mostly used for requests where the other methods cannot be used.
Parameter values
This method can have several name/value pairs for the AJAX requests. The names and values are defined in the following table.
Async
beforeSend
cache
complete
url
...

## What is Ajax?
AJAX = Asynchronous JavaScript And XML.
AJAX is not a programming language.
AJAX just uses a combination of:
•	A browser built-in XMLHttpRequest object (to request data from a web server)
•	JavaScript and HTML DOM (to display or use the data)


## What are the advantages of Ajax?
•	Allows applications to render without data and fill data as the application gets it from the server.
•	Gives platform independence to application developers
•	Faster page renders
•	More responsive applications
•	No rerenders of whole pages are needed to update only a single area.


•	Update a web page without reloading the page
•	Request data from a server - after the page has loaded
•	Receive data from a server - after the page has loaded
•	Send data to a server - in the background


## What are the disadvantages of Ajax?
•	Any user whose browser does not support JavaScript or XMLHttpRequest, or has this functionality disabled, will not be able to properly use pages that depend on Ajax.
•	Multiple server requests need more data consumed at the client-side.
•	Failure of any one request can fail the load of the whole page.
•	Browsers with JS disabled will not be able to use pages using ajax.


## What are all the controls of Ajax?

The keystone of AJAX is the XMLHttpRequest object.

The important properties of the XMLHttpRequest object are given below.
o	onReadyStateChange - It is called whenever readystate attribute changes.
o	readyState - It represents the state of the request.
o	responseText - It returns response as text.
o	responseXML - It returns response as XML.
o	status - It returns the status number of a request.
o	statusText - It returns the details of status.

 important methods of XMLHttpRequest?
o	abort() - It is used to cancel the current request.
o	getAllResponseHeaders() - It returns the header details.
o	getResponseHeader() - It returns the specific header details.
o	open() - It is used to open the request.
o	send() - It is used to send the request.
o	setRequestHeader() - It adds request header.


## What are all the technologies (ie. think: protocol) used by Ajax?
HTML/XHTML and CSS - These technologies are used for displaying content and style.
DOM - It is used for dynamic display and interaction with data.
XML - It is used for carrying data to and from server
XMLHttpRequest - It is used for asynchronous communication between client and server.
JavaScript - It is used mainly for client-side validation

## What is JSON?
Javascript object notation
 it is language and platform independent.
 is a syntax for exchanging and storing the data. It is language independent data format and an open standard file format. It is mainly based on the Javascript
•	Data is in name/value pairs
•	Data is separated by comma
•	Curly brackets hold objects
•	Square bracket holds arrays

# ***ANGULARJS***
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
