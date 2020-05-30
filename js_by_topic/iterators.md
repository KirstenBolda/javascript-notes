## **Iterators**
---
### **Higher Order Functions**
- functions that accept other functions as arguments and/or return functions as output
- used to build abstractions on other abstractions
- helps with writing modular code which is easier to read and debug

### **Functions as Data**
- functions can be reassigned to a new variable that holds a reference to the original function
- reassign the function without using parentheses (assign the value of the function itself, not the value it returns when invoked)
- the new function name can be invoked with parentheses just as the original function

### **Properties of Functions**
(similar to other objects' properties)
- `.length`
- `.name`
  - use the dot operator `.` to access a function’s name property
- `.toString()`


### **Functions as Parameters**
- Callback Functions: functions that are passed in as parameters and invoked in the execution of the higher-order function
- pass in the function without the parentheses (including parentheses would call the result of the function, not the function)

### **Iterators (Iteration Methods)**
#### Iteration Methods
- also called **iterators**
-  methods called on arrays to manipulate elements and return values  
*Examples:*
   - `.forEach()`
     - calls a function for each element in an array (same output as using the `for` loop)
   - `.map()`
     - creates a new array with the results of a function call on each element in the array, 
      - the `map()` method must be assigned to a new variable
   - `.filter()`
     - creates a new array with the elements that pass the result of a given test, 
     - the `filter()` method must be assigned to a new variable 
     - does not mutate the original array
   - `.findIndex()`
     - returns the first index in an array that passes a given test
     - useful when working with arrays containing many items
   - `.reduce()` -
     - will reduce an array to a single value
     - seen commonly with numbers, such as finding the sum of all the numbers in an array
     - does not mutate the original array
   - `.every()`
   - `.some()`
   - `.find()` 
     - returns the first value in an array that passes a given test
     - can help with arrays that contain many values
   - `.includes()`
     - iterates through array and evaluates `true` if array element passes test


