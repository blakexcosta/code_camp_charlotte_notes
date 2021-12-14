### 12.1 Objets and why they matter

- initialization of a object is called an object literal

- objects require three things

  1. a name
  2. a set of keys
  3. their corresponding vbalues

- example format

  - ```javascript
    let objectName = {
        key1: value1,
        key2: value2,
        key3: value3,
        .
        .
        .
    };
    ```

- very important to pay attention to spacing and tabs when putting objects on newlines

- keys can *only* be valid js strings

- example object

  - ```javascript
    let tortoiseOne = {
        species: "Galapagos Tortoise",
        name: "Pete",
        weight: 919,
        age: 85,
        diet: ["pumpkins", "lettuce", "cabbage"],
        sign: function() {
            return this.name + " is a " + this.species;
        }
     };
    ```



### 12.2 Working with objects

- two ways to access a property

  - bracket notation
  - dot notation

- bracket notation: `object["key"]`

- dot notation: `object.key`

- use bracket syntax whenever possible

- objects are **mutable**

- changing values of properties:

  - ```javascript
    let tortoiseOne = {
        species: "Galapagos Tortoise",
        name: "Pete",
        weight: 919,
        age: 85,
        diet: ["pumpkins", "lettuce", "cabbage"]
    };
    
    console.log(tortoiseOne.weight);
    
    newWeight = tortoiseOne.weight + 10;
    
    tortoiseOne["weight"] = newWeight;
    
    console.log(tortoiseOne["weight"]);
    ```

- add new key/value pairs

  - ```javascript
    objectName["new-key"] = propertyValue;
    ```



### 12.3 Coding with objects

- objects are stored by *reference* meaning it's location is based in memory

  - meaning we can't compare objects themselves for equality when they have the same values because memory locations differ

  - i.e. (you already knew this blake)

    - ```javascript
      let tortoiseOne = {
         species: "Galapagos Tortoise",
         diet: ["pumpkins", "lettuce", "cabbage"]
      };
      
      let tortoiseTwo = {
         species: "Galapagos Tortoise",
         diet: ["pumpkins", "lettuce", "cabbage"]
      };
      
      console.log(tortoiseOne === tortoiseTwo);
      ```

- iterating through object properties with fancy for loop

  - ```javascript
    let giraffe = {
      species: "Reticulated Giraffe",
      name: "Cynthia",
      weight: 1500,
      age: 15,
      diet: "leaves"
    };
    
    for (item in giraffe) {
       console.log(item + ", " + giraffe[item]);
    }
    ```

- any changes done in a function to an object will still change the object itself (duh)





### 12.4 the Math object

- **Math** object is immutable
- Math properties are constants





### 12.5 Math methods

- common methods:

  - |                            Method                            |        Syntax         |                         Description                          |
    | :----------------------------------------------------------: | :-------------------: | :----------------------------------------------------------: |
    | [abs](https://education.launchcode.org/intro-to-professional-web-dev/appendices/math-method-examples/abs-examples.html#abs-examples) |  `Math.abs(number)`   |           Returns the positive value of `number`.            |
    | [ceil](https://education.launchcode.org/intro-to-professional-web-dev/appendices/math-method-examples/ceilfloortrunc-examples.html#ceilfloortrunc-examples) |  `Math.ceil(number)`  | Rounds the decimal `number` UP to the closest integer value. |
    | [floor](https://education.launchcode.org/intro-to-professional-web-dev/appendices/math-method-examples/ceilfloortrunc-examples.html#floor) | `Math.floor(number)`  | Rounds the decimal `number` DOWN to the closest integer value. |
    | [max](https://education.launchcode.org/intro-to-professional-web-dev/appendices/math-method-examples/max-and-min-examples.html#max-and-min-examples) | `Math.max(x,y,z,...)` |       Returns the largest value from a set of numbers.       |
    | [min](https://education.launchcode.org/intro-to-professional-web-dev/appendices/math-method-examples/max-and-min-examples.html#min) | `Math.min(x,y,z,...)` |      Returns the smallest value from a set of numbers.       |
    | [pow](https://education.launchcode.org/intro-to-professional-web-dev/appendices/math-method-examples/pow-examples.html#pow-examples) |    `Math.pow(x,y)`    |    Returns the value of x raised to the power of y (x y).    |
    | [random](https://education.launchcode.org/intro-to-professional-web-dev/appendices/math-method-examples/random-examples.html#random-examples) |    `Math.random()`    | Returns a random decimal value between 0 and 1, NOT including 1. |
    | [round](https://education.launchcode.org/intro-to-professional-web-dev/appendices/math-method-examples/round-examples.html#round-examples) | `Math.round(number)`  |    Returns `number` rounded to the nearest integer value.    |
    | [sqrt](https://education.launchcode.org/intro-to-professional-web-dev/appendices/math-method-examples/pow-examples.html#square-root) |  `Math.sqrt(number)`  |             Returns the square root of `number`.             |
    | [trunc](https://education.launchcode.org/intro-to-professional-web-dev/appendices/math-method-examples/ceilfloortrunc-examples.html#trunc) | `Math.trunc(number)`  | Removes any decimals and returns the integer part of `number`. |



### 12.6 Combining Math methods

- Random selection from array

  - ```javascript
    function randomSelection(arr){
       let index = Math.floor(Math.random()*arr.length);
       return arr[index];
    }
    
    let happiness = ['Hope','Joy','Peace','Love','Kindness','Puppies','Kittens','Tortoise'];
    
    for (i=0; i < 8; i++){
       console.log(randomSelection(happiness));
    }
    ```

- rounding to decimal places

  - ```javascript
    Math.round(5.56789123*100)/100
    ```

  - | Decimal Places In Answer | Multiply & Divide By |             Syntax             |
    | :----------------------: | :------------------: | :----------------------------: |
    |            1             |          10          |   `Math.round(number*10)/10`   |
    |            2             |         100          |  `Math.round(number*100)/100`  |
    |            3             |         1000         | `Math.round(number*1000)/1000` |
    |           etc.           |         etc.         |              etc.              |



