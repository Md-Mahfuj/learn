1. Remove falsy values from array
2. Convert any value to boolean
3. Resizing any array
4. Flatten multi-dimensional array
5. Short conditionals
6. Replace all occurrences of a string 
7. Log values with variable names
8. Know performance of task

#   Remove falsy values from array
### Note: There are only six falsy values in JavaScript: undefined , null , NaN , 0 , "", and false.

```JavaScript
// passing boolean to arr.filter(boolean) will remove falsy values from array.

const arr = [1, "test", undefined, null,  5, false, "", 3, NaN];
const result = arr.filter(Boolean);   // = > [1, "test", 5, 3]
console.log(result);

```
```JavaScript
// Boolean(expression) in JS returns true/false
Boolean(5 < 6); //  true
Boolean(100 > 200); // false
Boolean('JavaScript'); //true
Boolean(''); //false

// array example
let miscellaneous = ['🍎', false, '🍊', NaN];
let fruits = miscellaneous.filter(Boolean);

console.log(fruits); // ['🍎', '🍊']

```
```JavaScript
// Convert any value to boolean

// Using !! in front of any value
console.log(!!"mashrafi"); // true
console.log(!!1); // true
console.log(!!0); // false
console.log(!!undefined); // false

// We can also use Boolean() to achieve same
console.log(Boolean("mashrafi")); // true

```
```JavaScript
// Resizing any array
let animals = ["🐕", "🐒", "🦊", "🐅"];

// We can use array's length property
animals.length = 3;

console.log(animals); // ["🐕", "🐒", "🦊"]
```
```JavaScript
// How to flattern a multi-dimensional array
let smileys = ['🥰', ['😄', '😃'], '😉', ['🥲', '😑']];

// We can use array.flat() method to flattern one level array
console.log(smileys.flat()); // ['🥰', '😄', '😃', '😉', '🥲', '😑']

// Multi level array
let smileys2 = ['🥰', ['😄', '😃', ['🥲', '😑']], '😉'];

// We can pass 'Infinity' parameter to array.flat function
console.log(smileys2.flat(Infinity)); // ['🥰', '😄', '😃', '🥲', '😑', '😉']

```

```JavaScript
// Short conditionals
const captain = "Mashrafi";

// Instead of doing this
if(captain === "Mashrafi") {
    console.log("❤️");
}

// We can use &&
captain === "Mashrafi" && console.log("❤️");

// And instead of doing this
if(captain !== "Mashrafi") {
    console.log("😡");
}

// We can use ||
captain === "Mashrafi" || console.log("😡");

```
```JavaScript
// Replace all occurances of a string
const quote = "React is a JS framework & this framework is the most popular front-end framework right now";

// Replace all occurances of 'framework' with 'library'
console.log(quote.replace(/framework/g, "library")); // React is a JS library & this library is the most popular front-end library right now
```


```JavaScript
const a = 5;
const b = 10;

// we can test whether a value is greater than the other value
console.log(a > b);
// we can also test whether a value is greater than or equal to the other value
console.log(a >= b);
// looks like I have a font installed so for me, it's going to look like one sign,
// but it's two. The greater than sign, and then immidiately the equality sign.

// we can test whether a value is less than the other value
console.log(a < b);
// we can also test whether a value is less than or equal to the other value
console.log(a <= b);

// finally, we have the equality operators,
// we can test whether a value is equal
console.log(a == b);
// we also test whether a value is not equal
console.log(a != b);

// what you're going to see more often are going to be the strict equality
// and strict inequality operators. They look like this.

// strict equal, strict not equal
console.log(a === b);
console.log(a !== b);

```

# What is scope and why do we need it?

What is Scope? Why do we need it? And how can it help us write less error-prone code?

Scope simply allows us to know where we have access to our variables. It shows us the accessability of variables, functions, and objects in some particular part of the code.

Why would we want to limit the visibility of variables and not have everything availabile everywhere in our code?

Firstly, it provides us with some level of security to our code.

Secondly, it helps to improve efficiency, track bugs and reduce them. It also solves the problem of naming variables.

## We have three types of scopes:

### 1.Global Scope
### 2.Local Scope
### 3.Block Scope (only with let and const)

Variables defined inside a function are in local scope while variables defined outside of a function are in the global scope. Each function when invoked creates a new scope.

There are rules about how scope works, but usually you can search for the closest { and } braces around where you define the variable. That “block” of code is its scope.

All of this might be confusing, until you see some examples. You're going to immediately understand what a scope is. Let's explore it in the code.

```JavaScript

const name = "Adrian";

const logName = () => {
  console.log(name);
};

logName();

```

## Advantages of using Global variables
### You can access the global variable from all the functions or modules in a program
### It is ideally used for storing "constants" as it helps you keep the consistency.
### A Global variable is useful when multiple functions are accessing the same data.

## Disadvantages of using Global Variables

###  Too many variables declared as global, then they remain in the memory till program execution is completed. This can cause of Out of  Memory issue.
###  Data can be modified by any function. Any statement written in the program can change the value of the global variable. This may give unpredictable results in multi-tasking environments.
###  If global variables are discontinued due to code refactoring, you will need to change all the modules where they are called.


# Local Scope

### Variables defined inside a function are in the local scope.
```JavaScript

// Global Scope

const someFunction = () => {
  // Local Scope #1

  const anotherFunction = () => {
    // Local Scope #2
  };
};

```

## Advantages of using Local Variables
###  The use of local variables offer a guarantee that the values of variables will remain intact while the task is running
### You can give local variables the same name in different functions because they are only recognized by the function they are declared in.
### Local variables are deleted as soon as any function is over and release the memory space which it occupies.
## Disadvantages of using Local Variables
### They have a very limited scope.

```JavaScript
if (true) {
  // this 'if' conditional block doesn't create a scope

  // name is in the global scope because of the 'var' keyword
  var name = "Adrian";
  // likes is in the local scope because of the 'let' keyword
  let likes = "Coding";
  // skills is in the local scope because of the 'const' keyword
  const skills = "JavaScript and PHP";
}

console.log(name); // logs 'Adrian'
console.log(likes); // Uncaught ReferenceError: likes is not defined
console.log(skills); // Uncaught ReferenceError: skills is not defined

```

