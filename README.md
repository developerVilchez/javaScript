# javaScript

## Loops

Allows iteration. Repeat an action for a number of times.

###While Loops:

Example:
Count up to a 100 monkeys 🐒
```var x = 0;
while (x <= 99) {
x = x + 1;
console.log( x + " monkey");
}```
While the condition is true `(x <= 99)` will add one `x = x + 1;`, from the starting point `var x = 0;` and print `console.log( x + " monkey")` for each adition, until the condition stops being true.

Three main parts for a loop:
* When to start `var x = 0;`
* When to stop `while (x <= 99)`
* How to get to next item `x = x + 1`

"Fizzbuzz" example:
* Loop through the numbers 1 to 100
* If the number is divisible by 3, print "Fizz"
* If the number is divisible by 5, print "Buzz"
* If the number is divisible by both 3 and 5, print "FizzBuzz"
* If the number is not divisible by 3 or 5, print the number

`var x = 1;
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
}`

"Nasa" example:

* Orbiter transfers from ground to internal power (50 seconds)
* auto sequence start (31 seconds)
* Activate sound suppression system (16 seconds)
* Activate burnoff system (10 seconds)
* engine start (6 seconds)
* ignition and liftoff! (0 seconds)
* If there's a task being completed, it prints out the task
* If there is no task being completed, it prints out the time as x seconds

`var x = 60;
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
}`

### For Loops

> for ([initialExpression]; [condition]; [incrementExpression])
>  statement
>  **MDN Reference**

Example:
Count up to a 100 monkeys 🐒
```for (var i = 0; i <= 100; i = i + 1 ){ 
console.log( i + " monkey");
}```
All the neccesary information is declare in the first line.

Three main parts for a loop:
* When to start `var i = 0;`
* When to stop `i <= 100;`
* How to get to next item `i = i + 1 `

### Nested Loops
