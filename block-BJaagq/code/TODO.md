Create a execution context diagram of the following code on your notebook. Take a screenshot/photo and store it in the folder named `img`. Use `![](./img/image-name.png)` to display it here.

- Take in account the different phases of execution, different execution contexts

1.

```js
var species = 'human';

function change() {
  var species = 'vampire';
  console.log(species);
}

console.log(species); // 1
change();
console.log(species); // 2
```

<!-- Put your image below -->
//Here we can see that var species is given as global variable in first line.But in the function the var species is given as local variable for the function.SO in the memory the global varibale will be saved and the function name will be saved first.When the console log is been read the species variable will be read from the memory of species as it is the global variable.when function change is read the output will be the local variable inside the function change.
//value of species on 1 and 2 will be global value 'human'
![](./img/image-name.jpg)

- Create the execution context diagram
- What will be the value of species on 1 and 2

2.

```js
var topLevelVar = 'This is global scope!';

function topLevelFn() {
  var localVar = "This is local to topLevelFn's scope";

  function nestedFn() {
    var anotherLocalVar = "Local to nestedFn's scope.";

    console.log(localVar); // 1
    console.log(topLevelVar); // 2
  }

  nestedFn();
}

topLevelFn();
```

<!-- Put your image below -->
//Here as we saw in the above problem there is gloval variable and a function which has function inside it.first the main function and the global variable is stored in memory.
//When the function is called the function is read and in the end of it there is the inside fucntion is been called.Inside the function the console log is been read and the values of the console log is been outputed as the global variable and the main function value is also been consoled.
after giving the ouput the function gets deleted.
![](./img/image-name.jpg)

- Create the execution context diagram
- What will be the value of 1 and 2

3.

```js
var one = 'One';
var two = 'Two';

function main() {
  var three = 'Three';

  function inner() {
    var four = 'Four';

    console.log(one); // 1
    console.log(two); // 2
    console.log(three); // 3
  }
  console.log(four); // 4
  inner();
}

main();
console.log(one, two, three, four); // 5
```

<!-- Put your image below -->
//Here as we saw in the above problem there is gloval variable and function inside one fucntion..first the main function and the global variable is stored in memory.
//When the function is called the function is read and in the end of it there is the inside fucntion is been called.Inside the function the console log is been read and the values of the console log is been outputed as the global variable and the main function value is also been consoled.
after giving the ouput the function gets deleted.
![](./img/image-name.jpg)

- Create the execution context diagram
- What will be the value of 1, 2, 3, 4 and 5 or error if the code does not work
