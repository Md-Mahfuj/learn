```javascript
var str =" my name is mahfuj";
const saveArray = str.split(" ").map(function(word){
  return  word.split("").reverse().join("");
    
})
console.log(saveArray.join(" "));


```

```

//  How to check if an object is an array or not ? 

function checkArray(elem){
    return Array.isArray(elem);
}

console.log(checkArray([]));

```
