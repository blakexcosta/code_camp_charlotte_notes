

### 7.1 Strings as Collections

- **collections** - data types comprised of smaller pieces
- strings are made up of **characters**
  - javascript has no **char** data type
- strings are known as an **ordered collection**



### 7.2 Bracket Notation

- access individual character:

  ```javascript
  let jsCreator = "Brendan Eich";
  let firstInitial = jsCreator[0]; // access B
  let lastInitial = jsCreator[8]; // access E
  
  let outputStr = "JavaScript was created by somebody with initials " +
     firstInitial + "." +
     lastInitial + ".";
  
  console.log(outputStr);
  ```

- bracket notation is 0 based,

- you can't use -1 to access the last element

  - ex:) `jsCreator[-1]` will error out

- you will get `undefined` if you try to access element that doesn't exist

- get length of strings:

  - ex;) 

    ```javascript
    let phrase = "JavaScript rocks!";
    console.log(phrase[phrase.length - 8]);
    ```



### 7.3 Strings as Objects

- strings are objects in javascript.

- an operation carried out on an object is known as a **method**

- data associated with an object is known as a **property**

- length of a string:

  - ex:) 

    ```javascript
    let firstName = "Grace"; 
    console.log(firstName, "has", firstName.length, "characters");
    ```

- string to lowercase"

  - ex:) 

    ```javascript
    let nonprofit = "LaunchCode";
    console.log(nonprofit.toLowerCase());
    ```

  - toLowerCase() does not alter the original string itself



### 7.4 String immutability

- **immutable** = somethin that cannot be changed
- strings are immutable in js
  - we cannot change strings in js



### 7.5 String Methods

- Most common string methods:

  - |                            Method                            |                      Syntax                       |                         Description                          |
    | :----------------------------------------------------------: | :-----------------------------------------------: | :----------------------------------------------------------: |
    | [indexOf](https://education.launchcode.org/intro-to-professional-web-dev/appendices/string-method-examples/indexOf-examples.html#string-indexof-examples) |           `stringName.indexOf(substr)`            | Returns the index of the first occurrence of the substring in the string, and returns -1 if the substring is not found. |
    | [toLowerCase](https://education.launchcode.org/intro-to-professional-web-dev/appendices/string-method-examples/toLowerCase-examples.html#string-tolowercase-examples) |            `stringName.toLowerCase()`             | Returns a copy of the given string, with all uppercase letters converted to lowercase. |
    | [toUpperCase](https://education.launchcode.org/intro-to-professional-web-dev/appendices/string-method-examples/toUpperCase-examples.html#string-touppercase-examples) |            `stringName.toUpperCase()`             | Returns a copy of the given string, with all lowercase letters converted to uppercase. |
    | [trim](https://education.launchcode.org/intro-to-professional-web-dev/appendices/string-method-examples/trim-examples.html#string-trim-examples) |                `stringName.trim()`                | Returns a copy of the given string with the leading and trailing whitespace removed. |
    | [replace](https://education.launchcode.org/intro-to-professional-web-dev/appendices/string-method-examples/replace-examples.html#string-replace-examples) | `stringName.replace(searchChar, replacementChar)` | Returns a copy of `stringName`, with the first occurrence of `searchChar` replaced by `replacementChar`. |
    | [slice](https://education.launchcode.org/intro-to-professional-web-dev/appendices/string-method-examples/slice-examples.html#string-slice-examples) |             `stringName.slice(i, j)`              | Returns the substring consisting of characters from index `i` through index `j-1`. |



### 7.6 Encoding Characters

- **byte** = set of 8 bits

  - ex:) 00101101
  - this represents a binary number. i.e a **base-2** number

- we use base-10 numbers in normal life (0-9)

- each bit can have 2 value and 8  places. so there are 2^8 possibilites. or 256 different values

  - these can represent decimal integers from 0-255

- **character encodings** represent our characters that we use every day

- we use **ASCII**

- In summary, strings are stored in a computer using the following process:

  1. Break a string into its individual characters.
  2. Use a character encoding, such as ASCII, to convert each of the characters to an integer.
  3. Convert each integer to a series of bits using decimal-to-binary integer conversion.

- find character code of javascript string

  - ex:) 

    ```javascript
    let nonprofit = "LaunchCode";
    
    console.log(nonprofit.charCodeAt(0));
    console.log(nonprofit.charCodeAt(1));
    console.log(nonprofit.charCodeAt(2));
    console.log(nonprofit.charCodeAt(3));
    console.log(nonprofit.charCodeAt(4));
    console.log(nonprofit.charCodeAt(5));
    console.log(nonprofit.charCodeAt(6));
    console.log(nonprofit.charCodeAt(7));
    console.log(nonprofit.charCodeAt(8));
    console.log(nonprofit.charCodeAt(9));
    ```

- convert ascii code to charac ter

  - ex:) 

    ```javascript
    let codes = [76, 97, 117, 110, 99, 104, 67, 111, 100, 101];
    
    let characters = String.fromCharCode(codes[0]) + String.fromCharCode(codes[1])
                   + String.fromCharCode(codes[2]) + String.fromCharCode(codes[3])
                   + String.fromCharCode(codes[4]) + String.fromCharCode(codes[5])
                   + String.fromCharCode(codes[6]) + String.fromCharCode(codes[7])
                   + String.fromCharCode(codes[8]) + String.fromCharCode(codes[9]);
    
    console.log(characters);
    ```



### 7.7 Special Characters

- allows us to include characters in strings

  - ex:) 

    ```javascript
    console.log("A message\nbroken across lines,\n\tand indented");
    ```

- using unicode character in string

  - ex:) 

    ```javascript
    console.log("The interrobang character, \u203d, combines ? and !");
    ```

- including quotes within a string:

  - ex:)

    ```javascript
    console.log("\"The dog's favorite toy is a stuffed hedgehog,\" said Chris");
    ```



### 7.8 Template Literals

- i.e string interpolation

  - ex:)

    ```javascript
    let name = "Jack";
    let currentAge = 9;
    
    console.log(`Next year, ${name} will be ${currentAge + 1}.`);
    ```

- allows us to easily create multiline strings without concatenation as spaces and tabs preserved as presented

- They may not always be supported in older browsers that dont support at least ES2015



