# Javascript: Scopes and variables

## Scopes

An important idea in programming is scope. Scope defines where variables can be accessed or referenced. While some variables can be accessed from anywhere within a program, other variables may only be available in a specific context.

To really understand this concept check the links below:

- [Global Scope](https://www.codecademy.com/courses/introduction-to-javascript/lessons/scope/exercises/global-scope)
- [Block Scope](https://www.codecademy.com/courses/introduction-to-javascript/lessons/scope/exercises/block-scope)

In this lesson, you learned about scope and how it impacts the accessibility of different variables.

Let’s review the following terms:

- **Scope** is the idea in programming that some variables are accessible/inaccessible from other parts of the program.
- **Blocks** are statements that exist within curly braces `{}`.
- **Global** scope refers to the context within which variables are accessible to every part of the program.
- **Global variables** are variables that exist within global scope.
- **Block scope** refers to the context within which variables are accessible only within the block they are defined.
- **Local variables** are variables that exist within block scope.
- **Global namespace** is the space in our code that contains globally scoped information.
- **Scope pollution** is when too many variables exist in a namespace or variable names are reused.

As you continue your coding journey, remember to use best practices when declaring your variables! Scoping your variables tightly will ensure that your code has clean, organized, and modular logic.

## Variables

There are multiple ways to define a variable in JavaScript. Let's take a look at the difference between `let` and `const`.

### `let` keyword

The first time you define a variable, you have to prefix it with `let = `. Let's take an example:

```js
let name = 'Sam';
console.log(name);
```

This defines a variable called name with a value of `"Sam"`. The next time you'd like to use that variable, you reference it by its `name` (you only use the let keyword for declaration).

Variables defined with `let`, can be **re-assigned** later on:

```js
let language = 'C++';
language = 'JavaScript';
```

**Sources:**

- [egghead.io](https://egghead.io/lessons/javascript-the-let-keyword-in-es6)
- [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)

### `const` keyword

Variables defined with const cannot be re-assigned. This means you can use the = sign once when the variable is defined. Here's an example:

```js
const language = 'C++'; // Cannot be re-assigned anymore
console.log(language); // "C++"

language = 'Python'; // ❌ Type error: this will break your script
```

> An important note about `const` is that it does NOT create a Constant or an Immutable value. This will be thoroughly explained once we learn about arrays & objects. What you need to know, for now, is that you can only use the equal sign once, but you can still change elements inside an array or object.

### `var` keyword

When you're browsing the Internet for documentation, or Questions & Answers on StackOverflow, you will see a lot of code snippets using `var` instead of `let` & `const`.
Even though `var` still works, its usage is discouraged as it may be confusing in a lot of scenarios. So you can simply replace `var` with `let` (or `const` if the variable is not being reassigned).

Reason why we don't recommend using `var`, is because variables declared with `var` keyword are belong to **global scope**. This might cause some unexpected behaviors because the way Javascript acts behind the scene.

Before your JavaScript executes, the JavaScript engine will compile your code before it interprets it. Part of this compilation is to find all the variable declarations. It defines those declarations and associated them with their appropriate scopes. This is called `hoisting`.

What do you think will happen in this code snippet?

```js
var greeting = 'Hello';

var greet = function () {
  alert(greeting);

  var greeting = 'Ahoy';
};

greet();
```

If you are not sure, check [Hoisting Explained Video](https://egghead.io/lessons/javascript-hoisting-in-javascript).

> **Pro tip:** Avoid using `var` when defining variables. Use `let` or `const` instead.
