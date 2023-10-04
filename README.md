# JavaScript Practice

- [ProtoType](#ProtoType)
- [Window](#Window)
  - [GlobalScope](#GlobalScope)
  - [DOMAccess](#DOMAccess)
  - [Timers](#Timers)
  - [LocationInformation](#LocationInformation)
  - [Storage](#Storage)
- [Function](#FunctionInJavascript)
  - [DefineAFunction](#DefineAFunction)
  - [FunctionParameters](#FunctionParameters)
  - [ReturnInFunction](#ReturnInFunction)
  - [FunctionExpression](#FunctionExpression)
  - [AnonymousFunction](#AnonymousFunction)
  - [ArrowFunctions](#ArrowFunctions)

  ### ProtoType
  ```js
    const bercelona = {
      jerseyNumber: '',
      name: '',
      country: '',
      position: '',
  
      __proto__: {
          bercelonaPlayer: false,
  
          playerRegistration(jerseyNumber, name, country, position){
              this.jerseyNumber = jerseyNumber;
              this.name = name;
              this.country = country;
              this.position = position;
  
              console.log(`You are succesfully signup for FC Barcelona`);
          },
  
          playerIdentify(jerseyNumber, name){
                  if(this.jerseyNumber !== jerseyNumber || this.name !== name ) return;
                  this.bercelonaPlayer =  true;
              }
          }
      };
  
  bercelona.playerRegistration(10, 'Lionel Messi', 'Argentina', 'Forward');
  // bercelona.playerIdentify(10, 'Lionel Messi');
  bercelona.playerIdentify(30, 'Lionel Messi');
  
  if (bercelona.bercelonaPlayer) {
      console.log(`Welcome to Mr. ${bercelona.name} not the Barcelona's world`);
  } else {
      console.log(`Sorry, You are not Bercelona player!`);
  }
  
  console.log(bercelona);
  ```


### Window
 In JavaScript, a "window" refers to the global object that represents the web browser's window or tab in which your JavaScript code is running. The window object provides access to various properties and methods that allow you to interact with and control the browser environment. Here are some key aspects of the window object:

### GlobalScope
 Variables and functions declared in the global scope are attached to the window object. For example, if you declare a variable like var x = 10; at the top level of your JavaScript code, you can access it as window.x or simply x.
```js
  var x = 10;
  console.log(window.x) // the result will be same
  console.log(x) // the result will be same
```
### DOMAccess
You can use the window object to access and manipulate the Document Object Model (DOM) of the web page. For instance, window.document refers to the DOM of the current page, and you can use it to modify the content and structure of the page.

```js
  document.getElementById(#---)
```

### Timers 
The window object provides methods for working with timers, such as setTimeout and setInterval, which allow you to execute code after a specified delay or at regular intervals.

```js
  function func(){
      console.log("Ran")
  }
  setInterval(func,1000)//Runs the "func" function every second
```

### LocationInformation
You can access and manipulate the URL of the current page using window.location. This allows you to navigate to other pages, modify the URL, or extract information from it.

```js
  console.log(window.location);
  console.log(location.host); // 127.0.0.1:5500
  console.log(location.hostname); // "127.0.0.1"
  console.log(location.href); //"http://127.0.0.1:5500/index.html"

```

### Alerts
JavaScript can create alert boxes and dialogs using methods like window.alert(), window.confirm(), and window.prompt(). These are often used for user interaction.

```js
  window.alert('Welcome to javascript "window"');
  window.confirm('Are you sure you would like to play with javascript window?');
  window.prompt('Hello coders');

```

###Event Handling
The window object can be used to attach event handlers to various global events, such as window.onload to run code when the page finishes loading.

```js
  window.onload = function() {
    alert('The page has loaded')
  };

```

### Storage
You can use window.localStorage and window.sessionStorage to store data persistently or temporarily on the user's device.

```js
  ocalStorage.setItem('Karim', 'Abdul') //key: string, value: string
  localStorage.getItem('karim') // key: string

```

### FunctionInJavascript
Functions are the basic building block of JavaScript. Functions allow us to encapsulate a block of code and reuse it multiple times.
Functions make JavaScript code more readable, organized, reusable, and maintainable.

In JavaScript, a function can be defined using the function keyword, followed by the name of a function and parentheses. Optionally, a list of input parameters can be included within the parentheses. The code block that needs to be executed when the function is called is written within curly braces.

### DefineAFunction
```js
function greet(){
    // alert('This is javascript function');
};
greet();
```

### FunctionParameters
You can pass values to a function using parameters. A function can have one or more parameters, and the values will be passed by the calling code.

```js
function greetings(firstName, lastName){
    console.log(`Hello ${firstName} ${lastName}`);
};
greetings('Steve', 'Jobs');
```

### ReturnInFunction
A function can return a value to the calling code using the return keyword followed by a variable or a value

```js
function getNumber() {
    return 10;
};

let result = getNumber();
console.log(result);
```

### FunctionExpression
A function expression in JavaScript is a function that is stored as a value, and can be assigned to a variable or passed as an argument to another function.

```js
let add = function(num1, num2){
    return num1 + num2;
};

let addResult = add(97, 5);
console.log(addResult);
```

### AnonymousFunction
In JavaScript, you can also create anonymous functions, which are functions without a name. Anonymous functions are often used as arguments to other functions, and are
Anonymous functions are typically used in functional programming e.g. callback function, creating closure or immediately invoked function expression.

```js
let numbers = [2,5, 8, 7, 5];

let squareNumbers = numbers.map(function(number){
    return number * number;
});

console.log(squareNumbers);
```

### ArrowFunctions
Arrow functions are a shorthand syntax for defining anonymous functions in JavaScript. They have compact syntax compared to anonymous functions.

```js
let square = num => num * num;

let squareResult = square(97);
console.log(squareResult);
```

















