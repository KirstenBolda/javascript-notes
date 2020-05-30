## **Arrays**
---

#### Array Literal
Array created using `let`, `const`, or `var`, followed by the array name, the assignment operator, and the array items, separated by commas, in square brackets.
 - preferred method instead of array constructor
 - stores data  in order
 - elements in an array can be the same or different data types
 - each element is a key/value pair
 - the key is the index number (zero-indexed)
 - the value is the item (called an element) in the comma separated list
 - is actually a special type of object-with the keys for each value being an index number

*Example:* 

 ```
 let colors = ['black', 'orange', 'green'];
 ```

### **Arrays: Built-In Properties and Methods**

- `.concat()`  Method used to glue arrays together to create a new array, similar to `+` for strings
- `filter()` method executes a callback function on each element in an array which returns either `true` or `false` for each of the elements, then returns a new array with elements for which the callback function returns `true`

- `.indexOf()` Method returns the index of the first element matching the value of the argument, if no matching element is found returns -1 , original array remains unchanged

- `.join()`  Method creates and returns a new string by concatenating all of the elements in an array
  - *Example:*
     ```
     items.join('');
     // where the space between '' will be inserted between array items
     ```

- `.lastIndexOf()` Method returns the index of last index matching the value of the argument

- `.length` Property that returns the number of items in the array, use dot notation to chain the `.length` property to the array name

- `.pop()`Method that removes the last item of an array, use dot notation and connect to array name, removes last element of the array and returns it, takes no arguments, mutates the original array by removing one element
  - *Example:* 

       ```
       plants.pop();
       ```

- `.push()` Method that adds items to the end of an array, use dot notation to connect to array name, then call it as a function (because it is a built in function) with items to add as arguments, mutates the array by adding elements to it
  - *Example:* 
    ```
    const animals = ['cows', 'horses']
     animals.push('chickens', 'cats', 'dogs');
     console.log(animals);
     // returns [ 'cows', 'horses', 'chickens', 'cats', 'dogs' ]
    ```
- **replace** an item in an array with a different item:

   - *Example:*
     ```
     array[x] = 'newItem';
     // where 'x' is the index of the item to be replaced
     ```

- `.shift()` Method removes the first item from the array and returns the removed element, mutates the array by removing one element
  - *Example:* 

       ```
       array.shift();
       ```
- `.slice()` Method returns a copy of the array defined by beginning and ending indices, (ending is optional, if no ending is given the rest of the array to end is returned), original array remains unchanged, remember that the ending index is not included in the returned array
  - *Example:* 
  ```
    const animals = [ 'cows', 'horses', 'chickens', 'cats', 'dogs' ]
    console.log(animals.slice(1, 4));
    // returns [ 'horses', 'chickens', 'cats' ]
   ```

- `.splice()` Remove selected group of strings and replace with another string
    - *Example:* 
      ```
      array.splice(x, y, 'newItem');
      // where 'x' is the starting index, 'y' is the number of items
      ```
- `.unshift()` Method adds the item in its argument to the beginning of the array, mutates the array by adding one element

  - *Example:*  
      
      ```
      array.unshift('newItem');
      ```


### **Access Individual Characters in a String**

How to access individual characters in a string using bracket notation:
```
const hello = 'Hello World';
console.log(hello[6]);
// Output: W
```