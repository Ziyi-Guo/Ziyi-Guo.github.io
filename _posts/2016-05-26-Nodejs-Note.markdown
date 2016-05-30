---
sytle: post
title: Note on Node.js
categories: Dev
---
Node.js is a framework allows you to build net applications using js on server-side

Block and Non-Blocking code, former is one step and another, while the later is process some stuffs at the same time, and set callback if one is done. So it do things simultaneously.

Why Js,
> Js has certain characteristics that make it very different than other dynamic langs, namely that it has no concept of threads. Its model of concurrency is completely based around events

DOM - Document, Object, Model

Custom event emitters, we can define our own events emitter,like
	var EventEmitter = require('events').EventEmitter;
	var logger = new EventEmitter();
	logger.on("some",function(msg){
		console.log("SOME"+msg);
	};
To trigger the event emitter above, use 
	logger.emit('some',"data");

Some events: 'error','warn','info'

Stream, request as a readable stream, response as a writable stream
pipe, handle all the event listening and chunking writing,
all sources of readable stream can be pipe into all sorts of writable stream.

Modules, write some methods and using 'module.exports = methods' to export them as modules,
can do as well as 'module.mName = function(){}'. While the first one can set only one method to be public and 2nd one can do more. But, can do this **exports.x = x, exports.y = y**, NPM stands for node package manager.
Locally installed, need require, globally, no need (-g)

Json file for config, to specify name,version, dependencies(modules needed, name and version). 
Use npm install if dev with dependecies or on other's proj

Semantic versioning, say 1.9.7 major,minor,patch, major ones might change API. 
Can use "~" charactor before the version to set it as up-to-date as possible.

parse var into express get, app.get('/path/:var',function(req,res){ var x = req.params.varName; });

Express thingy, ***come back later***

Socket.io, abstracts websockets with fallbacks,
define like this, var io = require('socket.io')(server); and then it'll listen to the server.
Socket.io has a broadcast property, which will broadcast msg to all the user

