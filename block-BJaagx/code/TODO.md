
1. Which all function is Higher order function and which one is a callback function in the code given below.

```js
let marks = [34, 45, 56, 76];
function multiplyArrayByN(arr, cb) {
  let finalArr = [];
  for (let elm of arr) {
    finalArr.push(cb(elm)); 
  }
  return finalArr;
}
function addFive(n) {
  return n + 5;
}
function multiplyBy5(n) {
  return n * 5;
}
//higher order function
let numbersAddedFive = multiplyArrayByN(marks, addFive);//callBack Function
let numbersMultipliedBy5 = multiplyArrayByN(marks, multiplyBy5);//callBack Function
```

2. Create the execution context diagram of the above code snippet
Global Execution Context:
creation context()
marks is created empty as its let.
multiplyArrayByN() created as function.
addFive()  created as function.
multiplyBy5() created as function.

execution context()
marks is given the array of values.as its stored into the memory.
numbersAddedFive is read as it contains an function to be read for execution.multiplyArrayByN() has two arguments and for the execution two function is read as the argument for the execution.marks is the array of values.and addfive is an function.inside the multiplyArrayByN()
finalArr.push(cb(elm)) we read eaach element in the marks as i < 4;the four elemnts in the marks is been read using the above function for the execution using the  addFive.cb(elm) is just like addFive(n).the n elemets are added to five for the execution and we get the ouput as [39, 50, 61, 81]. the same is done for the numbersMultipliedBy5 parameter where the function is been read and executed.After the execution the function is deleted from the global execution for reading next function or parameter.

3. Write a higher order function that accepts a number and a operation function (callback function). Call the callback function passing the number as argument and return the returned value.

```js
function operation(n, opFn) { 
  return opFn(n);
}
// TEST
console.log(
  operation(21, function (n) {
    return n / 10;
  })
);
// Output: 2.1
console.log(
  operation(10, function (n) {
    return (n * n) / 5;
  })
);
// Output: 20
```

4. Write a higher order function that accepts a string and a operation function (callback function). Call the callback function passing the string as argument and return the returned value.

```js
function operation(str, opFn) {
  // your code goes her
  return opFn(str);
}
// TEST
console.log(
  operation("Learning to fly", function (text) {
    return text.toUpperCase();
  })
);
// Output: "LEARNING TO FLY"
console.log(
  operation("Higher Order Fucntion", function (text) {
    return text.split(" ");
  })
);
// Output: ["Higher","Order","Function"]
```
