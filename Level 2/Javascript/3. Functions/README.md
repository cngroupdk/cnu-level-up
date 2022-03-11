# Javascript: Functions

In programming, we often use code to perform a specific task multiple times. Instead of rewriting the same code, we can group a block of code together and associate it with one task, then we can reuse that block of code whenever we need to perform the task again. We achieve this by creating a `function`. A function is a reusable block of code that groups together a sequence of statements to perform a specific task.

```js
function greetWorld() {
  console.log('Hello, World!');
}

greetWorld(); // Print: Hello, World!
```

## Function Declarations

In this lesson, you will learn how to create and use functions, and how they can be used to create clearer and more concise code. Check the links below:

- [Function Declarations](https://www.codecademy.com/courses/introduction-to-javascript/lessons/functions/exercises/function-declaration)

> ```js
> function greetEveryone() {
>   console.log('Hello World!');
> }
> ```

- [Calling a Function](https://www.codecademy.com/courses/introduction-to-javascript/lessons/functions/exercises/functions)

> ```js
> greetEveryone();
> ```

- [Parameters and Arguments](https://www.codecademy.com/courses/introduction-to-javascript/lessons/functions/exercises/parameters)

> ```js
> function getCurrentDay(day) {
>   console.log(`Today is ${day}!`);
> }
> ```

- [Default Parameters](https://www.codecademy.com/courses/introduction-to-javascript/lessons/functions/exercises/default-parameters)

> ```js
> function getCurrentDay(day = 'Sunday') {
>   console.log(`Today is ${day}!`);
> }
> ```

- [Return](https://www.codecademy.com/courses/introduction-to-javascript/lessons/functions/exercises/return)

> ```js
> function plantNeedsWater(day) {
>   if (day === 'Wednesday') {
>     return true;
>   } else {
>     return false;
>   }
> }
> ```

- [Helper Functions](https://www.codecademy.com/courses/introduction-to-javascript/lessons/functions/exercises/return-ii)

## Function Expressions

- [Function Expressions](https://www.codecademy.com/courses/introduction-to-javascript/lessons/functions/exercises/function-expressions)

```js
const plantNeedsWater = function (day) {
  if (day === 'Wednesday') {
    return true;
  } else {
    return false;
  }
};
```

## Arrow Functions

- [Arrow Functions](https://www.codecademy.com/courses/introduction-to-javascript/lessons/functions/exercises/arrow-functions)

```js
const plantNeedsWater = (day) => {
  if (day === 'Wednesday') {
    return true;
  } else {
    return false;
  }
};
```

### Concise Body Arrow Functions

```js
const plantNeedsWater1 = (day) => {
  if (day === 'Wednesday') {
    return true;
  } else {
    return false;
  }
};

const plantNeedsWater2 = (day) => {
  return day === 'Wednesday' ? true : false;
};

const plantNeedsWater3 = (day) => day === 'Wednesday';
```
