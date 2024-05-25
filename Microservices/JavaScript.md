  ## Introduction to Rest and Spread Operator

 ### As stated from the beginning, the rest and spread operators are two different operators, but they have a common symbol: the three dots in JavaScript. Woah! Still trying to understand, right? Why are they both using three dots in JavaScript if they are not the same? Well, this is where it gets tricky, but I will explain it as we proceed.

## What Is a Rest Operator?
### A rest operator is a type of parameter that gets all of the remaining parameters of a function call via an Array. It enables us to handle a variety of inputs as parameters in a function. Because it is used to combine many items, the rest operator is very helpful during array and object destructuring

``` function sum(...numbers) {
 let total = 0;
  for (const num of numbers) {
    total += num;
  }
  return total;
}

const result =console.log (sum(1, 2, 3, 4)); 
// This returns 10 (1 + 2 + 3 + 4)
```

  
