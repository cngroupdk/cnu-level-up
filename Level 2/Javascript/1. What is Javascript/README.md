# What is JavaScript?

Let's start from the beginning and take a look at the `Javascript`. In this section you will learn some of the basic concepts and go through the topics listed below. At the end there are some exercises for you.

**Table of content:**

- Theory:
  - [1. Javascript](#javascript)
  - [2. Console](#console)
  - [3. Comments](#comments)
  - [4. Data Types](#data-types)
  - [5. Arithmetic Operators](#arithmetic-operators)
  - [6. String Concatenation](#string-concatenation)
  - [7. Properties](#properties)
  - [8. Methods](#methods)
  - [9. Built-in Objects](#built-in-objects)
  - [10. Review](#review)
- [Exercises](#exercises)

## Javascript

`JavaScript` is primarily known as the language of most modern web browsers, and its early quirks gave it a bit of a bad reputation. However, the language has continued to evolve and improve.

> JavaScript is a programming language that powers the dynamic behavior on most websites. Alongside HTML and CSS, it is a core technology that makes the web run.

## Console

The `console` is a panel that displays important messages, like errors, for developers. Much of the work the computer does with our code is invisible to us by default. If we want to see things appear on our screen, we can print, or log, to our console directly.

In JavaScript, the console keyword refers to an object, a collection of data and actions, that we can use in our code. Keywords are words that are built into the JavaScript language, so the computer will recognize them and treats them specially.

One action, or method, that is built into the `console` object is the `.log()` method. When we write `console.log()` what we put inside the parentheses will get printed, or logged, to the console.

It’s going to be very useful for us to print values to the console, so we can see the work that we’re doing.

```js
console.log('Hello CNU!');
```

This example logs `Hello CNU!` to the console. The semicolon denotes the end of the line, or statement. Although in JavaScript your code will usually run as intended without a semicolon, we recommend learning the habit of ending each statement with a semicolon so you never leave one out in the few instances when they are required.

## Comments

As we write JavaScript, we can write `comments` in our code that the computer will ignore as our program runs. These comments exist just for human readers.

Comments can explain what the code is doing, leave instructions for developers using the code, or add any other useful annotations.

There are two types of code comments in JavaScript:

1. `single line comment` will comment out a single line and is denoted with two forward slashes `//` preceding it.

```js
// Print greeting
console.log('Hello Human');
console.log('Hello E.T.'); // Greeting for alien
```

2. `multi-line comment` will comment out multiple lines and is denoted with `/*` to begin the comment, and `*/` to end the comment.

```js
/*
This is all commented 
console.log('Hello Human');
None of this is going to run!
console.log('Hello E.T.'); 
*/
```

You can also use this syntax to comment something out in the middle of a line of code:

```js
console.log(/*IGNORED!*/ 5); // Still just prints 5
```

## Data Types

Data types are how data in programming is classified. In JavaScript, there are eight fundamental data types:

- `number` Any number, including numbers with decimals
  ```js
   1, -2, 99, 3.14.
  ```
- `string` Any grouping of characters on your keyboard (letters, numbers, spaces, symbols, etc.) surrounded by single quotes `''` or double quotes `""`.
  ```js
  'single quotes';
  'double quotes';
  ```
- `boolean` This data type only has two possible values — either `true` or `false`.
  ```js
  true;
  false;
  ```
- `null` This data type represents the intentional absence of a value, and is represented by the keyword `null`.
  ```js
  null;
  ```
- `undefined` This data type is denoted by the keyword `undefined`. It also represents the absence of a value though it has a different use than `null`.
  ```js
  undefined;
  ```
- `symbol` A newer feature to the language, symbols are unique identifiers, useful in more complex coding. No need to worry about these for now.
- `object` Collections of related data.
  ```js
  {
      name: "Alice",
      age: 25,
      isStudent: true,
  }
  ```

## Arithmetic Operators

Basic arithmetic often comes in handy when programming.

An operator is a character that performs a task in our code. JavaScript has several built-in arithmetic operators, that allow us to perform mathematical calculations on numbers. These include the following operators and their corresponding symbols:

- Add: `+`
- Subtract: `-`
- Multiply: `*`
- Divide: `/`
- Modulo: `%`

The first four work how you might guess:

```js
console.log(3 + 4); // Prints 7
console.log(5 - 1); // Prints 4
console.log(4 * 2); // Prints 8
console.log(9 / 3); // Prints 3
```

## String Concatenation

Operators aren’t just for numbers! When a + operator is used on two strings, it appends the right string to the left string:

```js
console.log('hi' + 'ya'); // Prints 'hiya'
console.log('I love to ' + 'code.'); // Prints 'I love to code.'
console.log('One' + ', ' + 'two' + ', ' + 'three!'); // Prints 'One, two, three!'
```

## Properties

When you introduce a new piece of data into a JavaScript program, the browser saves it as an instance of the data type. Every string instance has a property called `length` that stores the number of characters in that string. You can retrieve property information by appending the string with a period and the property name:

```js
console.log('CN Group'.length); // Prints 8
```

The `.` is another operator! We call it the `dot operator`.

## Methods

Remember that methods are actions we can perform. JavaScript provides a number of string methods.

We _call_, or use, these methods by appending an instance with:

- a period (the dot operator)
- the name of the method
- opening and closing parentheses

`E.g. 'example string'.methodName().`

Does that syntax look a little familiar? When we use `console.log()` we’re calling the `.log()` method on the `console` object.

```js
'hello'.toUpperCase(); // returns 'HELLO'
'Ahoy'.startsWith('A'); // returns true
```

## Built-in Objects

In addition to `console`, there are other [objects built into JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects). Down the line, you’ll build your own objects, but for now these “built-in” objects are full of useful functionality.

For example, if you wanted to perform more complex mathematical operations than arithmetic, JavaScript has the built-in `Math` object.

The great thing about objects is that they have methods! Let’s call the `.random()` method from the built-in Math object:

```js
console.log(Math.random()); // Prints a random number between 0 and 1
```

The example above will likely evaluate to a decimal. To ensure the answer is a whole number, we can take advantage of another useful Math method called Math.floor().

Math.floor() takes a decimal number, and rounds down to the nearest whole number. You can use Math.floor() to round down a random number like this:

```js
Math.floor(Math.random() * 50);
```

The most commonly used are: `Math`, `Number`, `Date`, `String`, `RegExp`, `JSON`, `Promise` and more. Don't get too worried, you don't need to know them by heart.
If you would need some specific build-in object check [Official documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects).

## Review

Let’s take one more glance at the concepts we just learned:

- Data is printed, or logged, to the console, a panel that displays messages, with `console.log()`.
- We can write single-line comments with `//` and multi-line comments between `/*` and `*/`.
- There are 7 fundamental data types in JavaScript: `strings`, `numbers`, `booleans`, `null`, `undefined`, `symbol`, and `object`.
- `Numbers` are any number without quotes: `23.8879`
- `Strings` are characters wrapped in single or double quotes: `'Sample String'`
- The built-in `arithmetic operators` include `+`, `-`, `*`, `/`, and `%`.
- `Objects`, including instances of data types, can have properties, stored information. The properties are denoted with a `.` after the name of the object, for example: `'Hello'.length`.
- `Objects`, including instances of data types, can have methods which perform actions. Methods are called by appending the object or instance with a period, the method name, and parentheses. For example: `'hello'.toUpperCase()`.
- We can access properties and methods by using the `.`, dot operator.
- `Built-in objects`, including `Math`, are collections of methods and properties that JavaScript provides.

# Exercises

In `exercises` folder you will find `html` file which you will use as place where to practice the topics you just learned. To do so open this file in the browser of your choice and open the `JavaScript Console`.

1. [small exercise](./exercises/task.html)
