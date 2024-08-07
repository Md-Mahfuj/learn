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

```javascript 
let age = null;
```

### null is just a special value which represents “nothing”, “empty” or “value unknown”.
### The code above states that age is unknown or empty for some reason.

##  UNDEFINED

### A variable that has not been assigned a value is undefined.

### The special value undefined also stands apart. It makes a type of its own, just like null.

### The meaning of undefined is “value is not assigned”.

### If a variable is declared, but not assigned, then its value is undefined by default:


```javascript
let x;

console.log(x);
```

### Technically, it is possiable to assign undefined to any variable:


```javascript
let x = 123;

x = undefined;

alert(x); // "undefined"
```

### But I wouldn't recommend doing that. Normally, we use null to assign an “empty” or “unknown” value to a variable, and we use undefined for checks like seeing if a variable has been assigned.

## UNDEFINED VS NULL

### Many a times we often get confused on whats the difference between UNDEFINED and NULL.

### undefined means a variable has been declared but has not yet been assigned a value. On the other hand, null is an assignment value. It can be assigned to a variable as a representation of no value.

### Also, undefined and null are two distinct types: undefined is a type itself (undefined) while null is an object.

### Unassigned variables are initialised by JavaScript with a default value of undefined. JavaScript never sets a value to null. That must be done programmatically.


# Objects
```javascript
const person = {
  name: "John",
  age: 25,
};

console.log(person); // whole object
console.log(person.name); // just the name

```
### Object is the most important data-type and forms the building block for modern JavaScript. We will learn about objects in details in further lectures.

The object type is special. All other types are called “primitive” because their values can contain only a single thing (be it a string or a number or whatever). In contrast, objects are used to store collections of data and more complex entities.

What I'm going to let you know for now is that objects in their simplest forms are used to group variables.

### For example, we can create a variable of name, and age:

```javascript
const name = "John";
const age = 25;

```

These two variables in the current state are in no way related on to another.

We can create an object called person and put them together:


```javascript
const person = {
  name: "John",
  age: 25,
};
```

Now we know that both name and age belong to the same entity, the person. That is an object. As you can see, we declare it the same as all other variables and then put curly brackets inside of which goes the data.

The one last thing that we can mention is that we can now extract specific values from that object using the dot notation:

```javascript
person.name;
person.age;

```

### There are many other kinds of objects in JavaScript:

Array to store ordered data collections,
Date to store the information about the date and time,
Error to store the information about an error.
…And so on.


## There are two types of languages when it comes to data types:

### Statically typed language where each variable and expression type is already known at compile time. Once a variable is declared to be of a certain data type, it cannot hold values of other data types. Example: C, C++, Java.

### Dynamically typed languages can receive different data types over time. JavaScript is dynamically typed; variables in JavaScript can receive different data types over time. We're going to see this in action really soon.

A variable in JavaScript can contain any data. A variable can at one moment be a string and at another be a number, for example:

```javascript
let message = "Hello, World!";

message = 123456;

```
# Strict vs Loose Equality

### Equality is a fundamental concept in JavaScript. We say two values are equal when they are the same value. For example:

```javascript
console.log("This is a string." === "This is a string."); // true
console.log(2 === 2); // true

```

Note that we use three equal signs to represent this concept of equality in JavaScript.

JavaScript also allows us to test loose equality. It is written using two equal signs. Things may be considered loosely equal even if they refer to different values that look similar, an example would be the following:

```javascript
console.log(5 == "5"); // true
```

# Strict equality using ===
## The strict equality method of comparison is a preferred option to use because it’s behaviour can be easily predicted, which leads to less bugs and unexpected results. The JavaScript interpreter compares the values as well as their types and only returns true when both are the same.

```javascript

console.log(20 === "20"); // false
```

The code above will print false because even though the values seem to be the same, they are of different types. The first one is of type String and the second is of type Number.

Here's just one short thing that I wanted to show you. If we strictly compare objects, we're never going to get true. Let's test it out:

```javascript
console.log({} === {}); // false
// we get false, even though they have the same type and content, weird

// the same thing happens for arrays as they are actually objects under the hood
console.log([] === []); // false
```


For the sake of simplicity, we're not going to go into too much depth about non-primitive data types like objects and arrays. That is a rather complex topic on it’s own. Because of that, later in the course we have a whole separate section called Value vs Reference. In there we're going to explore the mentioned inconsistencies of the equality operator.

Now let's move on to the loose equality.

# Loose equality

We write loose equality using double equal sign. It uses the same underlying logic as the Strict equality except for a minor, yet huge, difference.

## The loose equality doesn’t compare the data types.

## You should almost never use the loose equality.

Douglas Crockford's in his excellent book called JavaScript: The Good Parts wrote:

JavaScript has two sets of equality operators: === and !==, and their evil twins == and !=.

The good ones work the way you would expect. If the two operands are of the same type and have the same value, then === produces true and !== produces false. The evil twins do the right thing when the operands are of the same type, but if they are of different types, they attempt to change the values. The rules by which they do that are complicated and unmemorable. These are some of the interesting cases:



```javascript
"" == "0"; // false
0 == ""; // true
0 == "0"; // true

false == "false"; // false
false == "0"; // true

false == undefined; // false
false == null; // false
null == undefined; // true
```

Using the == operator

```javascript
  true == 1; // true, because 'true' is converted to 1 and then compared
  "5" == 5; // true, because the string of "5" is converted to the number 5 and then compared
```

Using the === operator

```javascript
 true === 1; // false
 "5" === 5; // false
```

```javascript


```

That's exactly how it should be. On the other hand:

```javascript
  5 == "5"; // true
```
This isn't and should never be equal. "5" is a string, and should be treated like that. As I mentioned, most of the JavaScript developers completely avoid loose equality and rely only on the strict equality. It is considered a better practice and it causes less bugs. From now one, you're going to see me use only the strict equality.


So what's the moral of the story? Always use three equal signs.

```javascript
console.log("This is a string." === "This is a string."); // true
console.log(2 === 2); // true

console.log(5 == "5"); // true
console.log(20 === "20"); // false

"" == "0"; // false
0 == ""; // true
0 == "0"; // true

false == "false"; // false
false == "0"; // true

false == undefined; // false
false == null; // false
null == undefined; // true

```


In JavaScript, we also have something known as truthy values and falsy values.

Truthy expressions always evaluate to boolean true and falsy evaluate to boolean false.

Knowledge of truthy and falsy values in JavaScript is a must, if you don't know which values evaluate to truthy and which to falsy, you're going to have a hard time reading other people's code.

Longtime JavaScript developers often toss around the terms "truthy" and "falsy", but for those who are newer to JavaScript these terms can be a bit hard to understand.

When we say that a value is "truthy" in JavaScript, we don't just mean that the value is true. Rather, what we mean is that the value coerces to true when evaluated in a boolean context. Let's look at what that means.

The easiest way to learn truthy and falsy values is to memorise falsy values only. There are only six falsy values, all the other values are truthy.

Let's explore the list of falsy values:

# FALSY

### false
### 0 (zero)
### "", '', `` (empty strings)
### null
### undefined
### NaN (not a number)

note : Empty array ([]) is not falsy

### TRUTHY

### Everything that is not FALSY
That's a pretty straightforward list. But how can we actually use truthiness? Let's look at an example.

Taking advantage of truthiness can make your code a little bit more concise. We don't need to explicitly check for undefined, "", etc. Instead we can just check whether a value is truthy. However, there some caveats to keep in mind.

# for

### It’s called a for loop because it runs “for” specific number of times. For loops are declared with three optional expressions separated by semicolons: initialization, condition and final-expression. Followed by a statement (usually a block statement).

```javascript

for ([initialization]; [condition]; [final - expression]) {
  statement;
}


for (let i = 0; i < 10; i++) {
  console.log(i);
}


let i = 0; // we have i already declared and assigned
for (; i < 10; i++) {
  // no need for "initialization"
  console.log(i); // 0, 1, 2
}

// We can actually remove everything, creating an infinite loop:


for (;;) {
  // repeats without limits
}

```
#   Functions Intro

##  So what are functions, and why should we use them? 
### ans: A JavaScript function is a block of code designed to perform a particular task. Remember that, a block of code designed to perform 
    a particular task. We will often need to perform a similar task many times in our application.
### Functions are the main building blocks of the program. They allow the code to be called many times without repetition


## Defining functions

A function declaration consists of the function keyword, followed by:

I'm first going to show you an example of a simple function called square:

```javascript

function square(number) {
  return number * number;
}
```

## Calling Functions

Defining a function does not execute it. Defining it simply names the function and specifies what to do when the function is called.

Calling the function actually performs the specified actions with the indicated parameters. For example, if you define the function square, you could call it as follows:


```javascript
square(5);
```





  
