### 10.1 Introduction

- **function** = reusable, callable piece of code.
  - **method** = function that specifically belongs to an object
    - all methods are functions but not all functions are methods
- **Encapsulation** = process of packaging up code in a reusable way, without programmer needing tobe concerned with how it works.



### 10.2 Using Functions

- **function call** = act of using a function by referring to name followed by parenthesis
  - aka **function invocation/invoking a function**
- if function doesn't provide explicit return value, special value *undefined* will be returned
- **side effect** = calling a function results in an action that changes the state of a program outside of the function itself
  - ex:) Calling `console.log` results in output to the console



### 10.3 Creating functions

- creating function

  - ex:) 

    ```javascript
    function printNames(names) {
       for (let i = 0; i < names.length; i++) {
          console.log(names[i]);
       }
    }
    ```

- three components of function

  1. function name
  2. parameters
  3. function body

- **Abstraction** = process of taking something specific and making it more general



### 10.4 Function Input and Output

- using return 

  - ex:) 

    ```javascript
    function sumToN(n) {
       let sum = 0;
       for (let i = 0; i <= n; i++) {
          sum += i;
       }
       return sum;
    }
    
    console.log(sumToN(3));
    ```

- return is technically optional. but will return undefined

  - ex:) 

    ```javascript
    function doNothing() {}
    
    let returnVal = doNothing();
    console.log(returnVal);
    ```

- parameters vs arguments:

  - argument = specific value used during function call

    - ex:) 

      ```javascript
      console.log(hello("Lamar")); // the argument is lamar	
      ```

  - parameter = part of function definition and behaves like variable

    - ex:) 

      ```javascript
      function hello(name) { // name is parameter
         return `Hello, ${name}!`;
      }
      ```

- arguments are optional in js

  - ex:) 

    ```javascript
    function hello(name) {
       return `Hello, ${name}!`;
    }
    
    console.log(hello()); // will print undefined, will not error out
    ```

- giving default value to function

  - ex:) 

    ```javascript
    function hello(name = "World") {
       return `Hello, ${name}!`;
    }
    
    console.log(hello());
    console.log(hello("Lamar"));
    ```

- can call a function in js with more arguments than parameters. will just not use extra arguments

  - ex:) 

    ```javascript
    function hello(name = "World") {
       return `Hello, ${name}!`;
    }
    
    console.log(hello("Jim", "McKelvey")); // will print 'Hello, Jim!'
    ```

  - though technically.... you could access the McKelvey variable with `arguments` special object. but not covered in course



### 10.5 a good function-writing process

- create the basic structure
- write the body
- test every few lines or so



### 10.6 Parameters and variables

- **scope** = extent to which a variable is visible within a program

- variable shadowing. i.e. a variable defined outside of a function may be used inside of it:

  - ex:) 

    ```javascript
    let message = "Hello, World!";
    
    function printMessage() {
       console.log(message);
    }
    
    printMessage();
    ```

- *avoid naming variables and function parameters the same name*



### 10.7 Naming Functions

- use camelCase
- use verb/noun pairs
- use descriptive names
- use is/has for boolean functions



### 10.8 Composing Functions

- palindrome check

  - ex:) 

    ```javascript
    function reverse(str) {
       let reversed = '';
    
       for (let i = 0; i < str.length; i++) {
          reversed = str[i] + reversed;
       }
    
       return reversed;
    }
    ```

- functions should do only *one* thing (SOC)

### 10.9 why create functions?

- because. They are important. dude.



