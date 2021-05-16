Create the execution context diagram for following code. What will be the output in each line of code

```js
function getCounter() {
  let privateCounter = 0;
  function changeBy(val) {
    privateCounter += val;
  }
  return {
    increment: function () {
      changeBy(1);
    },
    decrement: function () {
      changeBy(-1);
    },
    value: function () {
      return privateCounter;
    },
  };
};

let counter = getCounter()

counter.value();  // output 0
counter.increment(); // output 1
counter.increment(); // output 2
counter.value(); // output 2
counter.decrement(); // output 1
counter.value(); // output 1
```
//In the above function the value of privatecounter is 0;
when the counter.value() is read the value stored in the closure baggage is 0;the output will be the same.
next it is the increment function is read.it increments by 1 and is stored in the closure.
again increment function is been read.increments by 2 and stored in the closure.
now when the value() is been read the value in closure is been displayed which is 2.
decrement() function decrements the value by 1.now the value in closure baggage is 1.
now the value() is been read the value 1 stored in the closure is been displayed.

2. Create the execution context diagram and write the output.

```js
function makeCounter() {
  let privateCounter = 0;
  function changeBy(val) {
    privateCounter += val;
  }
  return {
    increment: function() {
      changeBy(1);
    },

    decrement: function() {
      changeBy(-1);
    },

    value: function() {
      return privateCounter;
    }
  }
};

let counter1 = makeCounter();
let counter2 = makeCounter();

console.log(counter1.value());  // OUTPUT 0

counter1.increment();
counter1.increment();
console.log(counter1.value()); // OUTPUT 2

counter1.decrement();
console.log(counter1.value()); // OUTPUT 1
console.log(counter2.value()); // OUTPUT 0
```