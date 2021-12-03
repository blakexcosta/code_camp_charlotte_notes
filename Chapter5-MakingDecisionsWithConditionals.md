

### 5.1 Booleans

- creating boolean:

  - ex:)

    ```javascript
    console.log(true);
    console.log(typeof true);
    console.log(typeof false);
    ```

- converting number and strings to booleans

  - ex:) 

    ```javascript
    console.log(Boolean("true")); 		//true
    console.log(Boolean("TRUE")); 		//true
    console.log(Boolean(0));      		//false 
    console.log(Boolean(1));      		//true
    console.log(Boolean(''));     		//false
    console.log(Boolean('LaunchCode'));  //true	
    ```

- Boolean expressions evaluate to true or false and are done with **equality operator** i.e. ==

- List of comparison Operators:

  - 

  - |           Operator           |                         Description                          |        Examples Returning `true`         | Examples Returning `false` |
    | :--------------------------: | :----------------------------------------------------------: | :--------------------------------------: | :------------------------: |
    |         Equal (`==`)         | Returns `true` if the two operands are equal, and `false` otherwise. |         `7 == 7``"dog" == "dog"`         |  `7 == 5``"dog" == "cat"`  |
    |       Not equal(`!=`)        | Returns `true` if the two operands are not equal, and `false` otherwise. |         `7 != 5``"dog" != "cat"`         |  `7 != 7``"dog" != "dog"`  |
    |      Greater than (`>`)      | Returns `true` if the left-hand operand is greater than the right-hand operand, and `false` otherwise. |            `7 > 5``'b' > 'a'`            |     `5 > 7``'a' > 'b'`     |
    |       Less than (`<`)        | Returns `true` if the left-hand operand is less than the right-hand operand, and `false` otherwise. |            `5 < 7``'a' < 'b'`            |     `7 < 5``'b' < 'a'`     |
    | Greater than or equal (`>=`) | Returns `true` if the left-hand operand is greater than or equal to the right-hand operand, and `false` otherwise. | `7 >= 5``7 >= 7``'b' >= 'a'``'b' >= 'b'` |    `5 >= 7``'a' >= 'b'`    |
    |  Less than or equal (`<=`)   | Returns `true` if the left-hand operand is less than or equal to the right-hand operand, and `false` otherwise. | `5 <= 7``5 <= 5``'a' <= 'b'``'a' <= 'a'` |    `7 <= 5``'b' <= 'a`     |

- Do note that == has some funkiness in javascript

  - `7 == "7"`
  - `0 == false`
  - `0 == ''`
  - we will use === in the future 



### 5.2 Loose Equality

- == doesn't work as well when we're trying to compare things as different data types. ex:)

  - ```javascript
    console.log(7 == "7");
    console.log(0 == false);
    console.log(0 == '');
    ```

  - all above would return `true`

- this is why it's referred to as loose equality

- === is referred to as **strict equality**

  - it compares two operands *without* converting their data types

- example of using === that all return false

  - ex:) 

    ```javascript
    console.log(7 === "7");
    console.log(0 === false);
    console.log(0 === '');
    ```

  - use === or !== whenever possible



### 5.3 Logical Operators

- using AND operator

  - ex:) `console.log(7 > 5 && 5 > 3); // prints 'true'` 

- using OR operator

  - ex:) `console.log(2 > 3 || 'dog' === 'cat');  // prints 'false'`

- using NOT/bang operator. which just takes an operand and reverses its boolean value

  - ex:) `console.log(! true); // prints 'false'`

  - | Precedence |          Category           |        Operators         |
    | :--------: | :-------------------------: | :----------------------: |
    | (highest)  |         Logical NOT         |           `!`            |
    |            |       Exponentiation        |           `**`           |
    |            | Multiplication and division |      `*`, `/`, `%`       |
    |            |  Addition and subtraction   |         `+`, `-`         |
    |            |         Comparison          |   `<=`, `>=`, `>`, `<`   |
    |            |          Equality           | `===`, `!==`, `==`, `!=` |
    |            |         Logical AND         |           `&&`           |
    |  (lowest)  |         Logical OR          |           `||`           |



### 5.4 Conditionals

- using if statements in javascript

  - ex:) 

    ```javascript
    let billHasBeenPaid = false;
    
    if (!billHasBeenPaid) {
       console.log("Your bill is due soon!");
    }
    ```

- using an else clause in javascript

  - ex:) 

    ```javascript
    let billHasBeenPaid = true;
    
    if (!billHasBeenPaid) {
       console.log("Your bill is due soon!");
    } else {
       console.log("Your payments are up to date."); // this line will print
    }
    ```

- the example above provides a mechanism called **branching**. i.e. the program can take more than one path depending on when a condition is true or false

- using else-if statements in javascript

  - ex:)

    ```javascript
    let x = 10;
    let y = 20;
    
    if (x > y) {
       console.log("x is greater than y");
    } else if (x < y) {
       console.log("x is less than y"); // will print this line
    } else {
       console.log("x and y are equal");
    }
    ```

- we dont need to have an else statement with else if's

  - ex:)

    - ```javascript
      let x = 10;
      let y = 20;
      
      if (x > y) {
         console.log("x is greater than y");
      } else if (x < y) {
         console.log("x is less than y"); // this line will print
      } else if (x % 5 === 0) {
         console.log("x is divisible by 5");
      } else if (x % 2 === 0) {
         console.log("x is even");
      }
      ```





### 5.5 Nested Conditionals

- nesting conditionals:

- ex:)

  - ```javascript
    let num = 7;
    
    if (num % 2 === 0) {
        console.log("EVEN");
    
        if (num > 0) {
            console.log("POSITIVE");
        }
    }
    ```

- keep in mind about code conventions



### 5.6 Exercise

- Part A solution is:

  - ```javascript
    // Declare and initialize the variables for exercise 1 here:
    let engineIndicatorLight = "red blinking";
    let spaceSuitsOn = true;
    let shuttleCabinReady = true;
    let crewStatus = spaceSuitsOn && shuttleCabinReady;
    let computerStatusCode = 200;
    let shuttleSpeed = 15000;
    
    ```

- part B is will print "engines are off"

- rest of solutions are in replit

### 5.7 Studio

- Smart goals:
  - Specific 
  - Measurable
  - Attainable
  - Relevant
  - Time Bound