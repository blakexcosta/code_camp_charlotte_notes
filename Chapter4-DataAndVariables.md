

### 4.1 Values and data types

- value is specific piece of data such as word or number
  - EX:) 5, 5.2, "Hello, World!"
- each value has a **data type**
  - **number**
    - ex:) **4**, **3.3**
  - **string**
    - strings must be enclosed in single or double quotes
    - ex:) **"Hello World"**
- use **typeof** to find what data type a value falls into
  - ex:) `console.log(typeof "Hello, World!");`
- **Expressions** are code segments reduced to a value
  - ex:) `typeof "Hello, World"`
- Double quote'd strings can have single quotes in them. single quote strings can have double quotes in them:
  - ex:) `"Bruce's beard"`
  - ex:) `The knights who say "Ni!"'`
- Don't mix double quoted strings with doulbe quotes, or single qouted strings with single quotes. Will produce unexpected results. specifically a syntax error.
  - ex:) `"Bruce"s Beard"`
  - ex:) `'The knights who say 'Ni!''`
- Do *not* use commas for integer/number values
  - this will produce `42, 0`  and not behave as expected. treated as a pair of values
  - ex:) `console.log(42,000);`
- console.log can print any number of values as long as separated by commas
  - ex:) `console.log(3.4, "hello", 45); `
- Javascript *does not* distringuish between float and int types. 
  - ex:) both of these are **numbers** data type: `3.5` and `4`



### 4.2 Type Conversion

- convert string to number	
  - ex:) `console.log(Number("2345"));`
- convert number to string
  - ex:) `console.log(String("2345"));`
- **Nan** will be returned if a string cant be converted to a number
  - ex:) `console.log(Number("23bottles")); // will return NaN`



### 4.3 variables

- a **variable** is a name that refers to a value

- creating a variable is called **declaration**

- assigning variable value for first time is **initalization**

- declare and initializing variables

  - ex:) `let programmingLanugage = "Javascript"`;

- *don't* use `var` keyword. use `let` instead

- you can declare a variable without `let`

  - ex:) `programmingLanguage = "JavaScript";`
  - Above creates a global variable . Don't do this unless have good reason

- Evaluating a variable

  - ```javascript
    let message = "Hello, World!";
    console.log(message);
    ```

  - console.log evaluates "message"

- Reassigning variable

  - ```javascript
     let day = "Thursday";
     console.log(day);
     day = "Friday"; // day will now be "Friday"
    ```



### 4.4 More on Variables

- creating constant
  - ex:) `const appName = "Get It Done!";`
- use camelCase to name vairables
- collection of words used by the javascript language are known as **keywords**. 



### 4.5 Expressions and Evaluations

- nothing I don't already know



### Operators and Operands

- **operator** = characters that represent a computation (like addition)

  - ex:) +,-,/,%

- **operands** = values an operator works on

  - ex:) `20 - 32`
    - operands are 20 and 32

- **arithmetic operators list**

  - | Addition (`+`)        | Adds the two operands                                        | `2 + 3` returns `5`                                          |
    | --------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
    | Subtraction (`-`)     | Subtracts the two operands                                   | `2 - 3` returns `-1`                                         |
    | Multiplication (`*`)  | Multiplies the two operands                                  | `2 * 3` returns `6`                                          |
    | Division (`/`)        | Divides the first operand by the second                      | `6 / 2` returns `3`                                          |
    | Modulus (`%`)         | Aka the remainder operator. Returns the integer remainder of dividing the two operands. | `7 % 5` returns `2`                                          |
    | Exponentiation (`**`) | Calculates the base (first operand) to the exponent (second operand) power, that is, baseexponent | `3 ** 2` returns `9``5 ** -1` returns `0.2`                  |
    | Increment (`++`)      | Adds one to its operand. If used before the operand (`++x`), returns the value of its operand after adding one; if used after the operand (`x++`), returns the value of its operand before adding one. | If `x` is `2`, then `++x` sets `x` to `3` and returns `3`, whereas `x++` returns `2` and, only then, sets `x` to `3` |
    | Decrement (`--`)      | Subtracts one from its operand. The return value is analogous to that for the increment operator. | If `x` is `2`, then `--x` sets `x` to `1` and returns `1`, whereas `x--` returns `2` and, only then, sets `x` to `1` |

- arithmetic in javascript done with PE(MD)(AS)



### 4.7 Other Operators

-  using String operator to **concatenate**

  - ex:) `"Launch"+"Code" // results in "LaunchCode"`

- **Compound Assignment operators list**:

- |       Operator name       | Shorthand |   Meaning   |
  | :-----------------------: | :-------: | :---------: |
  |    Addition assignment    | `a += b`  | `a = a + b` |
  |  Subtraction assignment   | `a -= b`  | `a = a - b` |
  | Multiplication assignment | `a *= b`  | `a = a * b` |
  |    Division assignment    | `a /= b`  | `a = a / b` |



### 4.8 Input with readline-sync

- getting input from using readline sync

  - ex:)

    ```javascript
    const input = require('readline-sync');
    
    let info = input.question("Question text... ");
    ```

- make sure students have a package.json file like the following

  - ```
    https://replit.com/@launchcode/InputExamples01
    ```

- readling-sync treats all input like strings.