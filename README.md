# TOC
- [Javascript Basics](#javascript-basics)
- [Data Storage](#data-storage)
- [Practice Problems 2](#practice-problems-2)
- [Intermediate JavaScript Features](#intermediate-javascript-features)
- [Practice Problem 3](#practice-problem-3)
- [Class & Prototypes](#class---prototypes)
- [Binary and Hexidecimal](#binary-and-hexidecimal)
* * *
# Javascript Basics
  * [What are Programs](#what-are-programs)
  * [Intro to Javascript](#intro-to-javascript)
    + [Number Variable](#number-variable)
      - [Variables](#variables)
    + [Multiple Variables](#multiple-variables)
    + [Booleans](#booleans)
    + [Strings](#strings)
      - [Backticks](#backticks)
    + [Mutable Let](#mutable-let)
      - [Changing a Variable](#changing-a-variable)
    + [Comments](#comments)
  * [Functions and Operators](#functions-and-operators)
    + [Get Message](#get-message)
      - [Functions](#functions)
      - [Calling a Function](#calling-a-function)
      - [Function Declaration](#function-declaration)
      - [Return Statement](#return-statement)
    + [Add Two](#add-two)
      - [Parameters and Arguments](#parameters-and-arguments)
    + [Multiply](#multiply)
    + [Average](#average)
      - [Averaging Numbers](#averaging-numbers)
      - [Operator Precedence](#operator-precedence)
    + [Random](#random)
      - [Random Ranges](#random-ranges)
    + [Floor](#floor)
  * [Conditionals](#conditionals)
    + [Is Equal](#is-equal)
      - [Console Log](#console-log)
    + [Is Not Equal](#is-not-equal)
      - [Returning the Expression](#returning-the-expression)
    + [Else](#else)
      - [Boolean Conditions](#boolean-conditions)
    + [Greater Than](#greater-than)
      - [No Return Value](#no-return-value)
    + [Is Enough](#is-enough)
      - [Returning Early](#returning-early)
    + [Else If](#else-if)
      - [Closer Look](#closer-look)
  * [Loops](#loops)
    + [Summation](#summation)
      - [Real World Example](#real-world-example)
    + [Factorial](#factorial)
      - [Factorial to Loop](#factorial-to-loop)
    + [String Loops](#string-loops)
    + [Modulus Scream](#modulus-scream)
      - [Modulus in Loops](#modulus-in-loops)
    + [Top Double](#top-double)
## What are Programs

- Read line-by-line by a compiler or interpreter upon execution
- Each line is parsed and broken into tokens
- Compilers form a tree-like data structure to represent your program

```js
const a = 4
```

- tokens : `const`,`a`,`=`,`4`

* * *

## Intro to Javascript

### Number Variable

#### Variables

- Store values in variables

```js
const a = 3
```

- `const` is a keyword used to declare `a` as constant value

### Multiple Variables

- Lines of javascript are called statements and end with `;`

```js
const a = 4;
const b = a;
```

### Booleans

- a `true` or `false` value

```js
const loggedIn = false;
```

### Strings

- a bunch of characters

```js
const a = "Hello!";
```

#### Backticks

- used to interpolate or add values inside of string

```js
const helloMessage = `Hello ${anotherName}, my name is ${myName}!`;
```

- If you need to use double quotes inside of a double quote string use a backslash ()

```js
const message = "This is a double-quote \" inside double-quotes";
```

- you can use double quotes inside of single quote string

```js
const message = 'Then he said, "Wait, are you just going to stand there?"';
```

### Mutable Let

#### Changing a Variable

- constant variables or `const` are immutable; values cannot change
- using the keyword `let` allows variables to be mutable

### Comments

- lines beginning with // are excluded from the javascript compiler and can be used to add context to lines of code

```js
// this is price in U.S. Dollars
const price = 42;
```

- multi-line comments

```js
/* The price of all of our items
   Denominated in U.S. Dollars  */
const price = 42;
```

* * *

## Functions and Operators

### Get Message

#### Functions

- re-usable code
- often returns ouptut

```js
function getNumber() {
    return 4;
}
```

- code above returns `4`
- Calling the `getNumber` function

```js
const num = getNumber();
```

- value `4` would be stored in `num` variable

#### Calling a Function

- functions often require input statements

```js
const output = addOne(2);
```

- passing the input value `2`
- not all functions require input

```js
const message = getMessage();
```

#### Function Declaration

- defining a function; the function below is called `addOne`

```js
function addOne(input) {
    return input + 1;
}
```

#### Return Statement

- `return` keyword will return the desired output of the function

```js
const a = addOne(1);
```

- `a` is now assigned the return value of the `addOne` function invoked with an input of `1`

### Add Two

- functions with inputs are passed in parenthesis
- defining a function that takes input is also added in parenthesis
- `+` is reffered to as an addition operator

#### Parameters and Arguments

- both refer to the inputs supplied to a function
- multiple paraments are separated by commas and contained inside parenthesis

```js
function addNumbers(a, b) {
    return a + b;
}
// calling the addNumbers function
addNumbers(1, 2);
```

### Multiply

- multiplication operator `*`

```js
const b = a * 3;
```

### Average

- division operator `/`

#### Averaging Numbers

```js
const sum = 1 + 2 + 3;
const average = sum / 3;
// or
const average = (1 + 2 + 3) / 3;
```

#### Operator Precedence

- if operators are the same precedence (+ or - vs * or /) expression is read left to right
- parenthesis are alwasy evaluated first

```js
(5 + 1) * 2
```

### Random

- there are many math utilities on the `Math` object

```js
// Call Random Number
const myRandomNumber = Math.random();
```

- this will return some number between 0 and 1 (not including 1)

#### Random Ranges

- generating a number between 0 and 1

```js
// randomNumber will be between 0 and 100
const randomNumber = Math.random() * 100;
```

- get a random number between 25 and 100

```js
// randomNumber will be between 25 and 100
const randomNumber = (Math.random() * 75) + 25;
```

### Floor

- `Math.floor` takes arguements

```js
const two = Math.floor(2.2598223);
```

- this function will take `2.2598223` and round it down to `2` (nearest integer

* * *

## Conditionals

### Is Equal

- `if` is used when you need to branch based on a condition

```js
if(1 === 1) {
    console.log( "Yup, that's true!" );
}
```

- `===` is a strict equality operator

#### Console Log

- `console.log` will log values during the programs execution

### Is Not Equal

- `!==` or strict inequality
- evalulated as true if the two values are not equal

```js
console.log( 1 !== 2 ); // true
console.log( 2 !== 2 ); // false
console.log( 3 !== 2 ); // true
```

#### Returning the Expression

- often useful to just return the expression itself

```js
function isEqual(a, b) {
    if(a === b) {
        return true;
    }
}
//vs
function isEqual(a, b) {
    return a === b;
}
```

- the second expression will return `false` if a and b are not equal

### Else

- `else` statement runs only if the `if` condition is not `true`

```js
if(isRaining === true) {
    stayIndoors();
}
else {
    // isRaining is not true
    goOutside();
}
```

#### Boolean Conditions

```js
const a = true;

if(a === true) {
   console.log('hi!'); // hi!
}
//vs
const a = true;

if(a) {
   console.log('hi!'); // hi!
}
```

- the boolean itself is the condition upon with we are branching

### Greater Than

- greater than operator `>`
- less than operator `<`
- will evaluate to `false` if the operands are equa

```js
console.log(4 > 4); // false
console.log(4 < 4); // false
```

#### No Return Value

- if you dont return a value in a function, return will be considered `undefined`

```js
function add(a,b) {
    
}

const value = add(2,3); // undefined
```

### Is Enough

- greater than or equal to

```js
console.log(1 >= 2); // false
console.log(1 >= 1); // true

console.log(2 <= 1); // false
console.log(2 <= 2); // true
```

#### Returning Early

```js
// This Accomplishes The Same Thing
function isEqual(a,b) {
    if(a === b) {
        return true;
    }
    else {
        return false;
    }
}
// As This
function isEqual(a,b) {
    if(a === b) {
        return true;
    }
    return false;
}
```

### Else If

```js
if(firstCondition) {
    // firstCondition is true
}
else if (otherCondition) {
    // firstCondition is not true and otherCondition is true
}
else {
    // neither condition is true
}
```

#### Closer Look

- what happens if two conditions were true
- only the first condition will run
- else statements will only runid the original condition is not true

* * *

## Loops

### Summation

```js
let sum = 0;
for(let i = 1; i <= 4; i++) { 
    sum = sum + i; 
}
```

- the `i` variable will start at `1`
- it will be added to `sum`
- it will checkthe condition to see if we should continue the loop `i <= 4`
- add one to `i` using `i++`
- loop starts again with ''`i` being `2`
- example above added 1, 2 ,3, and 4 together to sum resulting in 10

#### Real World Example

- for loops can be broken down into the following

```js
for ([initialization]; [condition]; [update]) {
    statement
}
```

- `initialization` is run once at the beginning of the loop, create a varible to initialize the starting value
- `condition` is checked before each iteration. If `true` the statement will run
- `update` is run at the end of each iteration; can update a variable for the next execution of the statement; typically will increment or decrement some counter
- `++` operator means add 1 to the variable
- `+=` operator takes the right hand side and adds to the left hand side

### Factorial

- in mathematics a factorial is often denotaed with an exclamation mark '!'
- factorial is the product of all postive integers greater than 0 up to and including the factorial number 'n'

#### Factorial to Loop

- factorial '5!'
- `5 * 4 * 3 * 2 * 1`
- `*=` operator takes the right hand side and multiplies it by the left hand side

```js
function factorial(n) {
    let result = 1
    for(i = 1; i <= n; i++){
        result *= i;
    }
    return result
    
}
```

### String Loops

```js
function scream(n) {
    let str = "";
    for(let i = 1; i <= n; i++) {
       str += "a";
    }
    return str
}
```

- this will add `n` amount of `a` to `str` and return the final str

### Modulus Scream

- `%` called modulus operator and tells us the remainer of a division

```js
console.log(8 % 3) // 2
console.log(5 % 2) // 1
console.log(7 % 4) // 3
```

#### Modulus in Loops

- how many event numbers are between 1 and 11

```js
const remainder = num % 2;
const isEven = remainder === 0;
```

- `isEven` will tell us whether or not remainder is 0; when 0 the number is divisible by 2

```js
let count = 0;
for(let i = 1; i <= 11; i++) {
    const remainder = i % 2;
    const isEven = remainder === 0;
    if(isEven) {
        count++;
    }
}
console.log(count); // 5
```

### Top Double

```js
function topDouble(value, top) {
    let num = value
    for(let i = num; i <= top; i *= 2){
        num2 = i;
    }
    return num2;
}
```

- goal: find thelargest double for `value` that is below the `top`
---
# Data Storage
  * [String Manipulation](#string-manipulation)
    + [Starts With X](#starts-with-x)
      - [Comparison Strings](#comparison-strings)
    + [Starts with Casing](#starts-with-casing)
    + [Ends With X](#ends-with-x)
      - [String Length](#string-length)
    + [Is all X](#is-all-x)
      - [String Looping](#string-looping)
    + [Find First X](#find-first-x)
      - [Index Of](#index-of)
    + [Split at X](#split-at-x)
      - [Slicing Strings](#slicing-strings)
      - [Negative Arguements](#negative-arguements)
  * [Working with Arrays](#working-with-arrays)
    + [Create Array](#create-array)
    + [Has One](#has-one)
      - [Return Early](#return-early)
    + [Sum Even](#sum-even)
      - [Running Value](#running-value)
    + [Unique](#unique)
      - [Return a New Array](#return-a-new-array)
      - [Contains Element](#contains-element)
    + [Add One](#add-one)
      - [Modifying Array Values](#modifying-array-values)
      - [Reference](#reference)
    + [Remove Occurences](#remove-occurences)
      - [Modifying the Array](#modifying-the-array)
      - [Splice Index](#splice-index)
  * [Objects](#objects)
    + [Pizza Order](#pizza-order)
      - [Objects](#objects-1)
    + [How Many PIzzas](#how-many-pizzas)
      - [Retrieve Values](#retrieve-values)
    + [Many Orders](#many-orders)
      - [Array of Objects](#array-of-objects)
    + [Typed Orders](#typed-orders)
      - [Enumerated Types](#enumerated-types)
    + [Add By Type](#add-by-type)
      - [Importing Files](#importing-files)
    + [Object Keys](#object-keys)
      - [Find the Number of Keys](#find-the-number-of-keys)
    + [Secret Key](#secret-key)
      - [Edit Object Values](#edit-object-values)
## String Manipulation
### Starts With X
- you can lookup chracters in string by index
- there are two ways to do this
```js
"Hello".charAt(1); // e
"Hello"[1]; // e
```
#### Comparison Strings
- Can use comparison operators `====`,`<`, and `>`
- Can do case sensitive comparisons as well as whitespaces
```js
console.log( 'a' === 'a' ); // true
console.log( 'a' === 'A' ); // false
console.log( 'a' === 'a ' ); // false
```
- can use `<` and `>` to determine if a string comes before another
```js
console.log( 'a' > 'b' ); // false
console.log( 'a' < 'b' ); // true
console.log( 'abc' < 'apple' ); // true
```
### Starts with Casing
- manitpulate string casing
```js
console.log( "Hello".toLowerCase() );// hello
console.log( "Hello".toUpperCase() ); // HELLO

console.log( "Hello".toUpperCase() === "HELLO" ); // true
console.log( "Hello".toLowerCase() === "hello" ); // true
```
### Ends With X
#### String Length
- look up how many characters are stored in a string by accessing the property
```js
console.log( "a".length ); // 1
console.log( "Hello".length ); // 5
```
- length value is 1 greater that last character index
### Is all X
#### String Looping
```js
function isAllX(string) {
    let x = "";
    let str = "";
    for (let i = 0; i < string.length; i++) {
        str += string[i].toLowerCase();
        x += "x";
    }
    if(str === x){
        return true
    }
    else{
        return false
    }
}
```
### Find First X
#### Index Of
- Method `indexOf` to find index of string
```js
function findFirstX(string) {
    indx = string.indexOf("x")
    return indx
    
}
```
- if index not found `indexOf` returns `-1`
- `lastIndexOf` function finds the last occurrence of the string and returns its index
### Split at X
#### Slicing Strings
- `slice` allos for the passing of parameters: start index and end index
-  the result will be a sliced string between those two characters now inlcuding the end index
-  if last index is not provided, slice will continue until the end of the string
```js
function splitAtX(string) {
    xIndex = string.indexOf("x");

    afterX = xIndex + 1;

    firstHalf = string.slice(0,xIndex);
    secondHalf = string.slice(afterX);

    if(firstHalf.length > secondHalf.length){
        return firstHalf;
    }
    else{
        return secondHalf;
    }

}
```
#### Negative Arguements
- use negative arguements to slice starting fomr the end
- with out a second arguement this will return the rest of the string
- with second arguement specify at what point the string wil be sliced
 ```js
"the apple".slice(-5); // apple
"the apple".slice(-5, -2); // app
```
## Working with Arrays
### Create Array
- start with open squar bracket and ends with closed square bracket
- elements are separated by column
```js
const numbers = [1, 2, 3, 4, 5];
const booleans = [true, false, true, true];
const strings = ["happy", "go", "lucky"];
```
- arrays can be stored in arrays
```js
const nested = [[1, 2, [1, 2]], 2];
```
### Has One
- retrive elements in array
```js
const element = array[0];
```
- length method returns number of elements in array
#### Return Early
```js
function lessThanTen(array) {
    for(let i = 0; i < array.length; i++) {
        if(array[i] >= 10) {
            return false;
        } 
    }
    return true;
}
```
- check for the opposite of the thing you want, and return early to end the function when that’s the case
- reduces nested if statements
```js
function handleClick (event) {

	// Make sure clicked element has the .save-data class
	if (!event.target.matches('.save-data')) return;

	// Get the value of the [data-id] attribute
	let id = event.target.getAttribute('data-id');
	if (!id) return;

	// Get the user token from localStorage
	let token = localStorage.getItem('token');
	if (!token) return;

	// Save the ID to localStorage
	localStorage.setItem(`${token}_${id}`, true);

}
```
### Sum Even
#### Running Value
- keep running values
- average function will loop over the array and keeyp a running total of the values
```js
function average(array) {
    let total = 0;
    for(let i = 0; i < array.length; i++) {
        total += array[i];
    }
    return (total / array.length);
}

const result = average([80,90,98,100]); 
console.log( result ); // 92
```
### Unique
#### Return a New Array
- can create a new array and push elements from original filtered array
```js
function greaterThanFive(array) {
    const newArray = [];
    for(let i = 0; i < array.length; i++) {
        const element = array[i];
        // is this element greater than 5?
        if(element > 5) {
            // yes, push this element on our array
            newArray.push(element);
        }
    }
    return newArray;
}
```
#### Contains Element
- use `indexOf`
```js
const element = 3;
const array = [1,2,3];

const isContained = array.indexOf(element) >= 0;

console.log( isContained ); // true
```
- if array does not contain an element `indexOf` will return `-1`
```js
function unique(array) {
    const newArray = [];
    for(let i = 0; i < array.length; i++){
        const element =  array[i]
        if(newArray.indexOf(element) < 0){
            newArray.push(element)
        }
    }
    return
}
```
### Add One
#### Modifying Array Values
- write new values to positions in array using `=` assignment operator
```js
const array = [1,2,3];
array[0] = 5;
console.log(array); // [5,2,3]
```
#### Reference
- when storing an object to variable with are storing a reference to the object
- with primities values, values are simplied copied
```js
let a = 3;
let b = a;

a = 10;
console.log(a); // 10
console.log(b); // 3
```
- with objects values are assigned by reference
```js
let a = [1,2,3];
let b = a;

a[0] = 5;
console.log(a); // [5,2,3]
console.log(b); // [5,2,3]
```

- `const` will stop from changing the reference
```js
// GOOD
const arr = [1,2,3];
arr[0] = 5;
// BAD
const arr = [1,2,3];
arr = [5,6,7];
```
- `BAD` will throw a type error
### Remove Occurences
#### Modifying the Array
- `splice` uses two arguments
- first is the starting index; the start the removal of elements
- second is the number elements to be removed
```js
function greaterThanFive(array) {
    for(let i = array.length - 1; i >= 0; i--) {
        if(array[i] <= 5) {
            array.splice(i, 1);
        }
    }
}
```
#### Splice Index
- counting forward can cause loop condition and array index mismatchs
- remedy this by counting backwards in for lops
```js
const array = [1,2,3];
for(let i = array.length - 1; i >= 0; i--) {
    if(array[i] > 1) {
        array.splice(i, 1);
    }
}
console.log(array); // [1]
```
- remove occurences in array equal to num
```js
function removeOccurrences(array, num) {
    for (i = array.length - 1; i >= 0 ;i--){
        if(array[i] === num){
            array.splice(i,1);
        }
    }
    
}
```
## Objects
- object initializer syntax starts with `{` and ends with `}` with key value pairs in the middle
```js
const person = {
    hairColor: 'brown',
    toes: 10,
    grumpy: true
}
```
- values can be retrieved using the following
```js
console.log( person.toes ); // 10
console.log( person['hairColor'] ); // brown
```
### Pizza Order
#### Objects
```js
const order = {
    pizzas: 2,
    extraCheese: false,
    deliveryInstructions: "my house",
}
```
### How Many PIzzas
#### Retrieve Values
```js
const order = {
    pizzas: 3,
    extraCheese: true,
    deliveryInstructions: "Round the back, please!",
};

function numberOfPizzas(order) {
    return order.pizzas
    
}
```
### Many Orders
#### Array of Objects
```js
const orders = [
    { pizzas: 3 },
    { pizzas: 5 },
    { pizzas: 10 }
];

function numberOfPizzas(orders) {
    numPizzas = 0
    for(let i = 0; i < orders.length; i++){
        numPizzas += orders[i].pizzas
    }
    return numPizzas
}
```
### Typed Orders
#### Enumerated Types
- code us more readable and maintainable when numbers are defined
```js
const card = {
    suit: 1,
    value: 5
}
//VS
const CARD_SUITS = {
    DIAMONDS: 0,
    HEARTS: 1,
    SPADES: 2,
    CLUBS: 3
}
const card = {
    suit: CARD_SUITS.HEARTS,
    value: 5
}
```
- the value of `suit` would still be one however this clearly defines what the suit means
- this type of object is commonly referred to as an enumeration
- as with any predefined constant its common to use UPPER_SNAKE_CASE for enumerations in javascript
### Add By Type
#### Importing Files
- can use `require` to pull in exports
```js
const ORDER_TYPES = require('./orderTypes');

const orders = [
    { pizzas: 3, type: ORDER_TYPES.PIZZA },
    { wings: 12, type: ORDER_TYPES.WINGS },
];

function numberOfPizzas(orders) {
    numPizzas = 0;
    for(let i = 0; i < orders.length; i++){
        if (orders[i].type === ORDER_TYPES.PIZZA){
            numPizzas += orders[i].pizzas;
        }
    }
    return numPizzas
}

```
### Object Keys
#### Find the Number of Keys
- wasy to get all keys from an object
- `in` operator to iterate over all properties
```js
const object = { a: 1, b: 2, c: 3 } 
for(let key in object) {
    console.log(key);
}
```
- or use the object constructor
```js
const object = { a: 1, b: 2, c: 3 } 
console.log( Object.keys(object) ); // ['a', 'b', 'c']
console.log( Object.values(object) ); // [1, 2, 3]
```
### Secret Key
#### Edit Object Values
- editing values in objects is similar syntax to retrieving values
```js
const person = {
    name: "James",
    age: 22
}

person.name = "Sally";
person["age"] = 30;

console.log( person.name ); // Sally
console.log( person.age ); // 30
```
- remove keys completely
```js
const person = { 
    name: "Bob"
}

delete person.name;

console.log( person.name ); // undefined
```

---
# Practice Problems 2
  * [Shortest String](#shortest-string)
  * [Half Value](#half-value)
  * [Count C](#count-c)
  * [Count Vowels](#count-vowels)
  * [Reverse](#reverse)
  * [Palindrome](#palindrome)
  * [Sum Together](#sum-together)
  * [Count the Elements](#count-the-elements)
  * [Player Hand Score](#player-hand-score)
## Shortest String
```js
function shortestString(str1, str2) {
    if(str1.length > str2.length){
        return str2
    }
    else{
        return str1
    }

}
```
## Half Value
```js
function halfValue(numbers) {
    const newArray = [];
    for(let i = 0; i < numbers.length; i++){
        remainder = numbers[i] % 2;
        isEven = remainder === 0;
        if(isEven){
            newArray.push(numbers[i] / 2);
        }
        else{
            newArray.push(Math.ceil(numbers[i] / 2));
        }
    }
    return newArray
}
```
## Count C
```js
function countC(str) {
    const lowerStr = str.toLowerCase();
    let count = 0;
    for(let i = 0; i < str.length; i++){
        if(lowerStr[i] === "c"){
            count++;
        }
    }
    return count;
}
```
## Count Vowels
```js
function countVowels(str) {
    const lowerStr = str.toLowerCase()
    let count = 0
    const vowles = ['a','e','i','o','u']
    for(let i = 0; i < lowerStr.length; i++){
        let hit = vowles.indexOf(lowerStr[i]) !== -1
        if(hit){
            count++
        }
    }
    return count

}
```
## Reverse
```js
function reverse(string) {
    strBack = ""
    for(let i = string.length - 1; i >= 0; i--){
        strBack += string[i]
    }
    return strBack
}
```
## Palindrome
```js
function isPalindrome(string) {
    strBack = "";
    for(let i = string.length - 1; i >= 0; i--){
        strBack += string[i];
    }
    if(strBack === string){
        return true;
    }
    else{
        return false;
    }

}
```
## Sum Together
```js
function sumTogether(arr1, arr2) {
    sumArray = [];
    for(let i = 0; i < arr1.length; i++){
        sumArray.push(arr1[i] + arr2[i]);
    }
    return sumArray;
}
```
## Count the Elements
```js
function countElements(elements) {
    let charCount = {}
    for(let i = 0; i < elements.length; i++){
        if(charCount[elements[i]] >= 1){
            charCount[elements[i]]++;
        }
        else{
            charCount[elements[i]] = 1
        }
    }
    return charCount
}
```
## Player Hand Score
```js
const CARD_POINTS = {
    K: 4,
    Q: 3,
    J: 2,
}
function playerHandScore(hand) {
    let score = 0
    for(let i = 0; i < hand.length; i++){
        score += CARD_POINTS[hand[i]]
    }
    return score
}
```

---
# Intermediate JavaScript Features
  * [Logical Operators](#logical-operators)
    + [Or Operator](#or-operator)
      - [Logical OR](#logical-or)
    + [Default Operator](#default-operator)
      - [Truthy and Falsey](#truthy-and-falsey)
    + [AND Operator](#and-operator)
    + [Guard Operator](#guard-operator)
    + [NOT Operator](#not-operator)
  * [Exceptions](#exceptions)
    + [Throw an Error](#throw-an-error)
      - [Throwing Errors](#throwing-errors)
    + [Catch an Error](#catch-an-error)
    + [Return Error](#return-error)
      - [Catch and Return](#catch-and-return)
    + [Start an Error](#start-an-error)
      - [Type Error](#type-error)
      - [Reference Error](#reference-error)
      - [Syntax Error](#syntax-error)
      - [Range Error](#range-error)
  * [Type Conversion](#type-conversion)
    + [String to Number](#string-to-number)
      - [ParseInt and ParseFloat](#parseint-and-parsefloat)
      - [TypeOf](#typeof)
    + [To String](#to-string)
    + [Is Truthy](#is-truthy)
      - [Not Not](#not-not)
    + [Loose Equals](#loose-equals)
    + [Object to JSON](#object-to-json)
    + [Valid JSON](#valid-json)
  * [Destructuring, Rest, and Spread](#destructuring--rest--and-spread)
    + [Destructuring](#destructuring)
    + [Rest Parameters](#rest-parameters)
    + [Spread Arguements](#spread-arguements)
      - [Wrap Up](#wrap-up)
## Logical Operators
- in english we use **OR** in JavaScript we use `||`
- **AND** is set with `&&` as well as **NOT** is set with `!`
### Or Operator
#### Logical OR
- its good to **DRY** you code which stands for **DONT REPEAT YOURSELF**
```js
if(car || motorcycle || truck) {
    driveToAirport();
}
```
### Default Operator
- `||` is sometimes referred to as the default operator do to its behavior with truthey and falsey values
```js
console.log("" || "Something Else"); // Something Else
```
- here the empty string is falsey so `||` witll take the second value in this operation
- can be used to create a default message if one is not defined
```js
const message = WELCOME_MESSAGE || "Hello there!";
```
- if `user.age` is undefined or 0 it will default to `99`
```js
const age = user.age || 99;
```
#### Truthy and Falsey
- values are considered truthy if they behave like true when used with logical operators
```js
console.log(true || false); // true
console.log(false || true); // true
```
- false values include ```false```, `0`, `""`, `null`, `undefined`, and `NaN`
### AND Operator
- ``&&``
- both values must be true for the expression to evaluate as true
```js
console.log(true && true); // true
console.log(true && false); // false
console.log(false && true); // false
console.log(false && false); // false
```
### Guard Operator
- `||` is the "Logical OR" or the default operator
- `&&` is the "Logical AND" or the guard operator
- use `&&` to guard against run-time exceptions or erros when dealing with falsey values
```js
const user = { name: 'bob' }
console.log(user && user.name); // bob

const user2 = undefined;
console.log(user2 && user2.name); // undefined
```
- first example successfully retrieved the user's name
- the second returns undefined
### NOT Operator
- `!`
- the NOT operator will flip true and false
```js
console.log(!true); // false
console.log(!false); // true
```
- will also flip truthy and falsey values
```js
console.log(!2); // false
console.log(!undefined); // true
```
- `!!2` will equal `2`
## Exceptions
- an exception is an unexpected error in some function
- an thrown error stop execution in the current function and goes back to the function that called it
- a function can choose to catch a the exception and handle it
- if it doesnt catch it the exception will continue to be thrown up the call stack until it reaches the top level of the program
- an exception that cant be recovered is ofter referred to as a fatal exception
### Throw an Error
- create errors
```js
const error1 = new Error("Something bad happened!");
const error2 = Error("Something bad happened!");
```
- typically see Error created with the `new` operator
- `new` is used when creating a new instance of an object
#### Throwing Errors
- when error is thrown code stops running
```js
const a = 3;

if(a === 3) {
    throw new Error("we dont want a to be 3");
}

// <-- we never reach this line
```
### Catch an Error
- the code will `try` a statement
- if errors are thrown the logic will flow into the `catch` block
- the line ```console.log(ex);``` will only execute if an error `(ex)` is thrown by `readFile`
```js
try {
    readFile("book"); 
}
catch(ex) {
    console.log(ex); // EISDIR: illegal operation
}
```
- The EISDIR is thrown in Node.JS when the target is a directory when we were expecting it to be a file
### Return Error
#### Catch and Return
- an error is caught the program can continue executing
```js
function writeLogFile(id, contents) {
    try {
        writeFile(`logs/${id}`, contents);
    }
    catch(ex) {
        return false;
    }
    return true;
}
```
### Start an Error
#### Type Error
- thrown when a variable is no the expected type for the operation
```js
const x = 3;

x();

// TypeError: x is not a function
```
```js
let b;

b.prop;
// TypeError: Cannot read property 'prop' of undefined
```
#### Reference Error
- thrown in cases where the variable is not defined; the reference cannot be found
```js
z();

// ReferenceError: z is not defined
```
#### Syntax Error
- thrown in cases where the code is not valid JavaScript
```js
const a = 3;

a.72;
// SyntaxError: Unexpected number
```
#### Range Error
- Thrown when a value is passed to a function where the value is not within the intended range of accepted value
```js
new Array(Infinity)

// RangeError: Invalid array length
```
## Type Conversion
### String to Number
- explicitly
```js
const string = "2"
console.log(Number(string)); // 2

const string = "hello"
console.log(Number(string)); // NaN
```
- can also convert strings to numbers with `parseInt` and `parseFloat`
- these will chop off non-numeric characters at the end of the string
- implicitly
```js
const string = "2";
console.log(+string); // 2

const string2 = "hello";
console.log(+string2); // NaN
```
- best practice is to use explicit conversion in most cases
#### ParseInt and ParseFloat
- only works with non-numeric characters at the **end of the string**
- if the string starts with non-numeric characters it will return `NaN`
- `NaN` stands for **Not a Number**
- `parseFloat` function appears when working with **floating point** numbers
```js
const float = 12.24;
console.log(parseInt(float)); // 12
console.log(parseFloat(float)); // 12.24
```
#### TypeOf
- `typeof` operator is an easy way of checking a value's type
```js
console.log( typeof 1 ); // number
console.log( typeof "1" ); // string
console.log( typeof {} ); // object
```
### To String
- explicit
```js
const a = 123;

console.log(a.toString()); // "123"
console.log(String(a)); // "123"

console.log(false.toString()); // "false"
```
- implicit
```js
console.log(123 + ""); // "123"
console.log(true + ""); // "true"
```
- if the string has a number in it they will still be added together as strings
```js
console.log(2 + "2"); // "22"
```
### Is Truthy
- can covert boolean explicitly
```js
console.log(Boolean(2)); // true
console.log(Boolean("")); // false
```
- implicitly converted
```js
if(3) {
    console.log('3 is truthy!');
}
```
#### Not Not
```js
console.log(!3); // false
console.log(!""); // true
```
```js
console.log(!!3); // true
console.log(!!""); // false
```
### Loose Equals
- when values are different types, the `===` operator will always evaluate to false
```js
console.log("2" === 2); // false
```
- the loose equals `==` comparison operator will attempt type conversion to compare values
```js
console.log("2" == 2); // true
```
- many discourage the use o f`==` because its less performant and can lead to confusing results
### Object to JSON
- JSON = JavaScript Object Notation, a format for transferring JS data
```js
const person = '{"name":"Jim"}';
```
- can get the same string using `JSON.stringify` on an existing object
```js
const person = JSON.stringify({ name: "Jim" });

console.log(person); // {"name":"Jim"}
```
### Valid JSON
- keys in double quotes is required in valid JSON
- can be parsed and turned into an object
```js
const item = JSON.parse(itemJSON);

console.log(item.type); // food
console.log(item.edible); // true
```
- `.` operator can be used like JS objects
## Destructuring, Rest, and Spread
- transplilers convert new language features into code that older browsers support
### Destructuring
- unpack and object and assign its properties to new values
```js
const obj = {
  a: 2,
  b: 3,
}

// destructure assignment
const { a, b } = obj;

console.log(a); // 2
console.log(b); // 3
```
- works with arrays
- in this case we are pulling values out of the array based on their position
```js
const arr = ["hello", "world"];

const [a, b] = arr;

console.log(a); // hello
console.log(b); // world
```
- same works for functional arguments
```js
function addThree([a,b,c]) {
    return a + b + c;
}

const sum = addThree([1,2,3]);

console.log(sum); // 6
```
### Rest Parameters
```js
function log(...args) {
    console.log(args);
}

log(1, 2, 3, 4, 5); // [1, 2, 3, 4, 5]
```
- rest parameter syntax can assign function arguements as an array
- `...args` assigns an array with all the values of the arguements
- can also gran the rest of parameters
```js
function log(a, b, ...args) {
    console.log(args);
}

log(1, 2, 3, 4, 5); // [3, 4, 5]
```
```js
const [a, b, ...others] = [1, 2, 3, 4, 5];

console.log(others); // [3, 4, 5]
```
### Spread Arguements
- instead of saying saying grab the rest of the values (Rest Arguement) we're saying spread these values out
```js
const numbers = [1, 2, 3];

function add(a, b, c) {
  return a + b + c;
}

const sum = add(...numbers);

console.log(sum); // 6
```
- here the values are being spread out to the variable `a`, `b`, `c`
#### Wrap Up
- Instead of deconstructing we can assign variables to the objects properties
```js
const x = obj.x;
```
- rather than deconstructing it
```js
const { x } = obj;
```

---
# Practice Problem 3
  * [Either Not Both](#either-not-both)
  * [Fizz Buzz](#fizz-buzz)
## Either Not Both
```js
function eitherNotBoth(num) {
    const remainder3 = num % 3;
    const remainder5 = num % 5;
    if(remainder3 === 0 && remainder5 === 0){
        return false;
    }
    else if(remainder3 === 0 || remainder5 === 0){
        return true;
    }
    return false;    
}
```
## Fizz Buzz
```js
function fizzBuzz(numbers) {
    let fbArray = ""
    for(let i = 0; i < numbers.length; i++){
        if(numbers[i] % 5 === 0 && numbers[i] % 3 === 0){
            fbArray += "fizzbuzz";
        }
        else if(numbers[i] % 5 === 0){
            fbArray += "buzz";
        }
        else if(numbers[i] % 3 === 0){
            fbArray += "fizz";
        }
    }
    return fbArray
}
```
---
# Class & Prototypes
  * [This Keyword](#this-keyword)
    + [Using This](#using-this)
      - [Call Versus Apply](#call-versus-apply)
    + [Binding This](#binding-this)
      - [Bind Arguments](#bind-arguments)
    + [Implicit Binding](#implicit-binding)
      - [Call-Site](#call-site)
    + [Unbound Function](#unbound-function)
      - [Closure](#closure)
      - [Bind the Function](#bind-the-function)
      - [Arrow Syntax](#arrow-syntax)
      - [More Notes](#more-notes)
  * [Prototype Chain](#prototype-chain)
    + [Taking Shape](#taking-shape)
    + [Move Shape](#move-shape)
      - [Adding a Method](#adding-a-method)
    + [Circle Shape](#circle-shape)
      - [Share Functionality](#share-functionality)
    + [Move Circle](#move-circle)
      - [Linking Prototypes](#linking-prototypes)
      - [Object Create](#object-create)
    + [Rectangle](#rectangle)
      - [Create a Rectangle Shape](#create-a-rectangle-shape)
    + [Rectangle Flip](#rectangle-flip)
      - [Adding a Prototype](#adding-a-prototype)
  * [Classes](#classes)
    + [Hero](#hero)
      - [Classs Syntax](#classs-syntax)
      - [Instances](#instances)
    + [Take Damage](#take-damage)
      - [Methods](#methods)
    + [Warrior](#warrior)
      - [Subclasses](#subclasses)
    + [Super Warrior](#super-warrior)
      - [New Keyword Super](#new-keyword-super)
    + [Building Rage](#building-rage)
      - [Calling Super Methods](#calling-super-methods)
    + [Passing Health](#passing-health)
      - [Configurable Health](#configurable-health)
## This Keyword
- `this` keyword provides a function context
### Using This
- in a global function (not inside the function), `this` refers to the module itself with Node.js or the window inside the browser
- **explicit**
```js
function sum() {
    return this.a + this.b;
}

/* If we were to run sum() directly this would
be set from the global scope and likely
neither a nor b would be defined */

const result = sum.call({ a: 2, b: 4 });

console.log(result); // 6 
```
- `call` is available on all JavaScript function
- The first arguement we pass to `call` becomes `this` inside the new function
#### Call Versus Apply
- both `call` and `apply` can set context to `this`
```js
totalThings.call("Students", 10, 3, 2);

totalThings.apply("Students", [10, 3, 2]);
```
- in both cases `this` is set to "students"
- the difference is that `call` takes a list of arguments while `apply` takes a single array
### Binding This
- rather than relying on a function to be called with the correct `this` at the time of invocation we can `bind` functions
```js
function thisName() {
    return this.name;
}
const newFunction = thisName.bind({ name: 'Ted' }); 
console.log(newFunction()); // Ted
console.log(thisName()); // undefined
```
- `bind` does not change the nature of the original function; it creates a new function bound with the provided `this`
- once bound **binding cannot be overwritten**
```js
const newFunction2 = newFunction.bind({ name: 'Walt' });
console.log(newFunction2()); // Ted
```
#### Bind Arguments
```js
function add(x, y) {
    return x + y;
}
```
- bind an arguement to `add` to create a new type of function
```js
const addTwo = add.bind(null, 2);

console.log( addTwo(2) ); // 4
console.log( addTwo(10) ); // 12
```
### Implicit Binding
#### Call-Site
- without explicitly setting `this` with `call` or `apply` there are a few rules that dictate `this`
```js
const obj = {
    value: 2,
    getValue: function() {
        return this.value;
    }
}
```
- depending on how `getValue` gets called the result could be **different**
```js
console.log( obj.getValue() ); // 2
```
- the function got called by accessing it on the object's property; the `this` keyword is implicitly bound to the object its being called on
```js
const fn = obj.getValue;

console.log( fn() ); // undefined
```
- in this example `this` is not the obj itself. it's actually the `global` `this`.
- **without being called directly on the object, `this` is not bound at all**
- the place where the function gets called is referred to as the call-sit
- if the function is not bound it will determine the value of `this`
### Unbound Function
- often helpful to define functions inside of functions
- asynchronus programming means the code may run at a future point in time
```js
const YEAR = (1000 * 60 * 60 * 24 * 365);

function addYear() {
    setTimeout(function() {
        this.age++;
    }, YEAR);
}

const person = { name: 'Fred', age: 29 }

addYear.call(person);
```


#### Closure
- common way to fix issues with context in JavaScript is to capture the value of `this` inside of a function scope
```js
function addYear() {
    const that = this;
    setTimeout(function() {
        that.age++;
    }, YEAR);
}
```
#### Bind the Function
- we can bing the function inside of the `setTimeout`
```js
function addYear() {
    setTimeout(function() {
        this.age++;
    }.bind(this), 1);
}
```
- the new function is bound to the same context as `addYear`
#### Arrow Syntax
- another way to define function expressions
- the difference between arrow syntax and the traditional function syntax is in the behavior with `this`
```js
function addYear() {
    setTimeout(() => {
        this.age++;
    }, YEAR);
}
```
- Just by changing from `function() { }` to `() => {}`, we can fix the context issue
#### More Notes
- `this` is used to refer to the object that is "in charge" of the code that is currently running
## Prototype Chain
### Taking Shape
- **Classes** are template for creating objects called **instances**
- Each instance has its own set of properties called **state**
- Prototypes provide a way to share properties and functions by **linking objects together**
```js
function Car(make, model) {
    this.make = make;
    this.model = model;
}

const car = new Car('Toyota', 'Camry');
const car2 = new Car('Honda', 'Civic');

console.log(car.make) // Toyota
console.log(car2.model) // Civic
```
- `Car` is capitalized to show we plan to use it within the `new` operator
- Using the `new` operator creates new instances of `Car`
- the `new` operator will create a new object and set it to `this` within the car function
- `new` is another rule for how it is bound
- both `car` intstances will have the properties `make` and `model`
### Move Shape
#### Adding a Method
```js
function Shape(x,y) {
    this.position = { x,y }
}

Shape.prototype.move = function(x,y) {
    // move the shape
}
```
- by adding this method to the `Shape.prototype` object new instances will be able to access it via the prototype chain
- be careful not to use arrow function syntax here or `this` may not be appropriately bound
- with arrow syntx it will inherit the context of the scope
### Circle Shape
#### Share Functionality
```js
const Shape = require('./Shape');

function Circle(x, y, radius) {
    Shape.call(this, x, y);
    // store radius on 
    this.radius = radius
}
```
### Move Circle
#### Linking Prototypes
- inherit methods from another prototype chain
```js
Circle.prototype = Object.create(Shape.prototype);
```
#### Object Create
- method to link prototypes
```js
const car = {
    make: 'Toyota',
    model: 'Camry',
}

const camry = Object.create(car);

console.log(camry.make); // Toyota
console.log(camry.model); // Camry
```
- the property `make` doesn't exist on `camry`. It exist on `car` and `camry` is simply linked via the prototype chain to `car`. the property is shared.
### Rectangle
#### Create a Rectangle Shape
```js
const Shape = require('./Shape');

function Rectangle(x, y, height, width) {
    Shape.call(this, x, y);
    this.height = height;
    this.width = width;
    
}
```
### Rectangle Flip
#### Adding a Prototype
```js
const Shape = require('./Shape');

function Rectangle(x, y, height, width) {
    Shape.call(this, x, y);
    this.height = height;
    this.width = width;
    
}

Rectangle.prototype = Object.create(Shape.prototype);

Rectangle.prototype.flip = function() {
    const width = this.width;
    this.width = this.height
    this.height = width;

}
```
## Classes
- classes create a new interface for using **prototypes**
### Hero
#### Classs Syntax
- defined using the word `class` followed by its name  and  `{}`
- methods can be custom or a **constructor**
- **constructor** is a special function called only once per new **instance**
- when an instance is created the constructor function is called
```js
const h1 = new Hello(); // hello!
const h2 = new Hello(); // hello!
```
- constructor is a great place ot initialize properties on a class instance by using '`this
```js
class Team {
    constructor() {
        this.sport = "soccer";
    } 
}

const t1 = new Team();
console.log(t1.sport); // soccer
```
#### Instances
- Classes from templates for new objects to borrow behavior from
- these new objects are called **instances**
- all instances refer to the same method created on the class
```js
class Team {
    constructor(name) {
        this.name = name;
    }
}

const team1 = new Team("Giants");
const team2 = new Team("Jets");
```
### Take Damage
#### Methods
- can add methods to classes in addition to constructor
```js
class Hero {
    constructor() {
        this.health = 50  
    }
    takeDamage(num) {
        this.health -= num
    }
}
```
### Warrior
#### Subclasses
- its possible to create subclasses to **extend** or inherit behavior from their parent class
```js
class Shape {
    constructor() {
        this.position = { x: 0, y: 0 }
    }
}

class Rectangle extends Shape {
    
}
```
### Super Warrior
#### New Keyword Super
```js
class Shape {
    constructor() {
        this.position = { x: 0, y: 0 }
    }
}

class Rectangle extends Shape {
    constructor() {
        super();
        this.height = 10;
        this.width = 5;
    }
}
```
- notice the use of the keyword **super**, when invoked, this calls the constructor on `Shape`
- subclasses **must** call `super` before accessing `this` inside the constructor or JS will throw a reference error
```js
class Shape {
    constructor() {
        this.position = { x: 0, y: 0 }
    }
}

class Rectangle extends Shape {
    constructor() {
        super();
        this.height = 10;
        this.width = 5;
    }
}
```
### Building Rage
#### Calling Super Methods
- the class that has been extended is called the **parent** while the class extending it is called the **child**
```js
class Potion {
    constructor() {
        this.empty = false;
    }

    drink() {
        this.empty = true;
    }
}

class NoisyPotion extends Potion {
    drink() {
        super.drink();
        console.log("LOUD NOISES!");
    }
}
```
- by calling `super.drink()` it will also set itself to `empty`, which is the `drink` behavior of `Potion`
### Passing Health
#### Configurable Health
```js
class Hero {
    constructor(health) {
        this.health = health  
    }
    takeDamage(damage) {
        this.health -= damage
    }
}

const Hero = require('./Hero');

class Warrior extends Hero {
    constructor(health) {
        super(health);
        this.rage = 0
    }
    takeDamage(damage) {
        super.takeDamage(damage)
        this.rage += 1
    }
}
```
---
# Binary and Hexidecimal
  * [Binary](#binary)
    + [Representing Values](#representing-values)
    + [Multiple Characters in Decimal](#multiple-characters-in-decimal)
    + [Mutiple Characters in Binary](#mutiple-characters-in-binary)
    + [Rules for Counting Decimal](#rules-for-counting-decimal)
    + [Counting Binary](#counting-binary)
    + [Bits, Nibbles, and Bytes](#bits--nibbles--and-bytes)
    + [Magnitudes](#magnitudes)
  * [Hexidecimal](#hexidecimal)
    + [16 Symbols](#16-symbols)
    + [0x Prefix](#0x-prefix)
## Binary
### Representing Values
- **Decimal** can be **10 values** with symbols **0** - **9**
- **Binary** can represent **2 values** with symbols **0** and **1**
### Multiple Characters in Decimal
- **One decimal** character represents **10 values**
- **Two decimal** characters represents **100 values**
- **Three decimal** characters represents **1000 values**
### Mutiple Characters in Binary
- **One character** represents **2 values**
- **Two characters** represent **4 values**
- **Three Characters** represent **8 values**
	- `000`, `001`, `010`, `011`, `100`, `101`, `110`, `111`
- the number of values we can represent in binary is `2 ** n` where `n` is the number of characters
- 256 id `2 ** 8` and 1024 is `2 ** 10`
### Rules for Counting Decimal
1. Here are 10 symbols listed from lowest to highest, separated by a comma: `0,1,2,3,4,5,6,7,8,9`
2. Start at the lowest symbol (0).
3.  Count by moving up to the next highest symbol.
4.  Repeat step 3 until we have reached the highest symbol.
- the further left a character is is the more significance it has in our number
### Counting Binary
- same rules but range is shortened to just `0` and `1`
- `0, 1, 10, 11, 100, 101, 110, 111, 1000`
### Bits, Nibbles, and Bytes
- **bit** - a **single** character in binary (a single character in decimal is called a digit!)
- **nibble** - a somewhat uncommon term for **four bits together** (i.e. `1011`)
- **byte** - **eight bits together**: `1000 1100` would be a byte!
- `256` the number of distict values we can represent with a **byte**
- could represent all positive integersfrom 0 through 255
- to include negative numbers, split the range in half representing from -128 to 127
### Magnitudes
- 1_000 is referred to as a thousand
- 1_000_000 is referred to as a million
- 1_000_000_000 is referred to as a billion
- 1024 bits (2 ** 10) is referred to as a **kilobit**
- 1024 kilobits is referred to as a **megabit**
- 1024 megabits is referred to as a **gigabit**
- The same rule applies for bytes (i.e. 1024 bytes is a **kilobyte**)
## Hexidecimal
- Hexadecimal is traditionally used to represent raw data
### 16 Symbols
- uses 16 symbols: `0` through `9` and `a` through `f`
- The decimal values for a through f are `10` through `15`
### 0x Prefix
- the 0x in front simply denotes the rest of this string is hexadecimal
- Since each character in hexadecimal can represent 16 values, it essentially maps to a nibble or four bits:
	- 0 = 0
	- 1 = 0001
	- 2 = 0010
	- e = 1110
	- f = 1111
```
1111 0100 1101 1001 0111
F    4    D    9    7

1    C    3    A    F
0001 1100 0011 1100 1111
```