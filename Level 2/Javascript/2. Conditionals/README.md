# Javascript: Conditionals

We’ll be covering the following concepts:

- `if`, `else` statements
- truthy vs falsy values
- comparison operators
- logical operators
- ternary operators

## `if-else` statement

In programming, we can perform a task based on a condition using an if statement:

```js
if (true) {
  console.log('This message will print!');
} else {
  console.log('This message will NOT print!');
}
// Prints: This message will print!
```

Inside the parentheses `()`, a condition is provided that evaluates to `true` or `false`.
If the condition evaluates to `true`, the code inside the curly braces `{}` runs, or executes.
The code inside the `else` statement code block will execute when the `if` statement’s condition evaluates to `false`.

## Truthy and Falsy

In JavaScript, values evaluate to `true` or `false` when evaluated as Booleans.

- Values that evaluate to `true` are known as _truthy_
- Values that evaluate to `false` are known as _falsy_

_Falsy_ values include `false`, `0`, empty strings, `null`, `undefined`, and `NaN`. All other values are _truthy_.

## Comparison Operators

Here is a list of some handy comparison operators and their syntax:

- Less than: `<`
- Greater than: `>`
- Less than or equal to: `<=`
- Greater than or equal to: `>=`
- Is equal to: `===`
- Is not equal to: `!==`

Comparison operators compare the value on the left with the value on the right. For instance:

```js
10 < 12; // true
'apples' === 'oranges'; // false
```

> **Q: Whats the different between two (`==`) and three (`===`) equal signs?** <br/>
> A: `===` is known as Identity or strict equality, meaning that the data types also must be equal:
>
> ```js
> 1 == '1'; // true
> 1 === '1'; // false
> ```
>
> **Pro Tip:** Avoid `==` and rather use `===` (unless you really know what you're doing.)
>
> If you're still curious check this [article](https://codeburst.io/javascript-double-equals-vs-triple-equals-61d4ce5a121a).

## Logical Operator AND `&&`, OR `||`, NOT `!`

We can use logical operators to add more sophisticated logic to our conditionals. There are three logical operators:

- the and operator `&&`
- the or operator `||`
- the not operator `!`

The logical OR operator `||` checks two values and returns a `boolean`. If one or both values are truthy, it returns `true`. If both values are falsy, it returns `false`.

```js
true || false; // true
10 > 5 || 10 > 20; // true
false || false; // false
10 > 100 || 10 > 20; // false
```

## Ternary Operator

The ternary operator allows for a compact syntax in the case of binary (choosing between two choices) decisions. It accepts a condition followed by a `?` operator, and then two expressions separated by a `:`. If the condition evaluates to _truthy_, the first expression is executed, otherwise, the second expression is executed.

```js
const day = 'Monday';

const price = day === 'Sunday' ? 9 : 12; // 12
```

# Exercises

- [Mathematical operations](https://www.codewars.com/kata/57356c55867b9b7a60000bd7/train/javascript)
- [Grade book](https://www.codewars.com/kata/55cbd4ba903825f7970000f5/train/javascript)
