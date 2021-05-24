# <span class="header">Node.js</span>

Node.js is one of the most popular real-time web applications that allow two way communication, where both client and server can initiate communication, allowing them both to exchange data freely.

>Node.js is an open source server enviornment. 

Node.js allows us to run JS on the server.

## <span class="header2"> Node.js Modules</span>

Modules are same as JavaScript libraries. A set of function we want to include in our application.

### <span class="header3">Core Modules</span>

Core modules include bare minimum functionalities of Node.js. These core modules are compiled into its binary distribution and load automatically when Node.js process starts. Although we need to import these modules in order to use them.

| Modules | Description |
| ------- | ----------- |
| http | To make Node.js act as an HTTP server |
| url | To parse URL strings |
| querystring | To handle URL query strings |
| path | To handle file paths |
| fs | To handle the file system |
| util | To access utility functions |

<br>
Loading Syntax for Core Module :-

```js
var module = require('module_name');

// Eg:-
var http = require('http');
var server = http.createServer(function(req, res){
  // some code
});
server.listen(5000);
```

### <span class="header3">Local Module</span>

Local modules are modules created locally in our Node.js application. These modules include different functionalities of our application in separate files and folders.

```js
var log = {
  info : function (info) { 
    console.log('Info: ' + info);
  },
  warning:function (warning) { 
    console.log('Warning: ' + warning);
  },
  error:function (error) {
    console.log('Error: ' + error);
  }
};

module.exports = log
```

Here we have created an object with three functions - info(), warning(), and error(). At the end we have assigned this object to `module.exports`. `module.export` is a special object which is included in ever JS file in Node.js by default. It is used to expose a function, object or variable as a module in Node.js

Loading a Local Module 

```js
var myLogModule = require('./Log.js');
myLogModule.info('Node.js started');
```
### <span class="header3">Third Party Modules</span>

## <span class="header2">Node.js Process Model</span>

## <span class="header2">Node Package Manager</span>

## <span class="header2">Express.js</span>

<style>
.highlight{
  color: #75FF33
}
.header3{
  color: #E6D100
}
.header{
  color: #EE82EE
}
.header2{
  color: #00FFFF
}
.imp{
  color: #FF8080
}
</style>