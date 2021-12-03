

### 6.1 What is debugging?

- programming errors are called bugs
- there are three kinds of errors
  1. **syntax errors**
  2. **runtime errors**
  3. **logic errors**



### 6.2 Categories of Errors

- two stages of code execution
  1. **Parsing** - this stage verifies syntax and structure of code
  2. **Execution** - when actions of our program are actually carried out
- **syntax** - structure of langauge + rules about that structure
- **Runtime errors** - appear when running the program. Also called **exceptions**
- **Logic erors**  - runtime or syntax wont show, but the program won't work as intended
  - logic erors are tricky. You have to thoroughly examine the program



### 6.3 Diagnosing error message

- search for errors as needed. Keep in mind they are our friends



### 6.4 Error Types

- **Error type** - clarrification that javacsript uses to group error sbased on their cause.

  - error type is actually a built-in object

  - 

  - |    Error Type    |                         Description                          |           Example of code triggering the error           |                     Example description                      |
    | :--------------: | :----------------------------------------------------------: | :------------------------------------------------------: | :----------------------------------------------------------: |
    |  `SyntaxError`   |   Occurs when trying to parse syntactically invalid code.    |                 `console.log("hello"; `                  | The call to `console.log` does not have a required close parenthesis. |
    | `ReferenceError` |   Occurs when a non-existent variable is used/referenced.    | `1 2`` let firstName = "Jack"; console.log(firstname); ` | The variable `firstname` does not exist; it is a misspelling of `firstName`. |
    |   `TypeError`    |     Occurs when trying to use a value in an invalid way.     |                         `1(); `                          | The numeric value `1` is not a function, so trying to use it as one results in `TypeError: 1 is not a function`. |
    |   `RangeError`   |     Occurs when passing an invalid value to a function.      |                 `let nums = Array(-1); `                 | The constructor function `Array(n)` creates an empty array of length `n`. It is not possible to create an array with negative length, so the code results in `RangeError: Invalid array length`. |
    |    `URIError`    | Occurs when improperly using a global URI-handling function. ('URI' = Uniform Resource Identifier) |                    `decodeURI('%'); `                    | The `%` character is used to encode characters not otherwise allowed in URIs, such as spaces (`%20`). If an invalid character encoding is given, a `URIError` results. |
    |     `Error`      | The type from which all other errors are built. It can be used to generate programmer-triggered and programmer-defined errors. |                                                          |                                                              |



### 6.5 Debugging logic errors

- Printing values can help diagnose logic errors
- remember to remove `console.log` statements when you're done debugging



### 6.6 How to avoid debugging

- first off, start small. don't spaghetti code.
-  "Get something working and keep it working."



### 6.7 Asking good Questions

- nothing I haven't learned



### 6.8 Exercises: Debugging

- solutions in repl.it

