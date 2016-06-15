---
style: post
title: AngularJS Note
categories: Mean Dev
---
After two series of courses on Angular.Js in CodeSchool, I'm quite stressed now.
I think I totally fucked up the second one. 

For the first one, basic things, easy to grab and the interactive way of showing the view right after my modification on code helps a lot.
But then came the second one,'Staying Sharp with Angular.js', emmm, hard.

Now, I'll try to review what I got from the courses, in a unordered list.

+ Directive, HTML annotation which triggers JS behaviors

+ AngularJS, client-side JS Framework for adding interactivity to HTML.

+ Module, where to write angular application.

+ define a js file with module, include it in HTML with <script src='xxx'></script>, and use it in the html tag like <html ng-app="app-name">

+ expression, {{variable}} to get value of var in html

+ Controller, where to define app's behavior by defining functions and values. app.controller("CtrlName",function(){}); , In HTML, ng-controller tag, <div ng-controller="CtrlName as alias">

+ BuiltIn directive, say:
	ng-show,
 	ng-hide,
	ng-if,
	ng-repeat, 
	ng-resouce(for resource display with expression in),
	ng-click (could use value or funtion in ) and **2-way data Binding**,
	ng-init="var = value" to initialize the var,
	ng-class as <sth ng-class="{ className : expression or function }">,
	ng-model binds form element value to property,
	ng-submit call a function then form is submit,
 *novalidate* to turn off HTML validation & *required* to choose which field is required ( us <ng-submit="form.$valid && functionToDealData()"> ),
	ng-href to do the href thingy in angular,
	
	directive set replace as true will set the outermost tag for element to be null

+ Filters, {{ data | filter:option }},say, date, currency, upper/lowercase,etc
	and a special filter filter, like {{ data | filter:{fild1:{field2:value}} }}, if we want to search across all the scope not just some fields, use dollar sign $

+ Dependency, like libraries in other languages. Reference the dependent lib with a blanket([]) and inject it inside the function.
Like, angular.module("mName").controller("thisController",['ngSth',function(ngSth,xx){ //functionhere  }]); 
Now I got $http and ngRoute libs, $http for http requests, and ngRoute for routing around.

+ Route, using ngRoute,
two specific function here, when and otherwise,
	
	angular.module('myModule',['ngRoute']).config(function($routeProvider){ 
	$routeProvider.when("/",{templateUrl:"/way/to/url.html"});
	$routeProvider.otherwise({redirectTo:"/redirect/url"})}; });

>
> Four steps to route with Angular
> 1. Using ng-view in html to set the href
> 2. Loading ngRoute lib src in html file like <script src="">
> 3. Import ngRoute Module 
> 4. Define route for specific route.

+ $scope thiny, which helps to get rid of the alias, No more alias in html and no more in Directive,
scope:{} in directive helps to define an isolate scope.It's a flexible way to access data 

+ Link, a great way to manipulate the DOM, it takes a function

	link:function(scope,element,attrs){ };

+ Services, Factory and Provider, define reusable functions throughout the application.

+ Controller/Link when to use, controller is for you when the function inside are shared with other directives, and remember to use 'require' field.

Some Practice Thingy Learnt:
===

1. Inject the dependency in your module js file, and dont do it else. 
As everytime you do it elsewhere, it's gonna overwrite the injections
