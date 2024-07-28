  ## Introduction to Rest and Spread Operator

 ### As stated from the beginning, the rest and spread operators are two different operators, but they have a common symbol: the three dots in JavaScript. Woah! Still trying to understand, right? Why are they both using three dots in JavaScript if they are not the same? Well, this is where it gets tricky, but I will explain it as we proceed.

## What Is a Rest Operator?
### A rest operator is a type of parameter that gets all of the remaining parameters of a function call via an Array. It enables us to handle a variety of inputs as parameters in a function. Because it is used to combine many items, the rest operator is very helpful during array and object destructuring

```javascript
function sum(...numbers) {
 let total = 0;
  for (const num of numbers) {
    total += num;
  }
  return total;
}

const result =console.log (sum(1, 2, 3, 4)); 
// This returns 10 (1 + 2 + 3 + 4)
```
###  In the code example above, we created a function sum. Inside the parentheses, we added the rest parameter that will allow the function to accept any number of arguments and gather them into an array called numbers. Next, we created a variable total and assigned an initial value of 0 to this variable, which will eventually store the sum of all the numbers.
### The loop will iterate through each element in the numbers array then the const num will declare a variable num that represents the current number that’s being processed in the loop. Inside the loop, the next line, total+=num adds the current number num to the total sum. Once the loops finishes, the function will return the total, which is the sum of all the numbers.
### The final line invokes the function, which takes four inputs. All arguments are gathered into the numbers array within the function. These numbers are then added together using the loop, and the result, which is 10, is saved in the result variable.



## What Is a Spread Operator?
### The spread operator divides an array or object into separate elements or properties. The spread operator is mostly used if you want to duplicate the content of an array or combine or combine multiple arrays/objects together.
### For instance, if we have an array of numbers and want to build a new array with the elements of the first array we made by adding another element to the end of the first array we formed, we will use the spread operator (again, it’s ...) since what we want to do here is combine two arrays.


```javascript
const firstArray = [5, 10, 15, 20, 25, 30];
const newArray=[...firstArray, 35, 40]

```



##  NULL

### This type has only one value: null.
### The special null value does not belong to any of the types described above.
### It forms a separate type of its own which contains only the null value:

```let age = null;```

### null is just a special value which represents “nothing”, “empty” or “value unknown”.
### The code above states that age is unknown or empty for some reason.

##  UNDEFINED

### A variable that has not been assigned a value is undefined.

### The special value undefined also stands apart. It makes a type of its own, just like null.

### The meaning of undefined is “value is not assigned”.

### If a variable is declared, but not assigned, then its value is undefined by default:


```let x;

console.log(x);```

### Technically, it is possiable to assign undefined to any variable:


```let x = 123;

x = undefined;

alert(x); // "undefined"```

### But I wouldn't recommend doing that. Normally, we use null to assign an “empty” or “unknown” value to a variable, and we use undefined for checks like seeing if a variable has been assigned.

## UNDEFINED VS NULL

### Many a times we often get confused on whats the difference between UNDEFINED and NULL.

### undefined means a variable has been declared but has not yet been assigned a value. On the other hand, null is an assignment value. It can be assigned to a variable as a representation of no value.

### Also, undefined and null are two distinct types: undefined is a type itself (undefined) while null is an object.

### Unassigned variables are initialised by JavaScript with a default value of undefined. JavaScript never sets a value to null. That must be done programmatically.













  
