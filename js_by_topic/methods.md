## **Methods**
---

 - actions that can be performed in JavaScript.
  
- when data stored on an object is a function- a method is what an object does

 - Properties that hold function values are called **methods** of the value they belong to.
 - Methods are called by appending a JavaScript instance (an object) with a period (dot operator) followed by the name of the method and opening and closing parentheses.
 
   - *Example:*  `'example string'.methodName();`
 - A familiar example:  `console.log()` -calling the `.log() `method on the `console` object.

--- 
 ## Built-in String Methods

 **Calling a built-in string method:**
 - append a string instance with:
   - the dot operator
   - the method name
   - opening and closing parentheses

*Examples:*  
- `.toUpperCase()`  
- `.startsWith()`
- `.trim()`

[Complete list of built in string methods at MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

---
## Built-in Math Methods

**Calling a built-in Math method:**
 - append the Math method with:
   - the dot operator
   - the method name
   - opening and closing parentheses

*Example:*  
`Math.random();` : generates a decimal between 0 and 1
  

- to generate a random number in a range, multipy by the highest number in the range  

*Example:*  
`Math.random() * 100;`: generates a number between 1 and 100:

*Example:*   
`Math.floor();` : rounds a decimal number down to the nearest whole number

```
Math.floor(76.129);   // returns 76
```
Combine methods: Round down Math.random to nearest whole number  
*Example:*
Generate a random whole number between one and one hundred:
```
Math.floor(Math.random() * 100);
```
[MDN: Built-in Math Object methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

[MDN: Built-in Number Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
.  
.


## Creating Methods
 -  may be defined using anonymous arrow function expressions
    
     **Anonymous Arrow Function**
    - `sputter: () => {
    console.log('The engine sputters...');`
 - may be defined with shorthand method syntax
   
   **Shorthand Method Syntax**
     
   ```
      start(adverb) {
        console.log(`The engine starts up ${adverb}...`);
      }, 
       },
      ```
 #### Getters
 - Methods that get and return internal properties of an object
 - use the `get` keyword followed by the function
 - don't need to be called with parentheses, syntax appears the same as accessing a property
 - getter method cannot have the same name as a property

 #### Setters
 - Reassign values of existing properties within an object
 - don't need to be called with parentheses, syntax appears the same as resassigning the value of a property
 - All setters need at least one parameter to provide a parameter

#### Factory Functions
- function that returns an object and can be reused to make multiple object instances
- can have parameters allowing us to customize the object that gets returned

#### Built-in Methods for Arrays
- **Mutator** methods: modify the original array
- **Accessor** methods: methods that return a new value or representation
- **Iteration** methods: methods that operate on every item in an array, one at a time.  

![curly line](../img/curly-narrow.svg)![curly line](../img/curly-narrow.svg)![curly line](../img/curly-narrow.svg)![curly line](../img/curly-narrow.svg)![curly line](../img/curly-narrow.svg)![curly line](../img/curly-narrow.svg)![curly line](../img/curly-narrow.svg)
#### Iteration Methods
- also called **iterators**
-  methods called on arrays to manipulate elements and return values  
- [MDN’s Array iteration methods page.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Iteration_methods)  
*Examples:*
   - `.forEach()`
     - calls a function for each element in an array (same output as using the `for` loop)
     - does not change the array and returns `undefined`
   - `.map()`
     - creates a new array with the results of a function call on each element in the array, 
      - the `map()` method must be assigned to a new variable
   - `.filter()`
     - creates a new array with the elements that pass the result of a given test, 
     - the `filter()` method must be assigned to a new variable 
     - does not mutate the original array  
     *Example:*
     ```
     // the original array
     const firstNames = ['Teisha', 'Taylor', 'Pearl', 'Reese', 'Lynne', 'Tegan'];
     // the filter function
     const namesLetterT = firstNames.filter( name => {
       return name[0] === 'T';
     })
     // the newly created array
     console.log(namesLetterT); // logs [ 'Teisha', 'Taylor', 'Tegan' ]
     ```
   - `.findIndex()`
     - returns the first index in an array that passes a given test
     - useful when working with arrays containing many items
     returns `-1` if none of the elements in the array satisfies the condition
   - `.reduce()` -
     - will reduce an array to a single value
     - seen commonly with numbers, such as finding the sum of all the numbers in an array
     - does not mutate the original array
     - the `accumulator` is the first value in the array of numbers, the `currentValue` is the second number in the array
     - can also take an optional second parameter to set an initial value for `accumulator` (remember, the first argument is the callback function!)  

     *Example:*
     ```
      const newNumbers = [1, 3, 5, 7];

      const newSum = newNumbers.reduce((accumulator, currentValue) => {
        console.log('The value of the accumulator: ', accumulator);
        console.log('The value of the currentValue: ', currentValue);
        return accumulator + currentValue;
        }, 10)
        /* logs:
        The value of the accumulator:  10
        The value of the currentValue:  1
        The value of the accumulator:  11
        The value of the currentValue:  3
        The value of the accumulator:  14
        The value of the currentValue:  5
        The value of the accumulator:  19
        The value of the currentValue:  7
        */
        console.log(newSum); // logs 26
        ```



   - `.every()`
   - `.some()`
   - `.find()` 
     - returns the first value in an array that passes a given test
     - can help with arrays that contain many values
   - `.includes()`
     - iterates through array and evaluates `true` if array element passes test
   - `.split()`
     - splits a string at a designated parameter, often a space
---
#### Returning a letter in a string
- `return string[i]` where `i` is the index position of the letter you want to return
- `.charAt(i)` where `i` is the index position of the letter you want to return
---