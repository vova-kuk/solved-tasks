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
#### Alan Partridge II - Apple Turnover
```javascript
function apple(x){
  return Math.pow(x, 2) > 1000 ? 'It\'s hotter than the sun!!' : 'Help yourself to a honeycomb Yorkie for the glovebox.';
}
```
#### Two Oldest Ages
```javascript
function twoOldestAges(ages){
  ages.sort((a, b) => a - b);
  let a = [];
  a.push(ages[ages.length - 2], ages[ages.length - 1]);
  console.log(ages, a);
  return a;
}
```
#### Is it a palindrome?
```javascript
function isPalindrome(x) {
  return x.toLowerCase() === x.split('').reverse().join('').toLowerCase();;
}
```