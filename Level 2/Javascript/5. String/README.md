# Javascript: String

The `String` object is used to represent and manipulate a sequence of characters.

Strings are useful for holding data that can be represented in text form. Some of the most-used operations on strings are to check their `length`, to build and concatenate them using the `+` and `+=` string operators, checking for the existence or location of substrings with the `indexOf()` method, or extracting substrings with the `substring()` method.

Check the tutorials below to get deep into the topic:

- [1. Strings](https://learnjavascript.online/app.html?id=1440)
- [2. Character access](https://learnjavascript.online/app.html?id=1444)
- [3. Substring](https://learnjavascript.online/app.html?id=1447)
- [4. Template strings](https://learnjavascript.online/app.html?id=1453)

`String` object has much more build-in functionality. If you're looking for specific method, check [official documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#static_methods).

## Regular expression aka regex

In some cases you might need to match strings according to some pattern, for example if string is email. This pattern is called `regular expression`.

Javascript supports `regular expressions` through the standard class `RegExp` which is implemented natively in every modern browser.

```js
// Literal notation to match a string of alpha-numeric characters
const re = /\w+\d+/;
// Constructor notation of the same regular expression object
const regex = new RegExp('\\w+\\d+');
```

If you need to test your regex or its validity you can use the useful [site](https://regex101.com/).

### Matching string

The `RegExp` object has a number of top level methods, and to test whether a regular expression matches a specific string in Javascript, you can use `RegExp.test()`. To actually extract information from a string using a regular expression, you can instead use the `RegExp.exec()` call which provides more information about the match in its result.

```js
// Lets use a regular expression to match a date string.
const inputStr = 'June 24';
const regex = /([a-zA-Z]+) (\d+)/;

const hasMatch = regex.test(inputStr);
const matches = regex.exec(inputStr);
```

### String functions

There are also string functions to `match`, `search`, and even `replace` substrings based on a given regular expression, which can be useful and easy to use.

We can use String.search() to find the index of a particular pattern in an input string though.

```js
var inputStr = 'There are 15 cats on the bed';
// This will print 10, the index at which we find the digits
console.log(inputStr.search(/\d+/));
// If there is no such match, it returns -1
console.log(inputStr.search(/123/));
```

Lets try and replace some date strings

```js
var inputStr = 'June 24, August 9, Dec 12';
// This will print "June 1, August 1, Dec 1" since the global flag is set.
// and the match applies to all the dates
console.log(inputStr.replace(/\d+/g, '1'));
```

Lets try and reverse the order of the day and month in a date
string. Notice how the replacement string has back references to the captured groups.

```js
var inputStr = 'June 24, August 9, Dec 12';
// This will reorder the string and print:
//   24 of June, 9 of August, 12 of Dec
console.log(inputStr.replace(/(\w+) (\d+)/g, '$2 of $1'));
```

If you're are curious and want to know more about `regular expressions`, check [Regex One](https://regexone.com/references/javascript).

## Exercises

- [Remove First and Last Character](https://www.codewars.com/kata/56bc28ad5bdaeb48760009b0/train/javascript)
- [Remove String Spaces](https://www.codewars.com/kata/57eae20f5500ad98e50002c5/train/javascript)
- [Convert a string to an array](https://www.codewars.com/kata/57e76bc428d6fbc2d500036d/train/javascript)
- [Regex exercises](https://regexone.com/lesson/introduction_abcs) (optional)
