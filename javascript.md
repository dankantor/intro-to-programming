# Javascript

Javascript controls the interactivity of the webpage. We write our Javascript in a separate file. We can use Javascript to change information on the page, save data, fetch data from a server and more.&#x20;

```
<html>
  <head>
    <link rel="stylesheet" href="style.css"></link>
  </head>
  <body>
    <script type="text/javascript" src="script.js"></script>
  </body
</html>
```

### Variables

Variables are a way to store values in your code. You can store different types of values such as numbers (0,1,2...), strings "Hello world", booleans (true/false) and more.&#x20;

To create a variable you do this

```
var myNumber = 1;
var myString = "hi";
var myBoolean = true;
```

You can name a variable anything you like. You can then use variables the same way you use data anywhere.

```
var a = 1;
var b = 2;
var c = a + b;
```

### Functions

Functions are core to Javascript. Functions are pieces of code that usually take and input and then return an output. Here is a simple function that accepts two numbers, adds them and returns the sum.&#x20;

```
function addNumbers(a, b) {
  return a + b;
}
```

In the above example, we have named the function `addNumbers` so that later on we can call it by its name. We can see that the function takes two variables `a` and `b`. It then returns `a + b`.&#x20;

To call the function above all we have to do is write `addNumbers(1, 2)`. Usually we will want to set the output of a function to a variable `var sum = addNumbers(1,` `2);` We can also call a function with variables

```
var firstNumber = 5;
var secondNumber = 10;
var thirNumber = addNumbers(firstNumber, secondNumber); 
// 15
```

### If / Else

Many times we need to check if a variable is equal to a value and do something if it is. We may also want to do something if it is not. The way to do this is by using an `if` statement.&#x20;

```
var a = 1;
var b = 2;

if (a === b) {
  // do something here
} else {
  // do something different here
}
```

We use three `===` to check if things are equal. We can also do the opposite and check if two things are not equal by using `!==`.

### Arrays and Loops

There are times when we may want to store a set of values together in a list. We call this an Array. We write arrays like this&#x20;

```
var myArray = [0, 1, 2, 3];
```

We can then loop over all the values by using `forEach`

```
var myArray = [0, 1, 2, 3];
var total = 0;
myArray.forEach(function(i) {
  total += i;
});
// 6
```

In the above loop we go through the array for each value and then add it to the variable `total`. When the loop is finished `total` will equal 6.&#x20;

### Logging and Comments

Many times when we are writing code we want to see what a variable is equal to. We can do this by using `console.log(myVariable)`; We then can view the output in our development console. inside the browser.&#x20;

In the above examples we see `//` written a few times. We use this to write comments in our code. These comments are a way to remember what our code is supposed to do. When we come back later and read our code comments can help us.&#x20;

## Exercise

Create a function that returns the string "even" when it is passed an even number and "odd" when it is passed an odd number.

### Extra Credit

Use an array to do it.&#x20;
