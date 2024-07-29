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



