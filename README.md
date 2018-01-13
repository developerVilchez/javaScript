# javaScript

## INDEX
* [Basics](#basics)
    * [Link](#link)
    * [Alert](#alert)
    * [Comments](#comments)
    * [Console](#console)
* [Variables](#variables)
* [Data Types](#data-types)
    * [Math](#math-)
    * [Strings](#strings-)
    * [Template Literals](#template-literals)
* [Conditionals](#conditionals)
    * [Operators](#operators)
    * [Ternary Operators](#ternary-operators)
    * [Switch](#switch)
* [Loops](#loops)
    * [While Loops](#while-loops)
    * [For Loops](#for-loops)
    * [Do While Loops](#do-while-loops)
    * [Nested Loops](#nested-loops)
* [Functions](#functions)
    * [Type of functions](#type-of-functions)
        * [functions declarations](#functions-declarations)
        * [Function Expressions](#function-expressions)
            * [Functions as parameters](#functions-as-parameters)
            * [Inline function expressions](#inline-function-expressions)
        * [Inmidiatley Invokable function expresions - IIFEs](#inmidiatley-invokable-function-expresions---iifes)
        * [Property methods](#property-methods)
    * [Print Functions](#print-function)
    * [Return Functions](#return-function)
    * [Run a Function](#run-a-function)
    * [Parameters vs. Arguments](#parameters-vs-arguments)
    * [Scope](#scope)
        * [Shadowing or Scope overriding](#shadowing-or-scope-overriding)
    * [Hoisting](#hoisting)
    
* [Arrays](#arrays)
    * [Array Properties and Methods](#array-properties-and-methods)
    * [Array Loops](#array-loops)
    * [Arrays in Arrays](#arrays-in-arrays)
* [Objects](#objects)
* [Dates & Time](#dates--time)
* [jQuery](#jQuery)
    * [DOM](#dom)
    * [Methods](#methods)
    * [Event Listening with jQuery](#event-listening-with-jquery)
* [Needs futher clarification](#needs-futher-clarification)
* [Source of the materials](#source-of-the-materials)
    


## Basics

### Link
Link correctly html to js document:
`<script src="folderName/documentName.js"></script>`

### Alert
To create an alert on the site: <br>
`alert('Hello World!');`

### Comments
// One line comments <br>
/* for more than one line comments*/

### Console
console.log();<br>
console.table();<br>
console.error('This is a error');<br>
console.clear();<br>
console.warn('This is a warning');<br>
console.time();<br>
    between this 2 we can put anything (like console.log('Hello World!'); 4 times) and will print it in the console and tell us the time that took that process.<br>
console.timeEnd();

## Variables

**var** <br>
`var city = "Madrid";` <br>
This is how you declare a variable. <br>
Can be reassigned a different value.

**Naming conventions**

* dont use numbers as first character
* dont use spaces
* dont use "-"
* can be used "_" or "$" to start the name but not recomended.
* Use *camelCase* naming for a multi-word property name, and avoid the space or -.

**Initialize a variable** <br>
var city; <br>
without asigning any value initially. <br>
the value can be assigned afterwards.<br>
It is often used when there is a condition (If statement, if something it is true city = Barcelona).<br>
city = Madrid;

**let** <br>
works similar to *var*. <br>
was implemented with ES6. <br>

**const** <br>
constant. <br>
can not be reassigned. <br>
a value has to be assigned initially. <br>
In some cases, like when a *const* declares an object like the one in the following example, and values in the object can be change, what can not change in this case is sister, but can change the age number, the name, etc. <br> 
We can change the data inside of the object but not the object itself, can not be reassigned to a new object. <br>
Example:
```javascript
const sister = {
  name: "Sarah", 
  age: 23,
  parents: [ "alice", "andy" ],
  siblings: ["julia"],
  favoriteColor: "purple",
  pets: true
};
```
Const make your code more robust and readable.

## Data Types

Primitive & Refrence //needs clarification***************************************

**Primitive data types**:
* String ('' inside of quotation mark any concadenation of caracthers)
* Numbers
* Null (empty value)
* Undefined (variable that has no value assigned)
* Boolean (true/false)
* Symbols (ES6 - )

**Reference data types**:
* Arrays
* Objects
* Functions
* Dates
* anything that we can store in a variable

**JavaScript is dinamically typed language** <br>
data types are associated with values not with the variables. <br>
same variable can store different types and does not need to specify the type of data. <br>

**Data Type Conversion** <br>
To a string: <br>
by adding string(value) <br>
let amount = string(5); -> it is no longer a number, it is a string.<br>
same can be done with any data type. <br>

by adding .toString() property <br>
let amount = (5).toString();

To a number <br>
by adding Number(value) <br>
by adding .parseInt() property <br>
by adding .parseFloat() property <br>

**Data Type Cohersion** <br>
//needs clarification***************************************

### Math <br>
`Math.round();` will round the number. <br>
`Math.ceil();` will round the number up. <br>
`Math.floor();` will round the number down. <br>
`Math.sqr();` will give you the square root of the number. <br>
`Math.abs();` will give you the absolute of the number. <br>
`Math.pow();` will take 2 values and first the value number, second the value for the times the number will multiply by itself. number to the power of the second number<br>
`Math.min();` will return the minimun number of the value-numbers inside of the (). <br>
`Math.max();` will return the biggest number of the value-numbers inside of the (). <br>
`Math.random();` will return a random number (). <br>

### Strings <br>
concadenation <br>
```javascript
const name = 'Elena';
const place = ' is here!';
let status;
status = name + place
console.log(status);
```
append += <br> 
```javascript
let name;
name = 'Elena';
name += 'is here!'
console.log(name);
```
escaping \ in case of conflict with quotation marks<br>
.lenght <br>
.conact(); <br>
.toUpperCase(); <br>
.toLowerCase(); <br>
.indexOf();<br>
.lastIndexOf();<br>
.charAt();<br>
.charAt(variableName.lenght - 1); will always return last character<br>
.substring(0, 3); will return a new string (will bring the characters in between the index inside the () in this case the characters from the string from 0 to 3 ) from the original one<br>
.slice(); more use with arrays. similar to the substring, but if you put a negative number can start from the end of the string<br>
.split(); a string can be split by the space or coma (what it is split by needs to be specified inside of the ()) an crate an array with the result. (tags example)<br>
.replace(); <br>
.includes(); checks in the string if the value you put inside the () it is inside of the original string.<br>

### Template literals
Easier way to write html with js without using concadenation. <br>
example:
```javascript
const building = 'New Tower';
const city = 'Berlin';
const country = 'Germany';
let list;

list = `
    <ul>
    <li>Building: ${building}</li>
    <li>City: ${city}</li>
    <li>Country: ${country}</li>
    </ul>
`;

document.body.innerHTML = list;
```

## Conditionals

Evaluate a condition an execute based if the condition it is true or not.

```javascript
const amount =  50;

if(amount == 50){
    console.log("Well done, It´s correct!")
} else {
    console.log("Sorry, not correct this time!")
}
```
returns: <br>
Well done, It´s correct!<br>

```javascript
const flavor =  "lemon";

if(flavor === "lemon"){
    console.log("The flavor is lemon!");
} else if(flavor === "mint"){
    console.log("The flavor is mint!");
} else {
    console.log("Sorry, there is no flavor!")
}
```
returns: <br>
The flavor is lemon!<br>

### Operators
`>` greater than <br>
`>=` greater than or equal<br>
`<` less than <br>
`<=` less than or equal<br>
`==` equal value <br>
`===` equal value and type <br>
`!=` not equal <br>
`!==` not equal value and type <br>
`&&` and <br>
`||` or <br>

example:
```javascript
const name =  "Marta";
const age =  20;

if(age > 0 && age < 12){
    console.log(`${name} is a child because she is ${age} years old`);
} else if(age >= 13 && age <= 19){
    console.log(`${name} is a teen because she is ${age} years old`);
} else {
    console.log(`${name} is an adult because she is ${age} years old`);
}
```
returns: <br>
Marta is an adult because she is 20 years old<br>

### Ternary Operators
Shorter way to make operators <br>
represented by the "?" question mark.<br>
//needs clarification*****************************************

### Switch

Recommended when there is a lot of cases.<br>
very similar else if. <br>

```javascript
const flavor = "lemon";

switch(flavor){
    case "lemon":
        console.log("The flavor is lemon!");
        break;
    case "mint":
        console.log("The flavor is mint!");
        break;
    default:
        console.log("The flavor is not lemon or mint!");
        break;
}
```
returns: <br>
The flavor is lemon!<br>


## Loops

Allows iteration. Repeat an action for a number of times.

**Break & continue**
apply to all kind of loops<br>
Break: will stop the iteration <br>
continue: will make the iteration continue.

### While Loops:

Example:
Count up to a 100 monkeys 🐒
```javascript
var x = 0;
while (x <= 99) {
x = x + 1;
console.log( x + " monkey");
}
```

While the condition is true `(x <= 99)` will add one `x = x + 1;`, from the starting point `var x = 0;` and print `console.log( x + " monkey")` for each adition, until the condition stops being true.

Three main parts for a loop:
* When to start `var x = 0;` declaration.
* When to stop `while (x <= 99)` condition.
* How to get to next item `x = x + 1`

"Fizzbuzz" example:
* Loop through the numbers 1 to 100
* If the number is divisible by 3, print "Fizz"
* If the number is divisible by 5, print "Buzz"
* If the number is divisible by both 3 and 5, print "FizzBuzz"
* If the number is not divisible by 3 or 5, print the number

```javascript
var x = 1;
while (x <= 100) {
   if (x % 3 === 0 && x % 5 === 0){
        console.log ("FizzBuzz"); 
    }else if (x % 5 === 0){
        console.log("Buzz");
    }else if (x % 3 === 0){
        console.log("Fizz");
    }else {
        console.log(x);
    }
    x = x + 1; 
}
```

"Nasa" example:

* Orbiter transfers from ground to internal power (50 seconds)
* auto sequence start (31 seconds)
* Activate sound suppression system (16 seconds)
* Activate burnoff system (10 seconds)
* engine start (6 seconds)
* ignition and liftoff! (0 seconds)
* If there's a task being completed, it prints out the task
* If there is no task being completed, it prints out the time as x seconds

```javascript
var x = 60;
while(x >= 0){
    if (x === 50){
        console.log ("Orbiter transfers from ground to internal power"); 
    }else if (x === 31){
        console.log("auto sequence start");
    }else if (x === 16){
        console.log("Activate sound suppression system");
    }else if (x === 10){
        console.log("Activate burnoff system");
    }else if (x === 6){
        console.log("engine start");
    }else if (x === 0){
        console.log(" ignition and liftoff!");
    }else {
        console.log( x + " seconds");
    }
x = x - 1;
}
```

### For Loops

> for ([initialExpression]; [condition]; [incrementExpression])
> statement
>  **MDN Reference**

Example:
Count up to a 100 monkeys 🐒
```javascript
for (var i = 0; i <= 100; i = i + 1 ){ 
console.log( i + " monkey");
}
```
All the neccesary information is declare in the first line.

Three main parts for a loop:
* When to start `var i = 0;` the declaration.
* When to stop `i <= 100;` the condition.
* How to get to next item `i = i + 1 ` or `i++ `

### Do While Loops
Even if the condition it is not true, the out put will run at least once.
```javascript
var x = 200;
do{
    console.log( x + " monkey");
    x = x + 1;
}
while (x <= 99);
```

### Nested Loops

One or more loops can be nested inside of other loop.

The First/Main loop will triger the loop, then the nested one will loop until the condition is not longer true, stops, to go back to the main loop, that will trigger the nested ones everytime, until its condiction it is no longer true.

example:
```javascript
for (var x = 0; x < 4; x = x + 1) {
  for (var y = 0; y < 3; y = y + 1) {
    console.log(x + "," + y);
  }
}
```
that will print:
> 0, 0 <br>
> 0, 1 <br>
> 0, 2 <br>
> 1, 0 <br>
> 1, 1 <br>
> 1, 2 <br>
> 2, 0 <br>
> 2, 1 <br>
> 2, 2 <br>
> 3, 0 <br>
> 3, 1 <br>
> 3, 2 <br>

**Increment and decrement**

> x++ or ++x // same as x = x + 1 <br>
> x-- or --x // same as x = x - 1 <br>
> x += 3 // same as x = x + 3 <br>
> x -= 6 // same as x = x - 6 <br>
> x *= 2 // same as x = x * 2 <br>
> x /= 5 // same as x = x / 5 <br>

## Functions

package up code so you can easily use (and reuse) a block of code. 

### Type of functions:<br>
functions expressions, functions declarations, property methods. <br>
They all can take parameters. <br>

#### functions declarations
```javascript
function greeting() {
  return 'Hello';
}
console.log(greeting());
```
Returns: <br>
Hello<br>

One parameter, in this case name:
```javascript
function greeting(name) {
  return 'Hello ' +  name;
}
console.log(greeting('Leticia'));
```
Returns: <br>
Hello Leticia<br>

More parameters, in this case name & lastName:
```javascript
function greeting(name, lastName) {
  return 'Hello ' +  name + ' ' + lastName;
}
console.log(greeting('Leticia', 'Smith'));
```
Returns: <br>
Hello Leticia Smith<br>

Default values for parameters in case of undefine, in case the parameters are not passed:<br>
```javascript
function greeting(name = "John", lastName = "Smith") {
  return 'Hello ' +  name + ' ' + lastName;
}
console.log(greeting());
```
Returns: <br>
Hello John Smith<br>
If paramaters are passed will over-write the default values.

#### Function Expressions

A function stored inside a variable it's called a function expression.
Examples:

```javascript
const amount = function(y = 3){
    return y + y;
};
console.log(amount(5));
```
Returns: 10. <br>
"y" is = 3 to have a default, but it is over-writen by the arguments passed 5, in this case.

```javascript
var catSays = function(max) {
  var catMessage = "";
  for (var i = 0; i < max; i++) {
    catMessage += "meow ";
  }
  return catMessage;
};
```
Function has no name, it is anonymous.

##### Functions as parameters

callback: A function that is passed into another function.

##### Inline function expressions
//needs clarification*****************************************
Example:
```javascript
function movies(messageFunction, name) {
  messageFunction(name);
}

movies(function displayFavorite(movieName) {
  console.log("My favorite movie is " + movieName);
}, "Vikings");
```
Returns: My favorite movie is Vikings

Example:
```javascript
function emotions(myString, myFunc) {
    console.log("I am " + myString + ", " + myFunc(2));
}
emotions("happy", function laugh(num) {
    var risa = "";
    for (var i = 0; i < num; i++){
        risa += "ha";
    }
    return risa + "!";
});
```
Returns: I am happy, haha!


Example:
```javascript
var cry = function sad() {
    return "boohoo!";
}

console.log(cry());
```
Returns: boohoo!

anonymous inline function expressions: for functions that are not going to be reused.

Example:
```javascript
var laugh = function(num) {
    var L = "";
    for (i = 0; i < num; i++){
        L += "ha";
    }
    return L + "!";
}

console.log(laugh(3));
```
Returns: hahaha!

#### Inmidiatley Invokable function expresions - IIFEs
It is declare and run at the same time. <br>
very useful in case of modules. <br>
```javascript
(function(city){
    console.log('We are travelling to ' + city + '!')
})('Oslo');
```

#### Property methods
Put functions inside of objects:
```javascript
const list = {
    add: function(){
        console.log('Add item')
    }
}
list.add();
```

### Print function

using console.log, like this example, only displays a value.
```javascript
function sayHello() {
  var message = "Hello!"
  console.log(message);
}
```
Good to test code, get feedback and debugging purposes.
`console.log` to test your code in the JavaScript console, just that.

### Return function

Return statement:
```javascript
function sayHello() {
  var message = "Hello!"
  return message; // returns value instead of printing it
}
```
Stops the execution of the function.

#### Some Practise:
Build a triangle:
```javascript
function makeLine(length) {
    var line = "";
    for (var j = 1; j <= length; j++) {
        line += "* ";
    }
    return line + "\n";
}

function buildTriangle(length) {
    var Line = "";
    for (var i = 1; i <= length; i++) {
       Line += makeLine(i);
    }
    return Line;
}

console.log(buildTriangle(10));
```
prints: <br>
![image](https://user-images.githubusercontent.com/30567608/34456985-85ec9bb2-eda4-11e7-83e5-a11aa28311ff.png)


```javascript
function laugh(num){
    var laughter = "";
    for (var x = 0; x < num; ++x ){ 
        laughter += "ha";
    }
return laughter + "!";
}
console.log(laugh(3));
```
prints:
hahaha!

### Run a function

Up to here we only have declare the functions. <br>
For the function to do something, we have to invoke or call the function using the function name, 
followed by parentheses with any arguments that are passed into it, if it has any.
`cookChiken(6); or doubleAction(look, jump); or sayHello()`

### Parameters vs. Arguments

**Parameters** are always variables name and appears in the function declaration, that are used to store the data that's passed into a function for the function to use. <br>
**Arguments** are always going to be a value, the actual data (i.e. any of the JavaScript data types - a number, a string, a boolean, etc.) and will always appear in the code when the function is called or invoked.

### Scope

Global Scope: defined at the top level, not inside of any functions. Available everywhere.

Function Scope: variable defined inside a function. Available inside of the function it was declared in (even in functions declared inside the function).

Block Scope: //needs clarification***************************************

JavaScript Engine´ll start looking inside the current function when trying to access an identifier. 
If it does not get any results it'll continue to the next outer function to see if it can find any there. 
It will keep doing this until it reaches the global scope.

Minimize the use of global variables. Can lead to bad variable names, conflicting variable names, and messy code.

#### Shadowing or Scope overriding

This first case will shadow, since "x" it is re-asign inside of the function:

```javascript
var x = 1;

function addTwo() {
  x = x + 2;
}

addTwo();
x = x + 1;
console.log(x);
```

The way to avoid it´s by declering "x" in a new variable inside of the function.
From altering a global scope variable becomes a function scope variable.

```javascript
var x = 1;

function addTwo() {
  var x = x + 2;
}

addTwo();
x = x + 1;
console.log(x);
```

### Hoisting 
//needs clarification*****************************************
To avoid bug due to this: 
always declare functions at the top of the sripts and variables at the top of the functions.
This way syntax and behavior are consistent.



## Arrays

Stores information.
Stores multiple values into a single, organized data structure. 
Start an array by listing values separated with commas between square brackets []. <br>
Most used one: `var donuts = ["glazed", "powdered", "jelly"];` <br>
Also can be done with the Array constructor: `var donuts = new Array("glazed", "powdered", "jelly");` <br>
You can store strings, like the example above or numbers, booleans or any type of data, even mixed them. But usually arrays are made out of same data values. <br>
We can even put an array inside an array to create a nested array.

**Arrays Elements** : Are the individual pieces of data in the array.

**Index**: the position/location of the element inside of the Array (starts counting from 0).

**Accessing Array elements**:

First put the name of the array followed by square brackets [] containing the index of the value you want to access.

Example:
```javascript
var donuts = ["glazed", "powdered", "sprinkled"];
console.log(donuts[0]);
```
Prints: "glazed"

In case we need to change the value of an element in array:
```
donuts[1] = "glazed cruller"; 
console.log(donuts[1]);
```
Prints: "glazed cruller"

### Array Properties and Methods 

[MDN documentation about Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

JavaScript provides a large number of built-in methods for modifying arrays and accessing values in an array.
<!-- Type [] in the console to see full list -->
List:
concat()
Array()
copyWithin()
entries()
every()
fill()
filter()
find()
findIndex()
flatMap()
flatten()
forEach()
includes()
indexOf()
join()
keys()
lastIndexOf()
map()
pop()
push()
reduce()
reduceRight()
reverse()
shift()
slice()
some()
sort() 
splice()
toLocaleString()
toString()
unshift()
values()

Array.lenght = find the lenght of an array. <br>
example:
```
var donuts = ["glazed", "powdered", "sprinkled"];
console.log(donuts.length);
```
Prints: 3

Array.push & Array.pop: <br>
modifying arrays.

push() <br>
add elements to the end of an array. <br>
example:
```
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled"];
donuts.push("powdered");
```
Returns: 7 <br>
donuts array: ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled", "powdered"]

pop() =  <br>
remove elements from the end of an array. <br>
example:
```
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled", "powdered"];

donuts.pop(); 
donuts.pop();
donuts.pop();
```
Returns: "cinnamon sugar" <br>
donuts array: ["glazed", "chocolate frosted", "Boston creme", "glazed cruller"]

splice() = <br>
powerful method. <br>
changes the contents of an array by removing existing elements and/or adding new elements.<br>
allows you to specify the index location to add new elements, as well as the number of elements you'd like to delete (if any).<br>
sintax: <br>
`array.splice(start[, deleteCount[, item1[, item2[, ...]]]])`

Examples: <br>
Remove 0 elements from index 2, and insert "drum":
```
var myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];
var removed = myFish.splice(2, 0, 'drum');
```
result: <br>
myFish is ["angel", "clown", "drum", "mandarin", "sturgeon"] <br> 
removed is [], no elements removed

Remove 1 element from index 3:
```
var myFish = ['angel', 'clown', 'drum', 'mandarin', 'sturgeon'];
var removed = myFish.splice(3, 1);
```
result: <br>
removed is ["mandarin"] <br>
myFish is ["angel", "clown", "drum", "sturgeon"]

More examples [MDN Splice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)

### Array Loops

Example:
```javascript
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

for (var i = 0; i < donuts.length; i++) {
    donuts[i] += " hole";
    donuts[i] = donuts[i].toUpperCase();
}
```
Prints: 
donuts array: ["JELLY DONUT HOLE", "CHOCOLATE DONUT HOLE", "GLAZED DONUT HOLE"]

**The forEach() loop**
alternative way to iterate over an array
Parameters: can take up to 3.(iterator, index, array )

Example:
```javascript
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

donuts.forEach(function(donut) {
  donut += " hole";
  donut = donut.toUpperCase();
  console.log(donut);
});
```
Prints: 
JELLY DONUT HOLE
CHOCOLATE DONUT HOLE
GLAZED DONUT HOLE

forEach() method calls the function once for each element in the array.
Example:
```javascript
words = ["cat", "in", "hat"];
words.forEach(function(word, num, all) {
  console.log("Word " + num + " in " + all.toString() + " is " + word);
});
```
Prints:
Word 0 in cat,in,hat is cat
Word 1 in cat,in,hat is in
Word 2 in cat,in,hat is hat

Example:
```javascript
var test = [12, 929, 11, 3, 199, 1000, 7, 1, 24, 37, 4,
    19, 300, 3775, 299, 36, 209, 148, 169, 299,
    6, 109, 20, 58, 139, 59, 3, 1, 139
];

test.forEach(function(value,index) {
    if(value % 3 === 0){
      test[index] += 100;
    }
});

console.log(test);
```
Prints:
[ 112, 929, 11, 103, 199, 1000, 7, 1, 124, 37, 4, 19, 400, 3775, 299, 136, 209, 148, 169, 299, 106, 109, 20, 58, 139, 59, 103, 1, 139 ]

**Map**
Returns a new array from an existing array.
Accepts only 1 argument.

Example:
```javascript
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

var improvedDonuts = donuts.map(function(donut) {
  donut += " hole";
  donut = donut.toUpperCase();
  return donut;
});
```
Prints:
donuts array: ["jelly donut", "chocolate donut", "glazed donut"]
improvedDonuts array: ["JELLY DONUT HOLE", "CHOCOLATE DONUT HOLE", "GLAZED DONUT HOLE"]

Example:
```javascript
var bills = [50.23, 19.12, 34.01,
    100.11, 12.15, 9.90, 29.11, 12.99,
    10.00, 99.22, 102.20, 100.10, 6.77, 2.22
];

var totals = bills.map(function(amount){
    amount += Number (0.15*amount)
    return Number(amount.toFixed(2));
})

console.log(totals);
```
Prints:
[ 57.76,
  21.99,
  39.11,
  115.13,
  13.97,
  11.38,
  33.48,
  14.94,
  11.5,
  114.1,
  117.53,
  115.11,
  7.79,
  2.55 ]

### Arrays in Arrays


Example:
```javascript
var donutBox = [
  ["glazed", "chocolate glazed", "cinnamon"],
  ["powdered", "sprinkled", "glazed cruller"],
  ["chocolate cruller", "Boston creme", "creme de leche"]
];

for (var row = 0; row < donutBox.length; row++) {
  for (var column = 0; column < donutBox[row].length; column++) {
    console.log(donutBox[row][column]);
  }
}
```
Prints:
"glazed"
"chocolate glazed"
"cinnamon"
"powdered"
"sprinkled"
"glazed cruller"
"chocolate cruller"
"Boston creme"
"creme de leche"
![image](https://user-images.githubusercontent.com/30567608/34461587-2d284776-ee2e-11e7-8b45-d7c69f7ecccc.png)

Example:
```javascript
var numbers = [
    [243, 12, 23, 12, 45, 45, 78, 66, 223, 3],
    [34, 2, 1, 553, 23, 4, 66, 23, 4, 55],
    [67, 56, 45, 553, 44, 55, 5, 428, 452, 3],
    [12, 31, 55, 445, 79, 44, 674, 224, 4, 21],
    [4, 2, 3, 52, 13, 51, 44, 1, 67, 5],
    [5, 65, 4, 5, 5, 6, 5, 43, 23, 4424],
    [74, 532, 6, 7, 35, 17, 89, 43, 43, 66],
    [53, 6, 89, 10, 23, 52, 111, 44, 109, 80],
    [67, 6, 53, 537, 2, 168, 16, 2, 1, 8],
    [76, 7, 9, 6, 3, 73, 77, 100, 56, 100]
];

for (var row = 0; row < numbers.length; row++) {
  for (var column = 0; column < numbers[row].length; column++) {
    if(numbers[row][column] % 2 === 0){
        numbers[row][column] = "even";
    }else{
       numbers[row][column] = "odd"; 
    }
  }
}
console.log(numbers);
```
Prints:
[ [ 'odd','even','odd','even','odd','odd','even','even','odd','odd' ],
  [ 'even','even','odd','odd','odd','even','even','odd','even','odd' ],
  [ 'odd','even','odd','odd','even','odd','odd','even','even','odd' ],
  [ 'even','odd','odd','odd','odd','even','even','even','even','odd' ],
  [ 'even','even','odd','even','odd','odd','even','odd','odd','odd' ],
  [ 'odd','odd','even','odd','odd','even','odd','odd','odd','even' ],
  [ 'even','even','even','odd','odd','odd','odd','odd','odd','even' ],
  [ 'odd','even','odd','even','odd','even','odd','even','odd','even' ],
  [ 'odd','even','odd','odd','even','even','even','even','odd','even' ],
  [ 'even','odd','odd','even','odd','odd','odd','even','even','even' ] ]


## Objects

It is a data structure in js that allows to store data about a particular item and we can keep track by using "key". <br>
**key : value** pairs separated from each other by commas. <br>
Inside curly Braces **{}** entire object is wrapped by it.<br>

Example:
```javascript
var sister = {
  name: "Sarah", 
  age: 23,
  parents: [ "alice", "andy" ],
  siblings: ["julia"],
  favoriteColor: "purple",
  pets: true,
  address:{
      city:"Barcleona",
      country:"Spain"
  },
  hobbies: ["gym", "music"]
}
```
This is object-literal notation.

Use they key to get in return value, to acces properties: <br>
`sister["parents"]` by bracket notation.<br>
`sister.parents` by dot notation.<br>
Both returns: `[ "alice", "andy" ]`

To access other values:<br>
`sister.address.country` returns: "Spain" <br>
`sister.hobbies[0]` returns: "gym" <br>

![image](https://user-images.githubusercontent.com/30567608/34904940-c601ac28-f84f-11e7-8a27-17c75432fd1f.png)

"Key" can be a property (like the ones above) or a method.
properties (information about the object) and methods (functions or capabilities the object has).<br>
Method in the following example is `paintPicture` with a function as a value (the remaining keys are properties):
```javascript
var sister = {
  name: "Sarah",
  age: 23,
  parents: [ "alice", "andy" ],
  siblings: ["julia"],
  favoriteColor: "purple",
  pets: true,
  paintPicture: function() { return "Sarah paints!"; }
};

sister.paintPicture();
```
Returns: "Sarah paints!"

Naming conventions:

To name properties:
* dont use numbers as first character.
* dont use spaces
* dont use "-".
Usel *camelCase* naming for a multi-word property name, and avoid the space or -.

Example:
```javascript
var savingsAccount = {
    balance: 1000,
    interestRatePercent: 1,
    deposit: function addMoney(amount) {
        if (amount > 0) {
            savingsAccount.balance += amount;
        }
    },
    withdraw: function removeMoney(amount) {
        var verifyBalance = savingsAccount.balance - amount;
        if (amount > 0 && verifyBalance >= 0) {
            savingsAccount.balance -= amount;
        }
    },
    printAccountSummary: function () {
        return "Welcome!\nYour balance is currently $" + savingsAccount.balance + " and your interest rate is " + savingsAccount.interestRatePercent + "%."
    }
};

console.log(savingsAccount.printAccountSummary());

```
Returns: <br>
Welcome! <br>
Your balance is currently $1000 and your interest rate is 1%.

Example:
```javascript
var facebookProfile = {
    name: "Elena",
    friends: 200,
    messages: ["Hola", "Feliz año", "Cómo estas?"],
    postMessage: function(message){
        message = "have a great one!";
        return facebookProfile.messages.push(message);
    },
    deleteMessage: function(index){
        index <= facebookProfile.messages.length;
        return facebookProfile.messages.splice(index, 1);
    },
    addFriend: function(){
        return facebookProfile.friends +=1;
    },
    removeFriend: function(){
        return facebookProfile.friends -=1;
    }
}

```
**Array of objects**<br>

Example:
```javascript
var person = [
    { name: "Mario", age: 40 },
    { name: "Teresa", age: 36 },
    { name: "Cristina", age: 4 }
];

for(let i = 0; i < person.length; i++){
    console.log(person[i].name);
}

```
Returns: 
Mario<br>
Teresa <br>
Cristina <br>

Example:
```javascript
var donuts = [
    { type: "Jelly", cost: 1.22 },
    { type: "Chocolate", cost: 2.45 },
    { type: "Cider", cost: 1.59 },
    { type: "Boston Cream", cost: 5.99 }
];

donuts.forEach(function(element) {
  console.log(element.type + " donuts cost $" + element.cost + " each");
});

```
Returns: <br>
Jelly donuts cost $1.22 each <br>
Chocolate donuts cost $2.45 each <br>
Cider donuts cost $1.59 each <br>
Boston donuts Cream cost $5.99 each <br>

**For in loop**
allow us to iterate through the key value pairs.
```javascript
const customer = {
    Name: "Cristina",
    LastName:"Smith",
    age:"25"
}

for (let person in customer){
    console.log(`${person} : ${customer[person]}`);
}
```
Returns: <br>
Name : Cristina<br>
LastName : Smith<br>
age : 25<br>


## Dates & Time

It is an object <br>

```javascript
let val;
const today = new Date();
val = today;
console.log(val);
```
Returns: <br>
Today´s date. <br>

If you want to declare any other date, just put it inside the () of new Date.<br>
`const importantDate = new Date("9-10-1981 12:30:00");`<br>
that will include the date especified date and time. and there is different ways to write it. <br>
```javascript
let val;
const today = new Date();
val = today.getMonth();
val = today.getDate();
val = today.getDay();
val = today.getFullYear();
val = today.getHours();
val = today.getMinutes();
val = today.getSeconds();
val = today.getMilliseconds();
val = today.getTime();

console.log(val);
```
Months are cero based, so january it is 0.<br>
Day is cero based, and start counting on sunday, so saturday is 6<br>

To modify/maniulate dates can be done with "set":
```javascript
let anniversarie = new Date("September 21 2006");
anniversarie.setMonth(1);
anniversarie.setDate(10);
anniversarie.setDay(5);
anniversarie.setFullYear(1986);
anniversarie.setHours(2);
anniversarie.setMinutes(45);
anniversarie.setSeconds(22);
anniversarie.setMilliseconds(22);

console.log(anniversarie);
```

# jQuery

It is a javaScript Library.

$ is a function that points to jQuery.

## DOM
It is a data structure

parent elements: one level above
child elements: one level below
sibling elements: in same level

CDN = Content Delivery Network

Selectors by tag name:
$('div');
Selectors by class name:
$('.container');
Selectors by id name:
$('#footer');

DOM transversal methods to move around the Dom:
$('.container').parent() => inmidiate parent element. only goes up 1 level.
$('.container').parents() => will go all the way to the top.
$('.container').child() => only goes down 1 level.
$('.container').find() => will go down more than one level.
$('.container').siblings() => that has same parent.

### Methods

toggleClass()
examples:
```javascript
var featuredArticle;

featuredArticle = $('.featured');
featuredArticle.toggleClass('featured');
```

toggleClass() & next()
```javascript
var article2, article3;

article2 = $(".featured");
article2.toggleClass("featured");

article3 = article2.next();
article3.toggleClass("featured");
```

first() & attr()
```javascript
var navList;
navList = $('.nav-list li a').first();
navList.attr('href', '#1');
```

css()
```javascript
var articleItems;
articleItems = $('.article-item');
articleItems.css("font-size", "20px");
```

val() & text()
```javascript
$('#input').on('change', function() {
    var val;
    val = $('#input').val();
    $(".articles").children("h1").text(val);
});
```

remove()
```javascript
var articleItems;

articleItems = $(".article-item");
articleItems.find("ul").remove();
```

this add children to an element:
append() : adds last child to the selected element
prepend() : adds first child to the selected element

this add sibling to an element:
insertBefore() : adds the siblings before the selected element
insertAfter() : adds the siblings after the selected element

```javascript
var family1, family2, bruce, madison, hunter;

family1 = $('#family1');

family2 = $('<div id="family2"> <h1>Family2</h1> </div>');
bruce = $('<div id="bruce"> <h2>Bruce</h2> </div>');
madison = $('<div id="madison"> <h3>Madison</h3> </div>');
hunter = $ ('<div id="hunter"> <h3>Hunter</h3> </div>');

family2.insertAfter(family1);
family2.append(bruce);
bruce.append(madison);
hunter.insertAfter(madison);
```

each()
```javascript
$('p').each(function(){
    var count = $(this).text().length;
    $(this).append(" " + count);
});
```



## Event Listening with jQuery
monitorEvents();

elements that are neccesary:
* target element to listen
* the event we are listening (kind of event)
* reaction to the event (function)

the target element calls the callback function when the event occurs

remove() & addClass()
```javascript
$("#my-button").on("click", function(){
    $("#my-button").remove();
    $('body').addClass("success");
});
```

**event object**:
this object it is called when the function it is triggered
usually reffer to as: e, evt, or event
contains info  about the event
very useful tool.

example:
```javascript
$( 'article' ).on( 'click', function( evt ) {
    console.log( evt );
});
```

Common Event Properties:
altKey, bubbles, button, buttons, cancelable, char, charCode, clientX, clientY, ctrlKey, currentTarget, data, detail, eventPhase, key, keyCode, metaKey, offsetX, offsetY, originalTarget, pageX, pageY, relatedTarget, screenX, screenY, shiftKey, target, toElement, view, which
there is more.

example:
```javascript
$( 'article' ).on( 'keypress', function( evt ) {
    $( evt.target ).css( 'background', 'red' );
});
```

event object can be used to prevent the default action:
```javascript
$( '#myAnchor' ).on( 'click', function( evt ) {
    evt.preventDefault();
    console.log( 'You clicked a link!' );
});
```

**The Convenience Method**

Instead of writing like the previus examples, after the target `$( 'article' ).on( 'keypress', function( evt )`,
the event that we are waiting for to triggers the function/reaction it becomes a method.

example:
```javascript
$( "#other" ).click(function() {
  $( "#target" ).keypress();
});
```

**Event Delegation**
what about when the target doesn't exist yet? 
Event delegation allows us to attach a single event listener, to a parent element, that will fire for all descendants matching a selector, whether those descendants exist now or are added in the future.
adding a third parameter between the event and the function

example:
```javascript
$( '.container' ).on( 'click', 'article', function() { … });
```




## Needs futher clarification:
* Primitive & Refrence data types: difference between them
* Data Type Cohersion
* Ternary Operators
* block scope
* Hoisting 
* Inline function expressions

## Source of the materials:
* MDN
* Udacity Google Challenge Scholarship: Front-End Web Dev 2017-2018
* [learn.jquery.com](https://learn.jquery.com/events/event-delegation/)
* JavaScript from the bigining by [Brad Traversy](https://twitter.com/traversymedia)