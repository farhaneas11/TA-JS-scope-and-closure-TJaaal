Create the execution context diagram for the following code snippets:

```js
function outer() {
  let b = 10;
  function inner() {
    let a = 20;
    console.log(a + b);
  }
  return inner;
}
let getSum = outer();
let num = getSum();
```
//In the above problem we can see that the inner is an inner function of the outer function.
IN the memory when global execution context is in deployed or creation context the outer is created as a function in the memory.
getsum is created as empty and num is also empty created.
//in execution context ,outer gets called from the getSum ,execution context for the getsum is created in GEC .The outer is a function as we can see in the memory.when the function reaches the return inner,a and b is created and in the extra baggage with the value of 10 and 20 but the console.log(a+b)wont be included in the getsum.but it will be stored in closure baggage in the memory.after the function is been read the 30 is been stored in the closure and but the output recieved for getsum is the function inner.
//when num is read,getsum is been read from the num.Same as before but the closure baggage is having console.log(a+b) and value of a,b plus the added value.
so the num will read the sum value from the getsum closure baggage and been outputed.
2.

Create the execution context diagram for following code. Also write the output of the code below.

```js
function getCounter() {
  let count = 0;

  return () => {
    return count++;
  };
}

let counter = getCounter();

counter(); // output
counter(); // output
counter(); // output
counter(); // output
```
//When GEC is created getcounter is created as a function.and counter is created empty in the memory.
//In the execution,when is counter is executed for the first time.It will read the whole function as it is,when count is come across ,it will be read  and stores the count value in the closure baggage as the return function is created as a function.
//when counter is called again the count value 0 from the baggage is been outputed and the value of count increases into 1 in the baggage closure.
/when counter is called again the value 1 is been outputed and the value in the baggage is been changed into 2;
//the value gets counted as the number is times its called.
//In the last counter the value outputed will be 3 and closure baggage is counted into 4.
3. Create the execution context diagram

```js
function makeColorChanger(color) {
  return function () {
    document.body.style.backgroundColor = color;
  };
}

let blue = makeColorChanger('blue');
let tomato = makeColorChanger('tomato');

blue();
tomato();

// What will be the background color after the execution of last line
tomato will be the color.
```
