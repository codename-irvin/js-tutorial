# JS Tutorial: Part 2 - Transforming Data

Ok, so we know that the primary goal of a computer program is to transform data and we know how to store data in our JavaScript programs. But how do we *actually* transform our data?

## Mathematical Functions

In mathematics, we have a concept called a function. I won't provide a rigorous definition of a function since it isn't essential for learning to program. `For now, we'll just say that a function is *something* that takes an input and produces an output.`

In JavaScript, that might look something like this:

```javascript
let x = add(9, 4);
x === 13; // true
```
In this example, we invoke a function called `add` with the inputs `9` and `4`. We then store the output of the function call in the variable `x`. Clearly, the value of `x` should be `13`.

In mathematics, we typically just define a function by its inputs and outputs. For example, we might say something like "The function `add` takes two real numbers as input and produces a real number as output such that the output is the sum of the two inputs." The mathematician doesn't concern themselves with *how* the output of a function is computed from its inputs. 

Unfortunately, since we are not mathemeticians, we don't have the same luxury.

## JavaScript Functions

Fortunately, JavaScript (and most every programming language) gives us the concept of a function! A JavaScript function has many similarities to a mathematical function. It usually (but not always) will take inputs and produce outputs. The primary difference is that, in JavaScript, we need to actually tell the computer exactly *how* the inputs map to the outputs.

Let's take a look at how our `add` function from the previous section might be implemented in JavaScript.

```javascript
function add(x, y) {
    return x + y;
}

let x = add(9, 4);
x === 13; // true
```

The first three lines of this example define a function called `add`. The function takes two inputs `x` and `y`. Everything inside of the curly braces `{}` is part of the function *body*. In this case, that's just `return x + y;`.

This function is very simple - in fact it doesn't really need to exist:

```javascript
let x = 9 + 4;
x === 13; // true
```

Most functions will have bodies that are much more complex than our simple `add` function.

In a real codebase, we would define dozens or hundreds of different functions to do various transformations on our data. This could include things like sorting lists, computing statistics, rendering 3D data to a monitor, detecting collisions between objects in a video game, etc. Additionally, we may bring in third-party packages and frameworks and call functions that they provide.

## Operators

In our `add` function in JavaScript, we made use of `+` to add two numbers together. But what is `+`? `+` is an operator provided by JavaScript that adds two `numbers` together (remember, `number` is a type in JavaScript). Operators are typically the most basic way to manipulate data in a programming language. Typically, a function body might make use of many different operators to perform a more complex transformation of the data.

JavaScript provides many operators that can be used to manipulate (or transform) the primitive datatypes. A complete list of the operators that JavaScript provides can be found here: https://www.w3schools.com/js/js_operators.asp.


## Example

### Prerequesite
In Part 1, we glossed over a couple of concepts. One of which was the `array` type. An array is a data type that can hold a list of items.

Here is an example:

```javascript
let names = ["Irvin", "Blister", "Crush"];
```

In this example, `names` is an array that stores 3 `string` values. However, an array can have arbitrary length and store any type of data.

## Practice

```javascript
const assert = require("node:assert");

function fullName(first, last) {
    // This function should combine first and last with a space in the middle.
}

let first = "John";
let last = "Smith";

let full = fullName(first, last);
assert.equal(full, "John Smith");
```

You can copy this code into a file like `fullname.js` and run it with `node fullname.js`.

If your code is working, you'll see nothing on the console. If it fails, you'll see something like this:

```
node:assert:126
  throw new AssertionError(obj);
  ^

AssertionError [ERR_ASSERTION]: undefined == 'John Smith'
    at Object.<anonymous> (D:\workspace\js-tutorial\fullname.js:11:8)
    at Module._compile (node:internal/modules/cjs/loader:1469:14)
    at Module._extensions..js (node:internal/modules/cjs/loader:1548:10)
    at Module.load (node:internal/modules/cjs/loader:1288:32)
    at Module._load (node:internal/modules/cjs/loader:1104:12)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:174:12)
    at node:internal/main/run_main_module:28:49 {
  generatedMessage: true,
  code: 'ERR_ASSERTION',
  actual: undefined,
  expected: 'John Smith',
  operator: '=='
}
```

Good luck!