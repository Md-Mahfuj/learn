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
