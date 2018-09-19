[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Javascript 101

**Jennifer Meade, Instructor**

Welcome to your crash course to Javascript and jQuery!

You can refer back to this document if you forget forget the syntax for anything we're learning.

## Data Types

There are many built-in data types in JS. Tonight, we'll look at just a few of
the most straightforward ones. Mainly, we'll focus on three types: numbers,
strings, and booleans.

### Numbers

Manipulating numbers is a crucial part of web development, and programming in
general. In JS, numbers can be integers or decimals, and they look exactly like
you'd expect. Some examples:

```js
10
578
5.225
-3
0
```

### Strings

"String" is a fancy programming word for text. All the text that web apps
display and manipulate is represented by strings. Strings are delimited by
quotes in Javascript -- either single quotes or double quotes. Here are some
examples of strings:

```js
"Hello!"
'this a string'
"200"
'x'
```

### Booleans

There are only two booleans: `true` and `false`. They represent the result of
evaluating some other expression. For example, we might write code that asks
"is thing1 the same as thing2", and we'd expect to get a boolean as a response.

## Variables

In Javascript, one of the most common operations is storing some data so we can
refer back to it later. To refer back to it, we give it a name. This is called
**variable**. Here's an example:

```js
var myName = 'Jennifer';
```

The `var` part is the keyword for declaring a variable. You may have seen this before if you've ever examined any Javascript code.  Using `var` is only one way to declare a variable though.  In modern Javascript, we actually have two others: `const` and `let`.  Using these offers us some additional benefits, which you can read about [here](https://medium.freecodecamp.org/javascripts-var-let-and-const-variables-explained-with-a-story-2038e3c6b2f9).

After writing var (or const or let), we need to give our variable a name -- this can be anything we want. The name is followed by an `=`, which means "set `myName` to the string `'Jennifer'`". We can do the same with numbers or booleans:

```js
var luckyNumber = 42;
var javascriptRocks = true;
```

To *evaluate* or access a variable, we just write the name:

```js
luckyNumber
```

## Comments

We can leave little notes to ourselves in our code. These are called comments.
It's considered a good practice to leave comments for any code that might be
hard to understand. Single line comments are created with two slashes (`//`). Here's an example:

```js
// dividing 22 by 7 gives you approximately 3.14
var almostPi = 22 / 7;
```

In that example, the second line will run just like we'd expect, but the first
line won't do anything at all. It's just for our reference as developers.

We can create multiple lines of comments by surrounding them with `/* comments here */`.  In this case, the comments will wrap until the closing `*/` is reached.

Most text editors have a shortcut for adding comments. Simply select what you want to comment, then press:
- <kbd>⌘</kbd> (command key) + <kbd>/</kbd> on Mac 
- <kbd>CTRL</kbd> + <kbd>/</kbd> on Windows or Linux

## Operators

"Operators" are what we call symbols like `+` or `>` (greater than) that modify or evaluate one or more variables. For example, we can add two numbers
like this:

```js
10 + 2
```

That will evaluate to `12`. Any operators can be applied to variables as well
as directly to data types:

```js
var num1 = 10;
var num2 = 4.67;

num1 + num2
// evaluates to 14.67
```

The main mathematical operators are `+`, `-`, `*`, and `/`, for addition,
subtraction, multiplication, and division.

There are also comparison operators, like `<` (less than).

```js
num1 = 5;
num2 = 3;

num1 < num2
// evaluates to false
```

We can also test if two values are equal, with `===`:

```js
9 * 9 === 81
// evalutes to true
```

We can save the result of an operation to a variable:

```js
var seconds = 2400;
var secondsPerMinute = 60;

var minutes = seconds / secondsPerMinute;

minutes
// evaluates to 40
```

The `+` and `-` operators can be applied to strings, too:

```js
var firstName = 'John';
var lastName = 'Smith';

firstName + lastName;
// evaluates to "JohnSmith"

firstName + " " + lastName;
// evaluates to "John Smith"
```

## Functions

Functions are basically small bits of code that we can use multiple times.
There's a lot of complexity to functions in JS, so we'll only scratch the
surface here.

We can define a function like this:
```js
function sayHello() {
  var name = "Jennifer";
  return "Hi, my name is " + name;
}
```
We *invoke* the function by calling its name followed by the `()`.

```js
var myName = sayHello();

/* The variable myName now holds the value: "Hi, my name is Jennifer" */

```


Sometimes, we want to put dynamic data into our functions. These are called
arguments. We can do that like this:

```js
function sayHello(salutation, name) {
  return salutation + "My name is " + name + ".";
}
```
Let's see how we can use the arguments:

This time when we call the function, we're going to pass it two values.  The first is the `salutation`, while the second is what will be used for the `name`.  We just have to pass them into the function in the order it is expecting them and the function will handle the rest.

```js
var greeting = sayHello('Hey there!', 'Jen');

console.log(greeting); // This will output: "Hey there! My name is Jen." 

```


