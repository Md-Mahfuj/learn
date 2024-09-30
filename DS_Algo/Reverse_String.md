```javascript
var str =" my name is mahfuj";
const sp = str.split(" ").map(function(word){
  return  word.split("").reverse().join("");
    
})


console.log(sp.join(" "));


```
