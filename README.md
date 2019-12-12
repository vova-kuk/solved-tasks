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
#### Breaking chocolate problem
```javascript
function breakChocolate(n,m) {
  console.log(n, m);
  if (n === 0 || m === 0) return 0;
  let acc = m * n - 1;
  
  return acc;
}
```
#### Remove String Spaces
```javascript
function noSpace(x){
  x = x.split(' ');
  return x.join('');
}
```
#### Sum The Strings
```javascript
function sumStr(a,b) {
  return (+a + +b).toString();
}
```