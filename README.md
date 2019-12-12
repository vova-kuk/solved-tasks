# solved-tasks
#### Filter the number
```javascript
var FilterString = function(v) {
  let c = '';
  for (let i = 0; i < v.length; i++){
    if (!isNaN(v[i])) c += v[i];
  }
  return +c;
}
```
#### Filling an array
```javascript
function arr (N) {
let arr = [];
for (let i = 0; i < N; i++){
  arr.push(i);
  }
  return arr;
}
```