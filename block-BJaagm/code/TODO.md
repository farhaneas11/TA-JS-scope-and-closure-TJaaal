1. What does thread of execution means in JavaScript?
Each unit capable of executing code is called a thread. The main thread is the one used by the browser to handle user events, render and paint the display, and to run the majority of the code that comprises a typical web page or app.
2. Where the JavaScript code gets executed?
JavaScript can execute not only in the browser, but also on the server, or actually on any device that has a special program called the JavaScript engine. The browser has an embedded engine sometimes called a “JavaScript virtual machine”.
3. What does context means in Global Execution Context?
Global execution context (GEC): This is the default execution context in which JS code start its execution when the file first loads in the browser. All of the global code i.e. code which is not inside any function or object is executed inside the global execution context.
4. When do you create a global execution context.
FEC or Functional Execution Code is that type of context which is created by the JavaScript engine when any function call is found. Every function has its own execution context, and thus unlike GEC, the FEC can be more than one.
5. Execution context consists of what all things?
Execution context (EC) is defined as the environment in which the JavaScript code is executed. By environment, I mean the value of this , variables, objects, and functions JavaScript code has access to at a particular time.
6. What are the different types of execution context?
Global execution context (GEC): This is the default execution context in which JS code start its execution when the file first loads in the browser. All of the global code i.e. code which is not inside any function or object is executed inside the global execution context. GEC cannot be more than one because only one global environment is possible for JS code execution as the JS engine is single threaded.
Functional execution context (FEC): Functional execution context is defined as the context created by the JS engine whenever it finds any function call. Each function has its own execution context. It can be more than one. Functional execution context has access to all the code of the global execution context though vice versa is not applicable. While executing the global execution context code, if JS engine finds a function call, it creates a new functional execution context for that function. In the browser context, if the code is executing in strict mode value of this is undefined else it is window object in the function execution context.
Eval: Execution context inside eval function.
7. When global and function execution context gets created?
Whenever the code runs for the first time or when the code is not inside any function then it gets into the global execution context. There is only one global execution context throughout the execution of code. Create a 'window' object. The window object is referenced to 'this' keyword.
8. Function execution gets created during function execution or while declaring a function.
While executing the global execution context code, if JS engine finds a function call, it creates a new functional execution context for that function. In the browser context, if the code is executing in strict mode value of this is undefined else it is window object in the function execution context.

9. Create a execution context diagram of the following code on your notebook. Take a screenshot/photo and store it in the folder named `img`. Use `![](./img/image-name.png)` to display it here.



```js
var user = "Arya";

function sayHello(){
  return `Hello ${user}`;
}

var userMsg = sayHello(user);
```

<!-- Put your image here -->

![](./img/image-name.jpg)



```js
var marks = 400;
var total = 500;

function getPercentage(amount, totalAmount){
  return (amount * 100) / totalAmount;
}

var percentageMarks = getPercentage(marks, total);
var percentageProfit = getPercentage(400, 200);
```

<!-- Put your image here -->

![](./img/image-name.jpg)



```js
var age = 21;

function customeMessage(userAge){
  if(userAge > 18){
    return `You are an adult`;
  }else {
    return `You are a kid`;
  }
}

var whoAmI = customeMessage(age);
var whoAmIAgain = customeMessage(12);
```

<!-- Put your image here -->

![](./img/image-name.jpg)