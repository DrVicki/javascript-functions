# javascript-functions

In this lesson you will learn how to define and call a function in JavaScript.

## What is Function?

function is a group of statements which perform specific tasks and can be kept and maintained separately from the main program. 

Functions provide a way to create reusable code packages which are more portable and easier to debug. 

Here are some advantages of using functions:
  - Functions reduce the repetition of code within a program — Function allows you to extract commonly used blocks of code into a single component. Now you can perform the same task by calling this function wherever you want within your script without having to copy and paste the same block of code again and again.
  - Functions make the code much easier to maintain — Since a function created once can be used many times, any changes made inside a function automatically implements at all the applicable places.
  - Functions make it easier to eliminate errors — When the program is subdivided into functions, if any error occurs you know exactly what function is causing the error and where to find it. Therefore, fixing errors becomes much easier.

The following section will show you how to define and call functions in your scripts.

## Defining and Calling a Function

The **declaration** of a function 
  - starts with the ```function``` keyword, 
  - followed by the name of the function you want to create, 
  - followed by parentheses i.e. ```()``` and 
  - finally you place your function's code between curly brackets ```{}```. 

Here's the basic syntax for declaring a function:

```
function functionName() {
    // Code to be executed
}
```
Here is a simple example of a ```function```, which will show a hello message:

```
// Define function
function sayHello() {
    alert("Hello, welcome to this website!");
}
 
// Calling function
sayHello(); // 0utputs: Hello, welcome to this website!
```
Once a function is defined it can be called (invoked) from anywhere in the document, by typing its name followed by a set of parentheses, like```sayHello()``` in the example above.

⭐ **Note**: A function name must start with a letter or underscore character not with a number, optionally followed by the more letters, numbers, or underscore characters. Function names are case sensitive, just like variable names.

## Add Parameters to Functions

You can specify parameters when you define your function to accept input values at run time. The parameters work like placeholder variables within a function; they're replaced at run time by the values (known as argument) provided to the function at the time of invocation.

Parameters are set on the first line of the function inside the set of parentheses, like this:

```
function functionName(parameter1, parameter2, parameter3) {
    // Code to be executed
}
```
The ```displaySum()``` function in the following example takes two numbers as arguments, simply s them together and then displays the result in the browser.

```
// Defining function
function displaySum(num1, num2) {
    var total = num1 + num2;
    alert(total);
}
 
// Calling function
displaySum(6, 20); // 0utputs: 26
displaySum(-5, 17); // 0utputs: 12
```

You can define as many parameters as you like. However for each parameter you specify, a corresponding argument needs to be passed to the function when it is called, otherwise its value becomes undefined. Let's consider the following example:

```
// Defining function
function showFullname(firstName, lastName) {
    alert(firstName + " " + lastName);
}
 
// Calling function
showFullname("Clark", "Kent"); // 0utputs: Clark Kent
showFullname("John"); // 0utputs: John undefined
```

## Default Values for Function Parameters ES6

With ES6, now you can specify default values to the function parameters. This means if no arguments are provided to a function when it is called these default parameter values will be used. This is one of the most awaited features in JavaScript. Here's an example:

```
function sayHello(name = 'Guest') {
    alert('Hello, ' + name);
}

sayHello(); // 0utputs: Hello, Guest
sayHello('John'); // 0utputs: Hello, John
```

While prior to ES6, to achieve the same thing we had to write something like this:

```
function sayHello(name) {
    var name = name || 'Guest'; 
    alert('Hello, ' + name);
}

sayHello(); // 0utputs: Hello, Guest
sayHello('John'); // 0utputs: Hello, John
```
## Returning Values from a Function

A function can return a value back to the script which called the function using the ```return``` statement. The value may be of any type, including arrays and objects.

The ```return``` statement is usually placed as the last line of the function before the closing curly bracket and ends it with a semicolon, as shown in the following example.

```
// Defining function
function getSum(num1, num2) {
    var total = num1 + num2;
    return total;
}
 
alert(getSum(6, 20)); // 0utputs: 26
alert(getSum(-5, 17)); // 0utputs: 12
```

A function can not return multiple values. However, you can obtain similar results by returning an array of values, as demonstrated in the following example.

```
// Defining function
function divideNumbers(dividend, divisor){
    var quotient = dividend / divisor;
    var arr = [dividend, divisor, quotient];
    return arr;
}
 
// Store returned value in a variable
var all = divideNumbers(10, 2);
 
// Displaying individual values
alert(all[0]); // 0utputs: 10
alert(all[1]); // 0utputs: 2
alert(all[2]); // 0utputs: 5
```

## Working with Function Expressions

The syntax we've used before to create functions is called function declaration. There is another syntax for creating a function called a function expression.

```
// Function Declaration
function getSum(num1, num2) {
    var total = num1 + num2;
    return total;
}
 
// Function Expression
var getSum = function(num1, num2) {
    var total = num1 + num2;
    return total;
};
```

Once the function expression has been stored in a variable, the variable can be used as a function:

```
var getSum = function(num1, num2) {
    var total = num1 + num2;
    return total;
};
 
alert(getSum(5, 10)); // 0utputs: 15
 
var sum = getSum(7, 25);
alert(sum); // 0utputs: 32
```
⭐**Note**: There is no need to put a semicolon after the closing curly bracket in a function declaration. But function expressions, on the other hand, should always end with a semicolon.

💡**Tip**: In JavaScript, functions can be stored in variables, passed into other functions as arguments, passed out of functions as return values, and constructed at run-time.

The syntax of the function declaration and function expression looks very similar, but they differ in the way they are evaluated. Check out the following example:

```
declaration(); // Outputs: Hi, I'm a function declaration!
function declaration() {
    alert("Hi, I'm a function declaration!");
}
 
expression(); // Uncaught TypeError: undefined is not a function
var expression = function() {
    alert("Hi, I'm a function expression!");
};
```
As you can see in the above example, the function expression threw an exception when it was invoked before it defined, but the function declaration executed successfully.

JavaScript parses the declaration function before the program executes. Therefore, it doesn't matter if the program invokes the function before it is defined because JavaScript has hoisted the function to the top of the current scope behind the scenes. The function expression is not evaluated until it is assigned to a variable; therefore, it is still undefined when invoked.

ES6 has introduced even shorter syntax for writing function expressions which is called the arrow function.

## Understanding the Variable Scope

You can declare the variables anywhere in JavaScript. But, the location of the declaration determines the extent of a variable's availability within the JavaScript program, i.e. where the variable can be used or accessed. This accessibility is known as variable scope.

By default, variables declared within a function have local scope that means they cannot be viewed or manipulated from outside of that function, as shown in the example below:

```
// Defining function
function greetWorld() {
    var greet = "Hello World!";
    alert(greet);
}
 
greetWorld(); // Outputs: Hello World!
 
alert(greet); // Uncaught ReferenceError: greet is not defined
```

However, any variables declared in a program outside of a function have global scope, i.e. it will be available to all scripts, whether that script is inside a function or outside. Here's an example:

```
var greet = "Hello World!";
 
// Defining function
function greetWorld() {
    alert(greet);
}
 
greetWorld();  // Outputs: Hello World!
 
alert(greet); // Outputs: Hello World!
```

## Now mosey over to the "Get Your Hands on the Code" Page to practice!!
