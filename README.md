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