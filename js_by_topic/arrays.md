# **Arrays**

- store any data type- including strings, numbers, and booleans- in an ordered list
  - can have different data types in the same array
- each item has a numbered position

### Array Literal
- preferred method instead of array constructor
- stores data in order
- elements in an array can be the same or different data types
- each element is a key/value pair
- the key is the index number (zero-indexed)
- the value is the item (called an element) in the comma separated list
- is actually a special type of object-with the keys for each value being an index number
- index: an array element's numbered position
- arrays are zero-indexed
  - positions start counting from zero
  - first item will be positioned at zero

#### Array Literal Syntax:
- array items inside square brackets `[]`
- each array item is referred to as an element
- commas between array elements
- can be saved in a variable, such as `let`, `const`, or `var` with the assigment operator `=`
- semicolon after the variable's array 


*Example:* 

 ```
 let colors = ['black', 'orange', 'green'];
 ```

#### Accessing Array Elements Syntax:
- use array name
- then bracket notation `[]` enclosing the index for the item you want to access

*Example:* 

 ```
 colors[0];
 // returns 'black'
 ```
---
![checkmark](../img/checkmark.svg)

#### Accessing Individual Characters in a String
- use bracket notation with an index for the character in the string  

*Example:* 

 ```
 let color = 'midnight';
 console.log(color[2]);
 // output: d
 ```
---
#### Updating Elements Syntax:
- name of the variable containing the array
- brackets `[]` enclosing the index of the array to be updated
- assignment operator `=`
- new elment value
- semicolon `;`
*Example:* 

 ```
 let colors = ['black', 'orange', 'green'];
 colors[1] = 'blue';
 console.log(colors);
 // returns [ 'black', 'blue', 'green' ]
 ```
#### Mutable Arrays Using `const` keyword
- Mutable: array elements can be changed
- cannot reassign a new array or a different value

#### Arrays Using `let` keyword
- Mutable: array elements can be changed
- can be reassigned a new array or a different value

### Arrays: Built-In Properties

- `.length` Property that returns the number of items in the array   
    - use dot notation to chain the `.length` property to the array name
    - end with a semi-colon `;`

---
![checkmark](../img/checkmark.svg)

#### `.length` : `'string'.length` versus `array.length`
```
// the array:
const miscellaneous =['scissors', 'tape', 'pencil', 'coffee'];

// log the length of the array:
console.log(miscellaneous.length);
// logs 4

// log the length of the string:
console.log('miscellaneous'.length);
//logs 13
 ```
 ---

### Arrays: Built-In Methods

### [Link to MDN Documentation for Array Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

- `.concat()`  Method used to join arrays together to create a new array
  - similar to `+` for strings

- `filter()` method executes a callback function on each element in an array which returns either `true` or `false` for each of the elements, then returns a new array with elements for which the callback function returns `true`

- `.indexOf()` Method returns the index of the first element matching the value of the argument 
  - if no matching element is found returns `-1` 
  - original array **remains unchanged**

- `.join()`  Method creates and returns a new string by concatenating all of the elements in an array  
*Example:*
```
items.join('');
// where the space between '' will be inserted between array items
```

- `.lastIndexOf()` Method returns the index of last index matching the value of the argument

- `.pop()`Method that removes the last item of an array  
  - use dot notation and connect to array name
  - removes last element of the array and returns it
  - takes no arguments
  - **mutates** the original array by removing one element

*Example:* 

```
plants.pop();
```

- `.push()` Method that adds items to the end of an array 
  - use dot notation to connect to array name, 
  - call it as a function (because it is a built in function) 
  - add items as arguments, 
  - **mutates** the array by adding elements to the end
  - can be referred to as a 'destructive' array method because it changes the original array 

*Example:*  
    
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

- `.shift()` Method removes the first item from the array and returns the removed element
  - **mutates** the array by removing one element  

*Example:* 

```
array.shift();
```
- `.slice()` Method returns a copy of the array defined by beginning and ending indices, 
  - ending is optional, 
  - if no ending is given the rest of the array to end is returned, 
  - original array **remains unchanged**
  - the ending index is *not* included in the returned array

*Example:* 
```
const animals = [ 'cows', 'horses', 'chickens', 'cats', 'dogs' ]

console.log(animals.slice(1, 4));
// returns [ 'horses', 'chickens', 'cats' ]
```

- `.splice()` Remove selected group of strings and replace with another string  

*Example:* 
```
array.splice(x, y, 'newItem');
// where 'x' is the starting index, 'y' is the number of items
```
- `.unshift()` Method adds the item in its argument to the beginning of the array, 
  - **mutates** the array by adding one element

*Example:*  
      
```
array.unshift('newItem');
```

### Pass-by-reference in Arrays
- if, when an array is passed into a function, the function mutates the array, the array will remain mutated outside the function as well

*Example:*

```
// original array
const miscellaneous =['scissors', 'tape', 'pencil', 'coffee'];

// function to mutate the array
function moreSupplies(add) {
  add.push('ruler');
}

// call function on original array
moreSupplies(miscellaneous);

// log new array to console
console.log(miscellaneous);
// logs [ 'scissors', 'tape', 'pencil', 'coffee', 'ruler' ]
```

### Nested Arrays
- an array containing another array
  - access the nested array with its index
  - chain the indices to access elements within the nexted array
  - remember to put commas `,` between the array elements and the nested array

*Example:*
```
// ['pelican', 'duck'] is its own array inside the nestedArray, notice the comma after 'hawk'

const nestedArray = ['crow', 'eagle', 'hawk',['pelican', 'duck']];

// to call the 'pelican' element:
const birdsWithBigBills = nestedArray[3][0];

console.log(birdsWithBigBills);
// logs pelican
```


