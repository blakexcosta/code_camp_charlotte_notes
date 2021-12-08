### 11.1 functions as values:

- functions are data types

- i.e. `console.log(typeof Number);  // returns function`

- functions may be assigned to variables

  - ```javascript
    function hello() {
    
       // function body
    
    }
    
    let helloFunc = hello;
    ```

- the above examples creates an alias to hello

- and because they're values they can be uesd like general values in javascript



### 11.2 anonymous functions

- normal functions are called **named functions**

- **anonymous functions** are functions that don't have names. the need to end with a semilcolon when used like below

  - ```javascript
    let add = function(a, b) {
       return a + b;
    };
    
    console.log(add(1, 1));
    ```



### 11.3 passing functions as arguments

- using setTimeout  (it's a predefined function, that takes a function as an argument):

  - ```javascript
    function printMessage() {
       console.log("The future is now!");
    }
    
    setTimeout(printMessage, 5000);
    ```

- it's common to use an anonymous function as an argument to a function that requires one

  - ```javascript
    setTimeout(function () {
       console.log("The future is now!");
    }, 5000);
    ```

- using map  array method. map doesn't alter original array

  - ```javascript
    // format: let mappedArray = someArray.map(functionName);
    let nums = [3.14, 42, 4811];
    
    let timesTwo = function (n) {
       return n*2;
    };
    
    let doubled = nums.map(timesTwo);
    
    console.log(nums);
    console.log(doubled);
    ```

- map is often used with an anoymous function

  - ```javascript
    let nums = [3.14, 42, 4811];
    
    let doubled = nums.map(function (n) {
       return n*2;
    });
    
    console.log(doubled);
    ```



### 11.4 Receiving function arguments

- ​	examplewith a simple logger

  - ```javascript
    let fileLogger = function(msg) {
    
       // Put the message in a file
    
    }
    
    function logError(msg, logger) {
       let errorMsg = 'ERROR: ' + msg;
       logger(errorMsg);
    }
    
    logError('Something broke!', fileLogger);
    ```

- more complex example:

  - ```javascript
    let fileLogger = function(msg) {
       // Put the message in a file
    
    }
    
    let consoleLogger = function(msg) {
       console.log(msg);
    }
    
    function logError(msg, loggers) {
       let errorMsg = 'ERROR: ' + msg;
       for (let i = 0; i < loggers.length; i++) {
          loggers[i](errorMsg);
       }
    }
    
    logError('Something broke!', [fileLogger, consoleLogger]);
    ```

- you will get a typeerror if a function is expected in a function and one is not provided



### 11.5 why use anonymous functions

- they can be single use
- they're ubiquitous in js



### 11.6 Recursion

- functions can call other functions
- **Recursion** is the process of solving a larger problem by breaking it into smaller pieces that *can all be solved in exactly the same way*
  - instead of loop, function can call itself over and over again



### 11.7 Recursion walkthrough

- identify the base case

  - if the base case is true, then process else

  - ```javascript
    function combineEntries(arrayName){
       if (baseCase is true){
          //solve last small step
          //end recursion
       } else {
          //call combineEntries again
       }
    }
    ```



### 11.8 MAking a function call itself

- completed recursion example:

  - ```javascript
    function combineEntries(arrayName){
       if (arrayName.length <= 1){
          return arrayName[0];
       } else {
          return arrayName[0]+combineEntries(arrayName.slice(1));
       }
    }
    
    
    let arr = ['L', 'C', '1', '0', '1'];
    
    console.log(combineEntries(arr));
    
    ```

- 