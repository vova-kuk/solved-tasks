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
#### Make a function that does arithmetic!
```javascript
function arithmetic(a, b, o){
  let obj = {
    "add": a + b,
    "subtract": a - b,
    "multiply": a * b,
    "divide": a / b,
    }
  return obj[o]; 
}
```
#### Playing with cubes I (Java)
public class Cube{
  int Side;
  void setSide(int num){
    this.Side = num;
  }
  int getSide(){
    return Side;
  } 
}
#### Numbers to Letters
```javascript
const switcher = x => x.reduce((word, number) => `${word}${' ?!abcdefghijklmnopqrstuvwxyz'[29 - number]}`, '')
```
#### Simple Fun #37: House Numbers Sum
```javascript
function houseNumbersSum(A) {
  let sum = 0;
  for (let i = 0; i < A.length; i++) {
    if (A[i] === 0) break;
    sum += A[i];
  }
  return sum;  
}
```
#### Well of Ideas - Easy Version (Java)
```java
public class Kata {
 

  public static String well(String[] x) {
    int a = 0;
    for (int i = 0; i < x.length; i++) {
      if (x[i].equals("good")) a++;
    }
    
  if (a == 0) return "Fail!";
  if (a > 0 && a < 3) return "Publish!";
  if (a > 2) return "I smell a series!";
  return "";
  }
}
```
#### Tail Swap
```javascript
function tailSwap(arr) {
  let a = arr[0].split(':');
  let b = arr[1].split(':');
  let ar = a[0] + ':' + b[1];
  let ar2 = b[0] + ':' + a[1];
  return [ar, ar2];
}
```
#### Santa's Naughty List
```javascript
function findChildren(s, c) {
  let arr = [];
  for (let i = 0; i < s.length; i++) {
    if (c.includes(s[i]) && !arr.includes(s[i])) arr.push(s[i])
  }
  return arr.sort();
}
```
#### Is n divisible by x and y?
```javascript
function isDivisible(n, x, y) {
  return n % x === 0 && n % y === 0;
}
```
#### Find The Parity Outlier
```javascript
function findOutlier(int){
  return int.filter(el => el % 2).length > 1 ? int.find(el => el % 2 === 0): int.find(el => el % 2);
}
```
#### Array.diff
```javascript
function array_diff(a, b) {
  return a.filter(el => !b.includes(el));
}
```
#### Counting Duplicates
```javascript
function duplicateCount(text){
  //...
  let arr = text.toLowerCase().split(''); 
  
  let newArr = arr.filter(function(a, b) {
    return arr.indexOf(a) !== b;
  });
  
  return newArr.filter(function(item, pos) {
    return newArr.indexOf(item) == pos;
  }).length;
}
```
#### Take a Ten Minute Walk
```javascript
function isValidWalk(walk) {
  let n=[],s=[],e=[],w=[];
  walk.map(v=>{
  if (v==='n')n.push(1);
  if (v==='s')s.push(1);
  if (v==='e')e.push(1);
  if (v==='w')w.push(1);
})
  return (n.length===s.length)&&(w.length===e.length)&&(walk.length===10)
}
```
#### Your order, please
```javascript
function order(w){
  if (w === '') return '';
  let arr = w.split(' ');
  let result = [];
  for (let i = 1; i < arr.length + 1; i++) {
    result.push(arr.find(el => el.includes(i)));
  }
  return result.join(' ');
}
```
#### Alphabetical Addition
```javascript
function addLetters(...letters) {
  const alpha = 'zabcdefghijklmnopqrstuvwxy';
  const sum = letters.reduce((sum, letter) => sum + alpha.indexOf(letter), 0) % 26;
  return alpha[sum];
}
```
#### Product of consecutive Fib numbers
```javascript
function productFib(prod){
  const fib = [1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597, 2584, 4181, 6765, 10946, 17711, 28657, 46368, 75025, 121393, 196418, 317811, 514229, 832040, 1346269, 2178309, 3524578, 5702887, 9227465, 14930352, 24157817, 39088169, 63245986, 102334155];
  let a, b;
  for (let i = 0; fib[i] * fib[i + 1] <= prod; i++) {
    a = i;
    b = i + 1;
  }
  return fib[a]*fib[b]===prod ? [fib[a], fib[b], true] : [fib[b], fib[b+1], false];
}
```