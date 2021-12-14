### 13.1 What are modules?

- modules allow us to keep features of our program in separate, smallerm pieces.
- modules help keep our project organized



### 13.2 Require modules

- importing modules

  - ```javascript
    const input = require('readline-sync');
    
    let name = input.question("What is your name?");
    console.log(`Hello, ${name}`);x const input = require('readline-sync');let name = input.question("What is your name?");console.log(`Hello, ${name}`);
    ```

- modules are either single functions or objects that contain multiple functions

- If the filename passed to `require` does NOT start with `./` or `../`, then Node checks two resources for the module requested.

  1. Node looks for a Core module with a matching name.
  2. Node looks for a module installed from an external resource like NPM.

- the modules we keep track of are stored in `package.json`



### 13.3 NPM

- npm has two main parts:
  1. A registry of modules.
  2. Command line tools to install modules.
- CAN add modules to replit via the packages button in replit



### 13.4 Exporting Modules

- every node file is treated as a module/package

- from a file we can export a single function or set of functions

- only ONE module.exports is allowed per file

- exporting a single function:

  - ```javascript
    function isPalindrome(str){
      return str === str.split('').reverse().join('');
    }
    
    
    module.exports = isPalindrome;
    ```

- using single function:

  - ```javascript
    const palindromeCheck = require('./practiceExports.js');
    
    console.log(typeof palindromeCheck);
    console.log(palindromeCheck('that'));
    console.log(palindromeCheck('radar'));
    ```

- exporting multiple functions:

  - ```javascript
    function isPalindrome(str){
      return str === str.split('').reverse().join('');
    }
    
    function evenOrOdd(num){
      if (num%2===0){
          return "Even";
      } else {
          return "Odd";
      }
    }
    
    function randomArrayElement(arr){
      let index = Math.floor(Math.random()*arr.length);
      return arr[index];
    }
    
    
    module.exports = {
       isPalindrome: isPalindrome,
       evenOrOdd: evenOrOdd,
       randomArrayElement: randomArrayElement
    }
    
    ```

- using multiple functions

  - ```javascript
    const practice = require('./practiceExports.js');
    
    console.log(practice.isPalindrome('mom')); // notice dot notation, as it's an object. could technically do  console.log(practice["isPalindrome"]("mom")); but dont do this way. it's ugly
    console.log(practice.evenOrOdd(9)); 
    
    ```

    



