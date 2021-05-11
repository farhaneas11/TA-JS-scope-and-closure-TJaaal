To create the execution context diagram consider the following:

- Global and Function Execution Context
- Different Phases Of Execution Context
- Var let and const

Create the execution context diagram of the following code line by line.

```js
let num = 21;
function square(num) {
  return num * num;
}
let hundred = square(10);
console.log(hundred);
```
creation()
num:undefined;
square:fn();
hundred : undefined 
Create the execution context diagram of the following code line by line.
execution()
num:21;
square:fn();
hundred : undefined  - execution context
where arguments{:10 , length:1}
hundred:100;
```js
var num = 21;
function addFive(n) {
  return n + 5;
}
var five = addFive(0);
var ten = addFive(5);
console.log(five, ten); expression statement
```
creation()
num:undefined;
addfive:fn();
five : undefined;
ten:undefined; 

execution()
num:21;
addfive:fn();
five : undefined  - execution context reads the function addfive(n)
where arguments{:0 , length:1}
five:5;
ten : undefined  - execution context reads the function addfive(n)
where arguments{:5 , length:1}
ten:10;
Create the execution context diagram of the following code line by line.

```js
let marks = [34, 45, 56, 76];
function multiplyArrayByN(arr, n) {
  let finalArr = [];
  for (let elm of arr) {
    finalArr.push(elm * 2);
  }
  return finalArr;
}

let numbers = multiplyArrayByN(marks);
```
creation()

let marks:undefined
multiplyArrayByN:fn();
numbers:undefined;

execution()
marks = [34, 45, 56, 76];
numbers:statement identifieer is read in the execution context table.
numbers: [68, 90, 112, 152]
Create the execution context diagram of the following code line by line.

```js
counter();
function counter(){
  let count = 0;
  funciton increment(){
    return count++;
  }
  return increment()
}
```
arguments: { length: 0 }
this: window
count: 1
increment: fn()
Create the execution context diagram of the following code line by line.

```js
counter();
let counter = function () {
  let count = 0;
  function increment() {
    return count++;
  }
  return increment();
};
```
window: global object
this: window
counter: fn()