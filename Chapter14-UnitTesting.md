### Chapter 14.1 Why test your code

- **unit tests** test the smallest units of code. these are typically functions
- unit tests can function as a set of statements about how the program should behave
  - this is called **self documenting code**
- it's important that tests never get out of sync with the updated code.



### 14.2 hello jasmine!

- we're using jasmine

- is npm module

- jasmine project structure:

  - ![image-20211214091635714](C:\Users\Blake\AppData\Roaming\Typora\typora-user-images\image-20211214091635714.png)
  - index.js contains reverse function
  - spec/reverse.spec.js - contains tests
  - reverse.js contains code

- index.js will contain jasmine code to find and execute our tests. project specific code will now live in other files

- index.js file for jasmine tests:

  - ```javascript
    const Jasmine = require('jasmine');
    const jasmine = new Jasmine();
    
    jasmine.loadConfig({
       spec_dir: 'spec',
       spec_files: [
          "**/*[sS]pec.js"
       ],
    });
    
    jasmine.execute();
    ```

- hello.js file

  - ```javascript
    function hello(name) {
       if (name === undefined)
          name = "World";
    
       return "Hello, " + name + "!";
    }
    
    module.exports = hello;
    ```

- `it` function creates a spec/specification which is a description of expected behavior.

- first argument to `it` describe behaviors, and should start with "should" 

- spec/hello.spec.js

  - ```javascript
    const hello = require('../hello.js');
    
    describe("hello", function(){
      it("should return custom message when name is specified", function(){
        expect(hello("Jasmine")).toEqual("Hello, Jasmine!");
      });
    });
    ```

- second argument takes an expectation

  - .toEqual is a *matcher*
  - list of matchers: https://jasmine.github.io/api/3.6/matchers.html

### 14.3 unit testing in action

- three types of tests:

  1. **positive test** - verifies expected behavior with valid data.
  2. **negative test** - verifies expected behavior with *invalid* data.
  3. **edge case** - is a subset of positive tests, which checks the extreme edges of valid values.

- testing palindrome with multiple cases:

  - ```javascript
    const isPalindrome = require('../palindrome.js');
    
    describe("isPalindrome", function(){
    
       it("should return true for a single letter", function(){
          expect(isPalindrome("a")).toBeTrue();
       });
    
       it("should return true for a single letter repeated", function(){
          expect(isPalindrome("aaa")).toBeTrue();
       });
    
       it("should return true for a simple palindrome", function(){
          expect(isPalindrome("aba")).toBeTrue();
       });
    
       it("should return true for a longer palindrome", function(){
          expect(isPalindrome("racecar")).toBeTrue();
       });
    
    });
    ```

- common workflow:

  - Write code
  - Write tests
  - Fix any bugs found while testing

- The BETTER workflow:

  - Write tests
  - Write code



### 14.4 Test-Driven Development

- this requires to think about our code **before** writing it

- example with a parse numbers project

  - ```javascript
    const parse = require('../parse-numbers');
    
    describe("parse numbers", function(){
    
       it("returns array when passed comma separated list of numbers", function(){
          let items = parse("5,8,0,17,6,4,9,3", ",");
          expect(Array.isArray(items)).toBeTrue();
       });
        
    });
    ```

- now write code to pass the new test

  - ```javascript
    function parseData(text, delimiter) {
       return text.split(delimiter);
    }
    
    module.exports = parseData;
    ```

- Red, green refactor cycle

  - Red -> Write a failing test.
  - Green -> Make it pass by implementing the code.
  - Refactor -> Make the code better.

### 14.5 TDD in action

- using not.toEqual()

  - checks that a value is NOT equal to some value

  - ```javascript
       it("returns id in object", function() {
         let result = processor("9701::<489584872710>");
         expect(result.id).not.toEqual(undefined);
       });
    ```

  - the above makes sure that the id is NOT equal to undefined

- 

