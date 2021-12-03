### 8.1 Arrays are like strings

- arrays a re sequence of values that can be accessed via an ordered index. 

- js arrays can store data of any type

- js arrays zero based

- Declaring an array

  - ex:)

    ```javascript
    let emptyArray = [];
    
    let programmingLanguages = ["JavaScript", "Python", "Java", "C#"];
    ```

- js arrays can dynamically add stuff

- getting array length:

  - ```javascript
    let programmingLanguages = ["JavaScript", "Python", "Java", "C#"];
    console.log(programmingLanguages.length); // will print 4
    ```

- js arrays can hold mixture of data types

  - ex:) 

    ```javascript
    let grabBag = ["A string value", true, 99, 105.5];
    ```



### 8.2 Working with arrays

- arrays accessed via an index. they are zero based

- end element can be accessed with `array.length-1`

- accessing elements:

  - ex:)

    ```javascript
    let programmingLanguages = [
       "JavaScript", // index 0
       "Python",     // index 1
       "Java",       // index 2
       "C#"          // index 3
    ];
    console.log(programmingLanguages[0]);
    console.log(programmingLanguages[3]);
    ```

- will get `undefined` if try to access element that doesn't exist

- arrays **are mutable**

- reassigning new value 

  - ex:)

    ```javascript
    let javaScriptFrameworks = ["React", "Angular", "Ember"];
    
    // Set the value of index 2 to be "Vue"
    javaScriptFrameworks[2] = "Vue"; // will now be "React", "Angular", "Vue"
    ```



### Array methods

- common array methods:

  - Methods that return info about array:

  - |                            Method                            |           Syntax           |                         Description                          |
    | :----------------------------------------------------------: | :------------------------: | :----------------------------------------------------------: |
    | [includes](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/includes-examples.html#includes-examples) | `arrayName.includes(item)` |       Checks if an array contains the specified item.        |
    | [indexOf](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/indexOf-examples.html#indexof-examples) | `arrayName.indexOf(item)`  | Returns the index of the FIRST occurrence of an item in the array. If the item is not in the array, -1 is returned. |

  - Methods that rearrange an array:

  - |                            Method                            |        Syntax         |                         Description                          |
    | :----------------------------------------------------------: | :-------------------: | :----------------------------------------------------------: |
    | [reverse](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/reverse-example.html#reverse-example) | `arrayName.reverse()` |       Reverses the order of the elements in an array.        |
    | [sort](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/sort-examples.html#sort-examples) |  `arrayName.sort()`   | Arranges the elements of an array into increasing order (kinda). |

  - Methods that add/remove entries from array:

  - |                            Method                            |                        Syntax                        |                         Description                          |
    | :----------------------------------------------------------: | :--------------------------------------------------: | :----------------------------------------------------------: |
    | [pop](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/push-and-pop-examples.html#pop) |                  `arrayName.pop()`                   |      Removes and returns the LAST element in an array.       |
    | [push](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/push-and-pop-examples.html#push-and-pop-examples) |         `arrayName.push(item1, item2, ...)`          | Adds one or more items to the END of an array and returns the new length. |
    | [shift](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/shift-and-unshift-examples.html#shift-and-unshift-examples) |                 `arrayName.shift()`                  |      Removes and returns the FIRST element in an array.      |
    | [splice](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/splice-examples.html#splice-examples) | `arrayName.splice(index, number, item1, item2, ...)` | Adds, removes or replaces one or more elements anywhere in the array. |
    | [unshift](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/shift-and-unshift-examples.html#unshift) |        `arrayName.unshift(item1, item2, ...)`        | Adds one or more items to the START of an array and returns the new length. |

  - Methods that create new arrays:

  - |                            Method                            |                   Syntax                    |                         Description                          |
    | :----------------------------------------------------------: | :-----------------------------------------: | :----------------------------------------------------------: |
    | [concat](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/concat-examples.html#concat-examples) | `arr.concat(otherArray1, otherArray2, ...)` | Combines two or more arrays and returns the result as a new array. |
    | [join](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/join-examples.html#join-examples) |           `arr.join('connecter')`           |     Combines all the elements of an array into a string.     |
    | [slice](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/slice-examples.html#slice-examples) |     `arr.slice(start index, end index)`     |    Copies selected entries of an array into a new array.     |
    | [split](https://education.launchcode.org/intro-to-professional-web-dev/appendices/array-method-examples/split-examples.html#split-examples) |       `stringName.split('delimiter')`       | Divides a string into smaller pieces, which are stored in a new array. |



### 8.4 Multi-dimensional arrays

- i.e. 2d arrays

- think of like a spreadsheet with rows and columns

  - i.e. `array[row][column]` like: `array[0][0]`

- example 2d array:

  - ex;)

    ```javascript
    let shuttleCrews = [
       ['Robert Gibson', 'Mark Lee', 'Mae Jemison'],
       ['Kent Rominger', 'Ellen Ochoa', 'Bernard Harris'],
       ['Eilen Collins', 'Winston Scott',  'Catherin Coleman']
    ];
    
    console.log(shuttleCrews[0][2]);
    console.log(shuttleCrews[1][1]);
    console.log(shuttleCrews[2][1]);
    ```

- applying array method to inner array

  - ex:)

    ```javascript
    let shuttleCrews = [
       ['Robert Gibson', 'Mark Lee', 'Mae Jemison'],
       ['Kent Rominger', 'Ellen Ochoa', 'Bernard Harris'],
       ['Eilen Collins', 'Winston Scott',  'Catherin Coleman']
    ];
    
    let newCrew = ['Mark Polansky', 'Robert Curbeam', 'Joan Higginbotham'];
    
    // Add a new crew array to the end of shuttleCrews
    shuttleCrews.push(newCrew);
    console.log(shuttleCrews[3][2]);
    
    // Reverse the order of the crew at index 1
    shuttleCrews[1].reverse();
    console.log(shuttleCrews[1]);
    ```









SMART Goals:
***Goals for class:***

​		To review and complete studios, assignments and exercises for next week's material by end of this week.

***goals for career:***

​	     To elevate myself to a senior AI engineer/ VP of research, and by doing this codecamp I'm improving upon my teaching abilities. Which in turn allows me to communicate + illustrate important points to both personnel and clients outside of class.

***Inspirational statements:***

# “Think not how unlucky I am that this should happen to me. But not at all. Perhaps, say how lucky I am that I am not broken by what has happened, and I am not afraid of what is about to happen. For the same blow might have stricken anyone, but not many would have absorbed it without capitulation and complaint.” - Marcus Aurelius



“Until you make the unconscious conscious, it will direct your life and you will call it fate.”
― **C.G. Jung**







































​	

​	

​	