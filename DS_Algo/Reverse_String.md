```javascript
var str =" my name is mahfuj";
const saveArray = str.split(" ").map(function(word){
  return  word.split("").reverse().join("");
    
})


console.log(saveArray.join(" "));


```
