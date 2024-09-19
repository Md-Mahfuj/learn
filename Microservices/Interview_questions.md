// guess the output

```javascript
var num =10;
(()=>{
    console.log(num);
    var num =20;
    console.log(num);
})();

// Output is : 
// undefined
// 20

```

```javascript
// Create a function multiplay that multiplies
// these 3 number provided that the 
// arguments are passed in this manner (multiply(2)(3)(4))

function multiply(a){
    //Closures
    return function(b){
       // Closures
        return function (c){
            return a*b*c;
       }
    }
}

console.log(multiply(2)(3)(4));
```
