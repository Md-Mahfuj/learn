```javascript
var str =" my name is mahfuj";
const saveArray = str.split(" ").map(function(word){
  return  word.split("").reverse().join("");
    
})
console.log(saveArray.join(" "));


```

```javascript

//  How to check if an object is an array or not ? 

function checkArray(elem){
    return Array.isArray(elem);
}

console.log(checkArray([]));

```
```javascript
// how to empty an array in javaScript ?
var arry =[2,4,5,6,54,76];
arry.length = 0;

console.log(arry);

```

```javascript
// how would you check if a number is an interger ?

const isInteger =(num)=>{
    if(num%1===0){
        console.log("integer");
    }else{
       console.log("not a integer");
    }
}
isInteger(1);
```

```javascript
// write a javaScript function  that reverse a number  ?

function reverseNum (num){
 return Number(num.toString().split("").reverse().join(""));
}
console.log(reverseNum(13))


function reverseNum2(num){
    var rev=0;
    while(num>0){
        var rem = num%10;
        rev = rev*10+rem;
        num =Math.floor(num/10);
    }
    
    return rev;
}

console.log(reverseNum2(13))


```



```javascript


