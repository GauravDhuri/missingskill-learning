# <span class="header">ES6</span>

ES6 is also known as ECMAScript 6. ES6 version brought lots of new syntax and new features that makes our code more mordern and more readable. Essentially it helps us write less code and do more.

## <span class="header2">Let and Const</span>

Before ES6 was released, developers used `var` as default way to decalre variables. However, `var` had certain problems that could produce unexpected outcomes. Mainly, if `var` was declared outside a function it had global scope and it meant that it could be used by whole window.

Also, biggest problem of `var` variables was that they could be re-declared and updated.
```js
var greet = "hey hi";
var greet = "Hello";
console.log(greet); // Hello
```

This could create alot of mess. So, it was a relief when ES6 released `let` and `const` as alternative ways to declare variables.

### <span class="header3">Let</span>

`let` is a block scoped variable. It solved the issuses that were caused by `var`. let variables can be updated buy cannot be re-declared.

```js
// updating let variable
let greet = "hi";
greet = "hello";

// re-declaring let variable
let greet = "hi";
let greet = "hello"; // will throw error
```

### <span class="header3">Const</span>

`const` is used for variables that should maintain constant values. Similar to `let`, `const` is block scoped too. However, unlike `let`, `const` variables cannot be re-declared or updated.

```js
const greet = "hi";
greet = "hello"; // will throw error
```

## <span class="header2">Destructuring</span>

Destructuring in JS is a method that helps us upack values from arrays and properties from objects into variables. 

Why is destructuring needed ? Many-a-times it can happen that arrays can be complexly nested which makes information access very tedious epecially when we might not need the entire informatioin but rather only a part of information. Here Destructuring can help us map elements that we are interested in while ignoring the other elements.

```js
// Array destructuring
var name = ["Gaurav", "Yash", "Aniket"];

var [first, second, third] = name;

console.log(first); // Gaurav
console.log(second); // Yash

// Object destructuring
var user = {
    id : 1,
    name : "Gaurav",
    age : 23,
};

var {id, name} = user;

console.log(id); //  1
console.log(name); // Gaurav
```
### <span class="header3">Rest</span>

In ES6 a new operator(...) was added that can be used in destructuring. If the operator appears on the left-hand side in destructuring then it is called as Rest parameter. Rest is used to map the remaining elements that were not intrested in by itself.

Eg :-
```js
var games = ["CS:GO", "Valorant", "Dota 2", "League of Legends", "Rainbow Six Seige"];
var [first, ,third, ...others] = games;

console.log(first); // CS:GO
console.log(third); // Dota 2
console.log(others); //["Valorant","League of Legends","Rainbow Six Seige"]
```

### <span class="header3">Spread</span>

When the operator(...) appears on the right-hand in destructuring then its called as Spread Synatax. It takes all the other elements which have no variable mapped to them and then maps it to rest variable.

Eg :-
```js
var planets = ["Mercury","Earth","Venus","Mars","Pluto","Saturn"];
var [first,second, ...rest] = ["Mercury","Earth", ...planets, "Saturn"];

console.log(first); // Mercury
console.log(second); // Earth
console.log(rest); // ["Venus","Mars","Pluto","Saturn"]
```

## <span class="header2">Built-in methods</span>

ES6 came along with lots of built methods. These methods simplyfy and standardize some scenarios that we developers came across often when working with JS.

<table>
<tr>
<td>Methods</td>
<td>Description</td>
<td>Syntax</td>
</tr>
<tr>
<td>Object Property Assignmnet</td>
<td>Used to assign properties of one or more source objects to a target object</td>
<td>

```js
var src1 = {a : 0}
var src2 = {b : 1, c : 2}
Object.assign(src1,src2)

src1 === {a : 0, b : 1, c : 2}
```

</td>
</tr>
<tr>
<td>Array Element  Finding</td>
<td>To find element in array</td>
<td>

```js
[1,2,3,4].find(x => x > 3) //4
```

</td>
</tr>
<tr>
<td>String Repeating</td>
<td>String repeating functionality</td>
<td>

```js
"hello".repeat(2)
```

</td>
</tr>
<tr>
<td>String Searching</td>
<td>Specific string functions to find a sub-string</td>
<td>

```js
hello.includes("ell") // true
```

</td>
</tr>
<tr>
<td>Number Type Checking</td>
<td>To check Non-Numbers and finite Numbers</td>
<td>

```js
Number.isNaN(42) // false
Number.isFinite(123) // true;
```

</td>
</tr>
<tr>
<td>Number Safety Checking</td>
<td>To check if integer number is in safe range. (i.e number is floating point numbber)</td>
<td>

```js
Number.isSafeInteger(42) /// true
Number.isSafeInteger(9007188254740992) //false
```

</td>
</tr>
<tr>
<td>Number Comparison</td>
<td>Uses EPSILON for more precise comparison of numbers</td>
<td>

```js
console.log(Math.abs((0.1 + 0.2) - 0.3) < Number.EPLISON) //true
```

</td>
</tr>
<tr>
<td>Number Truncation</td>
<td>Drops the fraction part of a floating point number</td>
<td>

```js
console.log(MAth.trunc(42.7)) // 42
```

</td>
</tr>
<tr>
<td>Number Sign Determination</td>
<td>Determines the sign of a number including non numbers</td>
<td>

```js
console.log(Math.sign(7)) //1
console.log(Math.sign(NaN)) //NaN
console.log(Math.sign(-0)) //-0
```

</td>
</tr>
</table>


## <span class="header2">Template Literals</span>

Template literals are string literals allowing embedded expressions. You can use multi-line strings and string interpolation features with them.

### <span class="header3">String Interpolation</span>

Template Strings can contain placeholders for string substitution using the `${ }` syntax,

Eg :-
```js
var name = "Brendan";
console.log(`Yo, ${name}!`);
```

### <span class="header3">Multiline Strings</span>

strings either exist on a single line or be split into multiline strings using a `\` (backslash) before each newline.

Eg :-
```js
var greeting = "Yo \
World";  
// Output :-
// Yo
// World
``` 

## <span class="header2">Classes</span>

Classes are a template for creating objects. They encapsulate data with code to work on that data.

Syntax :-
```js
class Class_name{

}

// Eg:-
class Polygon { 
   constructor(height, width) { 
      this.height = height; 
      this.width = width; 
   } 
}
```

Also, unlike funcitons and variables, class cannot be hoisted.

### <span class="header3">Understanding Why Setters & Getters are used</span>

```js
const person ={
  fname : 'Gaurav',
  lname : 'Dhuri',
  fullName() {
    return ${person.fname} ${person.lname}
  }
};

console.log(person.fullName()); // Result will be correct
```
However, in the above approach there a few problems or to simply it lacks effiency. `console.log(person.fullName())` is read only meaning we cannot set a person full name from outside. Also, we have to access fullName as a method than a property which can cause confusion. Instead of this approach we can use the concept of setters and getters here.



### <span class="header3">Setters</span>

A setter function is invoked when there is an attempt to set the value of a property.

```js
const person ={
  fname : 'Gaurav',
  lname : 'Dhuri',
  // setting fullName as getter we can access it like a property
  get fullName() {  
    return ${person.fname} ${person.lname}
  }
  console.log(person.fullName);
```

### <span class="header3">Getter</span>

A getter function is invoked when there is an attempt to fetch the value of a property.

```js
const person ={
  fname : 'Gaurav',
  lname : 'Dhuri',
  get fullName() {  
    return ${person.fname} ${person.lname}
  }
  // using this if we set full name from outside and it will update the object accordingly on its own.
  set fullName(value){
    const parts = value.split(' ');
    this.fname = parts[0];
    this.lname = parts[1];
  }
};

person.fullName = 'Yash Chuarasia';

console.log(person);
// fname : 'Yash'
// lname : 'Chuarasia'
// fullName : (...)
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