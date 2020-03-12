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
#### Product Of Maximums Of Array (Array Series #2)
```javascript
const maxProduct = (n, s) => n.sort((a, b) => b - a).slice(0, +s).reduce((a, c) => a * c, 1);
```
#### Palindrome Strings
```javascript
const isPalindrome = (line) => line.toString() === line.toString().split('').reverse().join('');
```
#### Primorial Of a Number
```javascript
function numPrimorial(n){
  const num = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97, 101, 103, 107, 109, 113 , 127, 131, 137, 139, 149];
  return num.slice(0, n).reduce((a, b) => a * b);
}
```
#### Balanced Number (Special Numbers Series #1 )
```javascript
function balancedNum(number){
    const n = number.toString().split('');
    if (n.length < 3) return "Balanced";
    let a = 0, b = 0;
    for (let i = 0, j = n.length - 1; i < (n.length/2)-1; i++, j--){
      a += +n[i];
      b += +n[j];
    }
    return a === b? "Balanced": "Not Balanced";
}
```
#### Beginner Series #4 Cockroach
```java
public class Cockroach{
  public int cockroachSpeed(double x){
    return (int)Math.floor(x / 0.036);
  }
}
```
#### Minimum to multiple
```javascript
const minimum = (a, x) => !a % x ? 0: Math.min(a % x,((1 + Math.floor(a / x)) * x) - a);
```
#### 1/n- Cycle
```javascript
function cycle(n) {
  if (n % 2 == 0 || n % 5 == 0) return -1;
  let i = 0, val = 1;
  while (++i) {
    val = val * 10 % n;
    if (val == 1) return i;
  }
}
```
#### Help Bob count letters and digits.
```javascript
function countLettersAndDigits(input) {
  let match = input.match(/[a-z0-9]/gi);
  return match === null ? 0 : match.length;
}
```
#### Will you survive the zombie onslaught?
```javascript
function zombie_shootout(zombies, range, ammo) {
  let step = range * 2;
  if (ammo < step && zombies > ammo)
    return `You shot ${ammo} zombies before being eaten: ran out of ammo.`;
  if (zombies > step)
    return `You shot ${step} zombies before being eaten: overwhelmed.`;
  return `You shot all ${zombies} zombies.`;
} 
```
#### A disguised sequence (I)
```javascript
let fcn = n => 2 ** n;
```
#### Thinking & Testing : True or False
```javascript
function testit(n){
  return n.toString(2).replace(/0/g,'').length
}
```
#### Drying Potatoes
```javascript
const potatoes = (p0, w0, p1) => Math.floor(w0 * (100 - p0) / (100 - p1));
```
#### Arrh, grabscrab!
```javascript
function grabscrab(anagram, dictionary) {
  anagram=anagram.split('').sort().join();
  let arr = dictionary.slice().map(v=>v.split('').sort().join()===anagram);
  return dictionary.filter((v,i)=>arr[i]===true);
}
```
#### Complete The Pattern #1
```javascript
function pattern(n){
 if (n < 1) return '';
 let output="1";
   for (let i = 2; i <= n; i++) {
    output += '\n' + String(i).repeat(i);
   }
 return output;
}
```
#### No oddities here
```javascript
const noOdds = ( values ) => values.filter(el => el % 2 === 0);
```
#### Row of the odd triangle
```javascript
function oddRow(n) {
  let a = 1;
  for (let i = 2, b = 2; i <= n; i++, b += 2) {
    a += b;
  }
  let arr = [];
  for (let i = 1; i <= n; i++, a += 2) {
    arr.push(a);
  }
  return arr;
}
```
#### What will be the odd one out?
```javascript
function oddOneOut(str) {
   let arr = str.split('');
   let result = [];
   let a;
   for (let i = 0; i < arr.length; i++) {
     a = arr.indexOf(arr[i], i+1);
     console.log(arr.indexOf(arr[i]), arr.lastIndexOf(arr[i]),arr.indexOf(arr[i], i+1));
       if (arr.indexOf(arr[i]) !== arr.lastIndexOf(arr[i])) {
       delete arr[i];
       delete arr[a];
       result.push(arr[i]);
       }
   }
   return arr.join('').split('');
}

function oddOneOut(str) {
  const obj = {}, result = [];
  for (let i = 0; i < str.length; i++) {
    if (obj[str[i]]) obj[str[i]]++;
    else obj[str[i]] = 1;
    if (str.lastIndexOf(str[i]) === i && obj[str[i]] % 2 !== 0)
      result.push(str[i]);
  }
  return result;
}
```
#### Holiday VI - Shark Pontoon
```javascript
const shark = (pD, sD, yS, sS, d) => d === true ? pD/yS < sD/(sS/2) ? "Alive!": "Shark Bait!": pD/yS < sD/sS ? "Alive!": "Shark Bait!";
```
#### Pandemia 🌡️
```javascript
function infected(s) {
  if (!s.includes(0) && !s.includes(0)) return 0;
  let total = 0, infected = 0;
  s = s.split('X');
  for (let i = 0; i < s.length; i++) {
    total += s[i].length;
    if (s[i].includes(1)) infected += s[i].length;
  }
  return 100*infected/total;
}
```
#### Convert string to camel case
```javascript
function toCamelCase(str) {
  return str.replace(/[_-]([a-z])/ig, (_, c) => c.toUpperCase())
}
```
Area or Perimeter
```java
public class Solution {
    public static int areaOrPerimeter (int l, int w) {
        return l == w ? l * w : (l + w) * 2;
    }
}
```
#### Break camelCase
```javascript
function solution(str) {
  str = str.split('');
  let result = [];
  for (let i = 0; i < str.length; i++) {
    if (str[i] === str[i].toUpperCase()) result.push(' ');
    result.push(str[i]);
  }
  return result.join('');
}
```
#### Sum of Minimums!
```javascript
function sumOfMinimums(arr) {
  let result = 0;
  for (let i = 0; i < arr.length; i++) {
    result += Math.min(...arr[i]);
  }
  return result;
}
-----------------------------------------------------
const sumOfMinimums = (arr) => arr.reduce((a, b) => a + Math.min(...b), 0);
```
#### Sum of Triangular Numbers
```javascript
function sumTriangularNumbers(n) {
let sum = 0;  
for(var i = 1; i <= n; i++) {
  sum += (i*(i+1))/2;
}
return sum;
}
```
#### Color Choice
```javascript
function checkchoose(m, n) {
  let x = 1;
  for (let i = 1; i < n; i++) {
    x = Math.round(x * (n + 1 - i) / i)
    if (x == m) 
      return i;
  }
  return -1;
}
```
#### Find the Mine!
```javascript
function mineLocation(field){
  for (var i = 0; i < field.length; i++)
    for (var j = 0; j < field[i].length; j++)
      if (field[i][j] === 1)
        return [i, j];
}
```
#### "Very Even" Numbers.
```javascript
function isVeryEvenNumber(n) {
  if (n < 10 && n%2 === 0) return true;
  return (n > 9) ? isVeryEvenNumber(String(n).split('').reduce((a,b) => +a + +b)) : false;
}
```
#### noobCode 01: SUPERSIZE ME.... or rather, this integer!
```javascript
const superSize = (num) => Number(String(num).split('').sort((a, b) => b - a).join(''));
```
#### Chocolate Party
```javascript
function shareChocolate(n) {
  if (n < 1 || n%1 !== 0) return null;
  let tables = [0,0,0,0,0,0], i = 0;
  for(let i = 0; i < n; i++) {
    let chocolate = tables.map((kids, choco) => kids ? (choco+1)/(kids+1) : choco+1)
    const idx = chocolate.indexOf(Math.max(...chocolate))
    tables[idx]++;
  }
  return tables;
}
```
#### Extra Perfect Numbers (Special Numbers Series #7)
```javascript
function extraPerfect(n){
  let arr = [1];
  for (let i=3;i<=n;i+=2){
  arr.push(i);
  }
  return arr;
}
```
#### Sort Out The Men From Boys
```javascript
const menFromBoys = arr => {
  const arrWithoutDuplicates = [...new Set(arr)]
  const evenNumbers = arrWithoutDuplicates.filter(number => number % 2 === 0).sort((a, b) => a - b)
  const oddNumbers = arrWithoutDuplicates.filter(number => number % 2 !== 0).sort((a, b) => b - a)

  return [...evenNumbers, ...oddNumbers]
}
```
#### Card Game
```javascript
function cardGame(card1, card2, trump) {
    function compare(card1, card2, trump) {
        const allRanks = '2345678910JQKA';
        if ([card1, card2].includes('joker')) return (card1 === 'joker') - (card2 === 'joker');
        const suits = [card1.slice(-1), card2.slice(-1)];
        if (suits[0] === suits[1]) return allRanks.indexOf(card1[0]) - allRanks.indexOf(card2[0]);
        if (suits.includes(trump)) return (suits[0] === trump) - (suits[1] === trump);
        return 0;
    }
    if (card1 === card2)
        return 'Someone cheats.';
    let cmp = compare(card1, card2, trump);
    return (cmp === 0) ? 'Let us play again.' : `The ${(cmp > 0)? 'first': 'second'} card won.`;
}
```
#### Esoland MiniBitMove
```javascript
function interpreter(tape, array) {
    let tapeIdx = 0, index = 0;
    array = array.split("").map(a=>+a);
    while(index != array.length){
        (tape[tapeIdx] === '0') ? index++ : array[index] = ~~!(array[index]);
        (tapeIdx >= tape.length-1) ? tapeIdx = 0: tapeIdx++;
    }
    return array.join("");
}
```
#### Simple Fun #303 Prime Product
```javascript
function isPrime(n) {
    if(n === 2) { return true;}
    if(n <= 1 || n % 2 === 0) { return false;}
    for(let i = 3; i <= ~~Math.sqrt(n); i+=2) {
        if(n % i === 0) {
            return false;
        }
    }
    return true;
}

let primeProduct = function(n) {
    if(n <= 3) { return 0; }
    for(let i = ~~(n/2); i > 0; i--) {
        if(isPrime(n-i) && isPrime(i)) {
            return (n-i) * i;
        }
    }
    return 0;
}
```
#### N-th Power
```javascript
function index(array, n){
  if (n >= array.length) return -1;
  return Math.pow(array[n], n);
}
```
#### Find the Difference in Age between Oldest and Youngest Family Members
```javascript
const differenceInAges = ages => [Math.min(...ages), Math.max(...ages), Math.max(...ages) - Math.min(...ages)];
```
#### Form The Minimum
```javascript
const minValue = v => +v.filter((el, i) => v.indexOf(el) === i).sort((a, b) => a - b).join('');
```
#### Experimenting with a sequence of complex numbers
```javascript
let f = (x, y, eps) => Math.max(-1,Math.log(eps)/Math.log(Math.hypot(x,y)));
```
#### Build a pile of Cubes
```javascript
let findNb = function(n) {
  let sum = 0, idx = 1;
  
  while(sum < n) {
    sum += Math.pow(idx, 3);
    idx += 1;
  }
  
  return (sum === n) ? idx-1 : -1;
}
```
#### Fantabulous Birthday
```javascript
function fantabulousBirthday(S){
    let row, col, n = Math.round(Math.sqrt(S));
    Math.pow(n, 2) >= S? col = n * n - S + 1 : col = S - n * n;
    Math.pow(n, 2) >= S? row = n : row = n + 1;
    return n & 1? [col, row] : [row, col];
}
```
#### Master of Files
```javascript
String.prototype.isAudio = function() {
  return /^[a-zA-Z]+\.(mp3|flac|alac|aac)$/.test(this);
}

String.prototype.isImage = function() {
  return /^[a-zA-Z]+\.(jpg|jpeg|png|bmp|gif)$/.test(this);
}
```
#### Errors Histogram
```javascript
function hist(s) {
  let obj = {u: 0, w: 0, x: 0, z: 0};
  s.split('').forEach(x => {if (x in obj) obj[x]++});
  return Object.entries(obj).filter(([a, x]) => x).map(([a, x]) => `${a}  ${x}     ${'*'.repeat(x)}`).join('\r');
}
```
#### Consonant Value
```javascript
const solve = s => Math.max(...s.split(/[aeiou]+/).map(group => group.split('').reduce((a,b) =>a + b.charCodeAt()-96,0))); 
```
#### Schrodingers Boolean
```javascript
class OmniBool {
  constructor() {
    this.n = false;
  }
}

OmniBool.prototype[Symbol.toPrimitive] = function() { 
  this.n = !this.n;
  return this.n;
};

let omnibool = new OmniBool(); 
```
#### Braces Status
```javascript
function bracesStatus(str){
  str = str.replace(/[^\(\)\[\]\{\}]/g, '');
  while (/\(\)|\[\]|\{\}/.test(str)) 
    str = str.replace(/\(\)|\[\]|\{\}/g, '');
  return (str.length < 1);
} 
```
#### Count Letters In String
```javascript
function letterCount(s){
  let res = {};
  [...s].sort((a, b) => a - b).forEach(el => res[el] ? res[el]++ : res[el] = 1)
  return res;
}
```
#### Backwards Read Primes
```javascript
let backwardsPrime = function(min, max) {
    let arr = [];
    for(let i = min; i <= max; i++) {
        let backwardNum = reverseNum(i);
        if(isPrime(i) && isPrime(backwardNum) && i != backwardNum){
            arr.push(i);
        }
    }
    return arr;
}

function reverseNum(n) {
    return Number(n.toString().split("").reverse().join(""));
}

function isPrime(n) {
    if(n === 2 || n === 3) { return true; }
    if(n % 2 === 0 || n < 2) { return false; }
    for(let i = 3; i <= Math.sqrt(n); i+=2) {
        if(n % i === 0) {
            return false;
        }
    }
    return true;
}
```
#### ASCII Fun#1 X-Shape
```javascript
function x(n) {
    let arr = Array(n).fill().map(_ => "□".repeat(n).split(""))
    for(let i = 0; i < arr.length; i++) {
        [arr[i][i], arr[i][arr.length-1-i]] = ["■","■"];
    }
    return arr.map(a=>a.join("")).join("\n");
}
```


