1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// Your code goes here
let percentage = function(marks , total) {
  return (marks * 100) / total;
}
```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
// Your answer
let percentage = (marks , total)=> {
  return (marks * 100) / total;
}
```

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
};
``function percentage(marks, total) {
  return (marks * 100) / total;
}`

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};
```
function percentage(marks, total) {
  return (marks * 100) / total;
}

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};
```

```js
let percentage = (marks, total) => (marks * 100) / total;
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.

4. Why is a function call an expression in JavaScript?
//calling an function to read the value is function execution. percentage(12,20);
5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); // Answer five = 5;
five = add; // Answer  
 add(a, b) {
  return a + b;
}
five = five(10, 11); // Answer 21
five = function () {
  return 'Hello';
}; // Answer //Hello
```

6. What is the difference between function definition and function call? Explain with an example.
A function is a group of statements that together perform a task. ... A function declaration tells the compiler about a function's name, return type, and parameters. A function definition provides the actual body of the function. The C standard library provides numerous built-in functions that your program can call.
7. What is the similarities between function definition and function call?
function call calls the function name with the values to be outputed.
8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log('Hello World!');
}

hello.user = 'Sam'; // valid or invalid
```
valid

9. What is higher order function explain with an example.
 A Higher-Order function is a function that receives a function as an argument or returns the function as output. For example, Array. prototype. map , Array. prototype
10. Explain what is callback function. Why you can pass a function inside a function?
A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
A callback function is a lucky function that gets passed into the enclosing higher-order function: The callback function gets executed (called) inside the higher order function, but not necessarily immediately. It gets “called back” — hence the name — at whatever point serves the code's purpose