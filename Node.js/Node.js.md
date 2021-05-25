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

The third party module can be downloaded by NPM (Node Package Manager). These type of modules are developed by others and we can use that in our project. Some of the popular third party modules are mongoose, express, angular, and react.

Installing third party modules :-
```
npm install express
npm install mongoose
npm install -g@angular/cli
```

## <span class="header2">NPM</span>

NPM is a package manager for Node.js packages, or modules.

### <span class="header3">Packages & How to download</span>

>A package in Node.js contains all the files you need for a module.

To download a package we have to open the command line interface and tell NPM to download the package that we want.

Eg :-
```
C:\Users\Gaurav>npm install upper-case
```
The NPM will then create a folder named "node_modules", where the package will be placed.

### <span class="header3">Using Packages</span>

Once the package is installed, it is ready to use. We will include the "package_name" the same way we include any other module:

```js
var uc = require('upper-case');
```

## <span class="header2">Node.js Process Model</span>

Node applications are highly scalable this is because of non-blocking and asynchronous nature of Node.

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