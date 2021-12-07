### Chapter 9.1 Iteration

- repeated execution of a sequence of statements = **iteration**

- basic for loop

  - ex:) 

    ```javascript
    for (let i = 0; i < 51; i++) {
       console.log(i);
    }
    ```



### 9.2 for loops

- for loop typically used for **definite iteration**
  - IE repeating a specific task with a specific dataset



### 9.3 iterating over collections

- iterating over a string:

  - ex:)

    ```javascript
    let name = "LaunchCode";
    
    for (let i = 0; i < name.length; i++) {
       console.log(name[i]);
    }
    ```

- iterating over an array

  - ex:)

    ```javascript
    let languages = ["JS", "Java", "C#", "Python"];
    
    for(let i = 0; i < languages.length; i++){
    	console.log(languages[i]);
    }
    ```



### 9.4 breaking down the for statement

- four pieces:
  - **loop variables**
  - **loop conditional**
  - **update expression**
  - **loop body**



### 9.5 the accumulator pattern

- basically adding numbers together:

  - ex:) 

    ```javascript
    let n = 6;
    let total = 0;
    
    for (let i = 1; i <= n; i++) {
       total += i;
    }
    
    console.log(total); // will output 21
    ```

- reversing a string:

  - ex:) 

    ```javascript
    let str = "blue";
    let reversed = "";
    
    for (let i = 0; i < str.length; i++) {
       reversed = str[i] + reversed;
    }
    
    console.log(reversed);
    ```

    

- summing an array:

  - ex:) 

    ```javascript
    let numbers = [2, -5, 13, 42];
    let total = 0;
    
    for (let i = 0; i < numbers.length; i++) {
       total += numbers[i];
    }
    ```



### 9.6 while loops

- basic while loop:

  - ex:)

    ```javascript
    let i = 0;
    
    while (i < 51) {
       console.log(i);
       i++;
    }
    ```

- be careful for infinite loops with while loops

- input validation example:

  - ex:) 

    ```javascript
    let num = input.question('Please enter a positive number:');
    num = Number(num);
    
    while (num <= 0) {
       num = input.question('Invalid input. Please enter a positive number:');
       num = Number(num);
    }
    ```

- gamification of cirriculum + dev

- quantum computing, data science, analytics, research, etc.



### 9.7 Terminating a loop with break

- using break with for loop:

  - ex:)

    ```javascript
    for (let i = 0; i < 42; i++) {
       // rest of loop body
        
       if (i > 10) {
          break;
       }
    }
    ```

- using break with while loop

  - ex:) 

    ```javascript
    let numbers = [ /* some numbers */ ];
    let searchVal = 42;
    let i = 0;
    
    while (i < numbers.length) {
       if (numbers[i] === searchVal) {
          break;
       }
       i++;
    }
    ```





### 9.8 Choosing which loop to use

- for loops typically used to iterate through a fixed set of values. called **definite iteration**
- while loops used more generally. i.e. when we don't know how many times something will iteratie. i.e **indefinite iteration**



