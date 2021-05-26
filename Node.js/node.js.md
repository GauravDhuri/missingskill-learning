# <span class="header">Node.js</span>

<span class="highlight">Node.js is one of the most popular real-time web applications that allow two way communication</span>, where both client and server can initiate communication, allowing them both to exchange data freely.

>Node.js is an open source server environment. 

Node.js allows us to run JS on the server.

## <span class="header2"> Node.js Modules</span>

<span class="highlight">Modules are same as JavaScript libraries</span>. A set of function we want to include in our application.

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

The best way to understand Node.js Model is to think of it as a Restaurant. 

- Customers come to counter and give order to waiter
- When too many customers arrive, they wait in a line for their turn
- Once the customer is served, the waiter passes the order to manager libuv, who assigns order to chef.
- Chefs are worker threads.
-  Once waiter passes the order to manager, he doesn't wait for order to be prepared instead, waiter takes order of next customer
-  When the order is read waiter calls out the name and serves customer.

<img src="../assests/Node.jsmodel.jpg" width="800">

The waiter here is a single thread that handles all the request. <span class="highlight">Also since the waiter doesn't wait for the order to be prepared and goes on asking other customer order, we can say it is a Non-Blocking architecture </span>.

This Model is what makes Node.js so popular. As this model increases the performance and scalability. 

<br>
<br>
<br>
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
.list{
  color: #FF8080
}
</style>
