# <span class="header">Arrays, Object & Function</span>

## <span class="header2">Arrays</span>

<span class="highlight">An array is a special variable that can store multiple values at a time</span>. However, another thing to know is that in Javascript Arrays are considered as an object. The `typeof` operator will return 'object' as a result for arrays.

Few distinct Features that array provide are :-
* It provides us index which uses numbers to access its 'elements'
* Since arrays are special kind of object it can store different types of variables in the same array.
<br>eg :-
```js
let Colors = ['red','green','1','2'];  // Perfectly valid array
```
* Another feature of JS arrays are their built-in properties and methods

### <span class="header3">Array Properties</span>

| Property | Description |
| ------- | ----------- |
| constructor | Returns the function that created the Array object's prototype |
| length | Returns the number of elements in an array |
| prototype | Allows us to add new properties and method to an array object |
<br>

### <span class="header3">Array Methods</span>

| Methods | Description |
| ------- | ----------- |
| concat | Returns a new array object that contains two or more merged arrays |
| filter | Creates new array with all elements that pass the test in the testing function |
| find | Returns the value of the first element that pass the test in testing function |
| forEach | Calls a function once for each element |
| indexof | Searches the array for an element and return its first index |
| lastIndexOf | Searches the array for an element, starting at the end and returns its last index | 
| isArray | To test if the variable is an array | 
| map | Calls a specified function for every array element and returns a new array | 
| pop | Removes last element from an array | 
| push | Adds a new element to an array | 
| reverse | Reverses the elements of array |
| splice | Adds/Removes element to/from given array |
| slice  | Returns a new array containing the copy of the part of selected array |  
| shift | Removes first element from an array and "shifts" all other elements to lower index |
| unshift | Adds a new element to an array at the start and "unshifts" other elements to higher index |
| toString | Converts an array into string form |
<br>


## <span class="header2">Object</span>

In JS, almost everything is an object. Objects are non-primitive data type that can be used to store data in key-value pair.

Objects can be created in JS using three ways :-
```js
// Using Object Literal
var person = {
  firstName : "Gaurav",
  lastName : "Dhuri",
  age: 23
}

// Using 'new' keyword
var person = new Object();
person.firstName = "Gaurav";
person.lastName = "Dhuri";
person.age = "23";

// Using Object Constructor
function Person(fname, lname, age){
  this.firstName = fname;
  this.lastName = lname;
  this.age = age;
}
```
### <span class="header3">Object Properties</span>

Properties in object are nothing but the association between names and values. In JS, we can add, delete and modify the properties.

Syntax for accessing prototype :-
```js
objectName.property

// or

objectName['property']

// or

objectName[expression]
```

### <span class="header3">Object Method</span>

| Methods | Description |
| ------- | ----------- |
| assign | Used to copy properties from source object to target object |
| create | Used to create a new object with specified prototype object and properties |
| keys | Returns an array of given object's own property name |
| values | Returns an array of values |

## <span class="header2">Understanding Arrays & Objects</span>

### <span class="header3">Difference between Arrays and Object</span>

So in the above Section, we have understood Arrays and Objects, both are basically different ways to organize and store data. However each of them have their merits and de-merits. Using a wrong data type to store data can cause mess in code and make it impossiblle to review our code. To avoid this we need to understand, when is it best to use an object vs when is it best to use an array. 

To understand that, think of Arrays as Books and think of Objects as Newspapers.

<table>
<tr>
<th>Arrays</th>
<th>Objects</th>
</tr>
<tr>
<td>Books consist of chapters. Each Chapter is associated with a number. If the reader wants to read a particular chapter he can use the number associated with it.</td>
<td>Newspaper consist of Sections. Each Section has a particular Name and some news associated to it. The reader can just flip immediately to the section and read the appropriate context.</td>
</tr>
<tr>
<td><img src="../assests/Books.jpg"></td>
<td><img src="../assests/Newspaper.jpg"></td>
</tr>
<tr>
<td class="highlight">We use arrays when order is the most important factor for organizing the information.</td>
<td class="highlight">We use Objects when we want to organize information based on data labels.</td>
</tr>
<tr>
<td>

```js
var books = ['Chapter 1','Chapter 2','Chapter 3','Chapter 4', 'Chapter 5'];
```

</td>
<td>

```js
var newspaper = {
  sports : 'Cricket is Awesome',
  business : 'Crypto currency crashed',
  movies : 'Venom 2',
}
```

</td>
</tr>
</table>

### <span class="header3">Combining Arrays and Objects</span>

So far, we know that we can store strings, numbers, booleans, etc in Arrays and Objects. Additionally we can also store :-
1. Arrays withing objects
2. Objects within arrays
3. Arrays within arrays
4. Object within objects

If we use the above example of book and newspaper, we can better understand it.

Eg :-
```js
// Book - object within an array
var book = [
  {name : 'Chapter 1', pagecount : 10,},
  {name : 'Chapter 2', pagecount : 20,},
  {name : 'Chapter 3', pagecount : 30,},
  {name : 'Chapter 4', pagecount : 40,},
]

// Newspaper - array within an object
var newspaper = {
  sports : 'Cricket is Awesome',
  sportsWriter : ['Sachin','Dhoni','Virat'],
  business : 'Crypto currency crashed',
  businessWriter : ['Elon','Andre','Cathie']
  movies : 'Venom 2', 
  movieWriter : ['Anthony Russo','Joseph Russo']
}
```

Here, we can see that for the array we can not only have the Chapters arranged in order but we can also name specific property like page of the chapter. And for the newspaper we still have the data based on Section and each section has an order of the writer.

## <span class="header2">Functions</span>

<span class="highlight">A function is a block of code designed to perform a particular task</span>. The main purpose behind creating/using a function is that we can reuse the code as many times as we want, this helps use save time and also helps us make our progams compact.

Syntax of a function is :

```js
 function name(parameter1, parameter2, parameter3){
   // code to be executed
 }
```
Think of function like a food recipe.

Eg :- Making a sandwich. The ingredients will be the parameters and the code will be the procedure we use on the ingredients and this procedure when performed should result us with a output which is a sandwich. 
```js
makeSandwich(onion 🧅, bread 🍞, tomato 🍅, cheese 🧀){
 let sandwich = 🧅 + 🍞 + 🍅 + 🧀;
 return sandwich 🥪;
}
```

Also, if<span class="highlight"> a function is associated with an object it is often called as method</span>.

### <span class="header3">Arrow Functions</span>

Arrow Functions are also called as 'fat arrow function'. In JS, arrow function are just an alternate way to write a shorter syntax compared to normal function expression. 

<table>
<tr>
<td>Normal function expression</td>
<td>Arrow function expression</td>
<td>Output</td>
</tr>
<tr>
<td>

```js
function hello(){
  return 'Hello World';
}
```

</td>
<td>

```js
let hello = () => 'Hellor World';
```

</td>
<td>Output will be the same</td>
</tr>
<tr>
<td>

```js
function hello(val){
  return 'Hello' + val;
}
```

</td>
<td>

```js
let hello = val => 'Hello' + val;
```

</td>
<td>Output will be the same</td>
</tr>
<tr>
<td>

```js
function sum(a,b){
  return a + b;
}
```

</td>
<td>

```js
let sum = (a,b) => a + b;
```

</td>
<td>Output will be the same</td>
</tr>
</table>

As we can see arrow function expression is just a more concise and easier way of using arrow function but that's not what makes arrow function really great. <span class="highlight">What really makes arrow function great is that they redefines `this` keyword inside of them as opposed to normal function</span> .

Eg :-
<table>
<tr>
<td></td>
<td>Normal function expression</td>
<td>Arrow function expression</td>
</tr>
<tr>
<td>Function</td>
<td>

```js
class Person{
  constructor(name){
    this.name = name
  }
  printNameFunction(){
    setTimeout(function() {
      console.log('Function: ' + this.name)
    }, 100)
  }
}

let person = new Person('Gaurav')
person.printNameFunction()
```

</td>
<td>

```js
class Person{
  constructor(name){
    this.name = name
  }
  printNameArrow(){
    setTimeout(() => {
      console.log('Arrow: ' + this.name)
    }, 100)
  }
}

let person = new Person('Gaurav')
person.printNameArrow()
```

</td>
<tr>
<td>Output</td>
<td>Function: </td>
<td>Arrow: Gaurav</td>
</tr>
<tr>
<td>Reason</td>
<td>In regular functions, <code>this</code> represents the object that called the function. Since, here <code>printNameFunction()</code> was called in global scope we get <code>this.name</code> empty</td>
<td>In arrow functions, <code>this</code> always represents the object that defined the arrow function. This is why, when <code>printNameArrow()</code> was called we get <code>this.name</code> as Gaurav</td>
</tr>
</table>
<br>

### <span class="header3">IIFE</span>

IIFE stands for 'Immediately Invoked Function Expression'.
>It is a design pattern which is also known as a Self-Executing Anonymous Function.

IIFE is divided into two parts :-
1. If we write function within Grouping Operator it will be a anonymous function. This ensures data privacy and makes it so that the function cannot be accessed from outside.
2. As soon as the function is defined within the Grouping Operator it will run.

Below are some ways we can write IIFE :-
```js
(function(){
  console.log("My Name is Gaurav");
})();
// Output will be- My Name is Gaurav

(myName = function(name = "Gaurav Dhuri"){
  console.log("My Name is" + name);
})();
// Output will be- My Name is Gaurav Dhuri

myName(Dhuri);  // Inline Parameter
// Output will be- My Name is Dhuri
```
<span class="highlight">One of few reasons IIFE is used because it doesnt let Global variables get polluted and this helps us avoid variable conflicts</span>, however with the addition of block scopes like `const` and `let` IIFE isnt used as much anymore. 

### <span class="header3">Constructor Function</span>

Constructor function is nothing but one of the three way of creating an objectConstructor functions helps us create multiple object of same type. We need to use the `new` keyword when we call the constructor function.

Syntax of Constructor function :-
```js
// constructor function
function Person(person_fname, person_lname){
  this.fname = person_fname,
  this.lname = person_lname,
}

// creating objects
const person1 = new Person('Gaurav','Dhuri');
const person2 = new Person('Yash','Chaurasia');

// access properties
console.log(person1.fname); // Gaurav
console.log(person2.fname); // Yash
```



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