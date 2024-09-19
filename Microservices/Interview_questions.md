### Master Closures with these 5 JavaScript Interview questions


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
    
    return function(b){
       // Closures
        return function (c){
       //Closures
            return a*b*c;
       }
    }
}

console.log(multiply(2)(3)(4));
```

// what do you think will be the output of this code 


```javascript
let count = 0;
(function printCount(){
    if (count===0){
        let count =1;
        console.log(count);
    }
    
    console.log(count);
})();

```


```javascript
// guess the output

// function a(){
//     for (var i=0;i<3;i++){
//         setTimeout(()=>{
//             console.log(i)
//         },i*1000)
//     }
// }
// a();

// modify this code to get the 
// output as 0 , 1 , 2


// function a(){
//     for (let i=0;i<3;i++){
//         setTimeout(()=>{
//             console.log(i)
//         },i*1000)
//     }
// }
// a();

// modify this code to get the 
// output as 0 , 1 , 2 using var keyword

function a(){
    for (var i=0;i<3;i++){
        (function(index){
             setTimeout(()=>{
            console.log(index)
        },i*1000)
            
        })(i)
       
    }
}
a();

```
