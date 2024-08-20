# JS Tutorial: Part 1 - Data

## It's All About the Data

The fundamental purpose of a computer program is to transform data. Consider a program that takes in real estate data and attempts to predict the value (data) of a home. Or, perhaps, a video game which takes user input (data) and uses it to update the game state (data) accordingly. Another program that comes to mind is Wine. Wine takes a Windows System Call (data) as input and transforms it into a corresponding Linux System Call (data). At the end of the day, every computer program operates on data - it takes data as input and produces data as output. An `algorithm` nothing more than a description of how the data should be transformed.

## Storing Data

Since every computer program operates on data, we need a way for our program to store data. This is where `variables` come in. You can define a variable in JavaScript like this:

```javascript
let x = 9;
```

In this example, we have defined a new variable called `x` and assigned it the value of `9`. We can change the value of a variable like this:

```javascript
x = 0;
```

Now `x` is `0`! Note that we did not have to use `let` in this case. That is only required the first time that a variable is defined.

Here are some more examples of variables:

```javascript
let firstName = "John";
let lastName = "Smith";
let age = 45;
let siblings = ["Mark", "Susan", "Glen"];
```

Don't worry if you don't fully understand all of the examples - the important thing to remember is that variables are used to store data!

## Types of Data

All data has an associated type. JavaScript has the following built-in data types:

Primitive
```
null
undefined
boolean
number
string
symbol
bigint
```

Complex
```
object
array
function
```

These types can broadly be split into two groups, primitive and complex. For now we will only focus on the primitive data types. We will also ignore `symbol` and `bigint` for now as they are rarely used. We will discuss these types in more depth once the need arises.

Here are some examples of variables and their corresponding types:

```javascript
let a;          // undefined
let b = null;   // null
let c = true;   // boolean
let d = 11;     // number
let e = "hello" // string
```
The type of the data you are working with is very important because it dictates what kinds of transformations you can do on the data. In the next part, we will start to look at examples of transforming data using `operations`. But for now, to understand the importance of `types` in programming, consider this example:

```javascript
let x = 5 + 9;    // makes sense. x is 14.
let y = true + 9; // doesn't make much sense
```

Note: JavaScript is a funky language and will actually let you do `true + 9` despite the fact that it doesn't make much sense. Most programming languages will not allow for such nonsense.