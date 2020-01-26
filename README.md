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
#### Which x for that sum?
```javascript
let solve = m => (2 * m + 1 -  Math.sqrt(4 * m + 1)) / (2 * m);
```
#### PI approximation
```javascript
function iterPi(epsilon) {
	let nearlyPi = 0;
	let alternate = 1;
	let i = 1;
	let count = 0;
	while ((Math.abs(nearlyPi * 4 - Math.PI)) > epsilon) {
		nearlyPi += (1 / i * alternate)
		i += 2;
		alternate *= -1;
		count += 1;
	}
	return [count, (Math.round((nearlyPi * 4) * 10000000000) / 10000000000)];
}
```
#### Sum of Digits / Digital Root
```javascript
function digital_root(n) {
  return (n - 1) % 9 + 1;
}
```
#### Tip Calculator
```javascript
function calculateTip(a, r) {
  console.log(a, r);
  let rating = r.toLowerCase();
  let res;
  switch (rating) {
    case 'terrible':
    res = 0;
    break;
    case 'poor':
    res = a * 1.05 - a;
    break;
    case 'good':
    res = a * 1.1 - a;
    break;
    case 'great':
    res = a * 1.15 - a;
    break;
    case 'excellent':
    res = a * 1.2 - a;
    break;
    default:
    return "Rating not recognised";
  }
  return Math.ceil(res);
}
```
#### Is Integer Array?
```javascript
function isIntArray(arr) {
  if (!arr) return false;
  if (0 === arr.length) return true;
  if (arr.some(el => !Number.isInteger(el))) return false;
  if (arr.some(el => isNaN(el))) return false;
  return arr.every(el => typeof el === 'number');
}
```
#### Basic Math (Add or Subtract)
```javascript
function calculate(str) {
return str.split('plus').join(' ').split('minus').join(' -').split(' ').reduce((acc, curr) => acc + +curr, 0) + '';
}
```
#### Absent vowel
```javascript
function absentVowel(x){
  if (!x.match(/a/)) return 0;
  if (!x.match(/e/)) return 1;
  if (!x.match(/i/)) return 2;
  if (!x.match(/o/)) return 3;
  if (!x.match(/u/)) return 4;
}
```
#### Beginner Series #3 Sum of Numbers
```javascript
function getSum( a,b ){
  let result = 0;
  if (a < b) {
    for (let i = a; i <= b; i++) {
      result += i;
  }
  } else if (a > b) {
    for (let i = b; i <= a; i++) {
      result += i;
  }
  } else {
    return a;
  }
  return result;
}
```
#### London CityHacker
```javascript
function londonCityHacker(j) {
  let res = 0;
  for (let i = 0; i < j.length; i++) {
    if (typeof j[i] === 'string') res += 2.4;
    if (typeof j[i] === 'number') res += 1.5;
  }
  for (let i = 0; i < j.length; i++) {
    if (typeof j[i] === 'number' && typeof j[i + 1] === 'number') {
    res -= 1.5;
    i++;
    }
  }
  return '£' + res.toFixed(2);
}
```
#### Watermelon
```javascript
function divide(weight){
  if (weight === 2) return false;
  return weight % 2 === 0;
}
```
#### Minimize Sum Of Array (Array Series #1)
```javascript
function minSum(arr) {
  let sum = 0;
  arr.sort((a, b) => a - b);
  for (let i = 0, j = arr.length - 1; i < arr.length / 2; i++, j--) {
    sum += arr[i] * arr[j];
  }
  return sum;
}
```
#### Cat and Mouse - Harder Version
```javascript
function catMouse(x, j){
  const C = x.indexOf('C');
  const m = x.indexOf('m');
  const D = x.indexOf('D');
  if (C === -1 || m === -1 || D === -1) return "boring without all three";
  if (Math.abs(C - m) > j) return "Escaped!";
  if (Math.abs(C - m) <= j && ((D < C && D < m) || (D > C && D > m))) return "Caught!";
  if (Math.abs(C - m) <= j && ((D > C && D < m) || (D < C && D > m))) return 'Protected!';
}
```
#### Moves in squared strings (I)
```javascript
const reverseString = (str, splitBy) =>
  str
    .split(splitBy)
    .reverse()
    .join(splitBy)

const vertMirror = string =>
  string
    .split('\n')
    .map(str => reverseString(str, ''))
    .join('\n')

const horMirror = string => reverseString(string, '\n')

const oper = (fct, s) => fct(s)
```
#### Count the divisors of a number
```javascript
function getDivisorsCnt(n){
  let result = 0;
  for (let i = 1; i <= n; i++) {
    if (n % i === 0) result ++;
  }
  return result;
}
```
#### Sum of odd numbers
```javascript
function rowSumOddNumbers(n) {
	return n * n * n;
}
```
#### The Wide-Mouthed frog!
```javascript
function mouthSize(a) {
  return a.toLowerCase() === "alligator" ? "small": "wide";
}
```
#### Multiples of 3 or 5
```javascript
function solution(n){
  if (n < 3) return 0;
  const arr = [];
  for (let i = 0; i < n; i++) {
    if ((i % 3 === 0 || i % 5 === 0) && !arr.includes(i)) arr.push(i);
  }
  return arr.reduce((a, c) => a + c);
}
```
#### Disarium Number (Special Numbers Series #3)
```javascript
const disariumNumber = n =>
  [...String(n)].reduce((total, num, index) => total + Number(num) ** (index + 1), 0) === n ? 'Disarium !!' : 'Not !!'
```
#### STRONGN Strong Number (Special Numbers Series #2)
```javascript
const factorial = n => (n < 0 ? null : n === 0 ? 1 : n * factorial(--n))
const strong = n =>
  [...String(n)].map(Number).reduce((total, digit) => total + factorial(digit), 0) === n
    ? 'STRONG!!!!'
    : 'Not Strong !!'
```
#### Grasshopper - Grade book
```javascript
function getGrade (s1, s2, s3) {
  const a = (s1 + s2 + s3) / 3;
  if (a >= 90) return 'A';
  if (a >= 80 && a < 90) return 'B';
  if (a >= 70 && a < 80) return 'C';
  if (a >= 60 && a < 70) return 'D';
  if (a < 60) return 'F';
}
```
#### Make the Deadfish swim
```javascript
function parse (data) {
  let res = 0;
  const arr = [];
  for (let i = 0; i < data.length; i++) {
    switch (data[i]) {
      case 'i':
        res++;
        break;
      case 'd':
        res--;
        break;
      case 's':
        res *= res;
        break;
      case 'o':
        arr.push(res);
        break;
      }
  }
  return arr;
}
```
#### Grasshopper - Terminal game move function
```Java
public class Move {
    public static int move(int position, int roll) {
        return roll * 2 + position;
    }
}
```
#### Jumping Number (Special Numbers Series #4)
```javascript
const jumpingNumber = n =>
  [...String(n)].every((num, index, array) => index === 0 || Math.abs(num - array[index - 1]) === 1)
    ? 'Jumping!!'
    : 'Not!!'
```
#### Simple Fun #1: Seats in Theater
```javascript
const seatsInTheater = (nCols, nRows, col, row) =>
  (nRows - row) * (nCols - (col - 1))
```











