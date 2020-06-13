## **Objects**
---

- Collections of related data and functionality  
- group of variables and functions to create a model of something from the real world  
- built-in data type
- strings and numbers can behave the same as numbers in some instances

In an Object:
- unordered data is organized into key-value pairs
- **variables** become **properties**
- **functions** become **methods**
- the name is a **key** or **identifier**
- each key-value pair is a property of the object
- the **value** of a **property** can be:
   - string
   - number
   - Boolean
   - array
   - another (nested) object
- the **value** of a **method** is always:
  - a function
- object literal uses colons `:` to separate key/value pairs 
- commas `,` to separate properties **(Very Important! Will cause errors if these are missing!)**
- a **method** is a **property** with a **function** as its **value**
- constructor literal uses `this` instead of object name, `= `to separate key/value variables and semicolons `;` to separate properties

---
### **Create an Object using Literal Notation**

#### Object Literal Syntax
- objects are assigned to variables 
- use curly braces `{}` to designate the object literal
- fill the object with unordered data organized into key-value pairs
  - key name: the **identifier**
    - points to a location holding the value
    - the value can be any data type, including functions or other objects
- key is separated from its associated value by a colon `:`
- key-value pairs are separated by commas `,`
- keys are strings, but quotation marks can be omitted if there are no special characters or spaces in the key name
- values are strings and enclosed with quotation marks
- use a semi-colon after the closing curly brace `};`
 
*Example:*
```
 const objectName = {
     key1 : 'value1',
     key2 : 'value2',
     methodName() {
       return some code;
     }
 };

 ```
 ---
 ### **Create an Object using Constructor Notation**
 
 ```
 const objectName = new Object();
     objectName.key1 = 'value1';
     objectName.key2 = 'value2';
     objectName.methodName = function() {
       return some code;
     };
 ```
 ---
### **Including a method in an object literal**

- Create key-value pairs
- Key is the method name (*identifier*)
- Value is an anonymous function expression
- Omit colon and and `function` keyword in ES6
- Invoked by appending the object's name with the dot operator and the method name with parentheses

*Example:*
```
// pre ES6

const myObject = {
 letUsCode: function () {
   console.log('Learning about Objects!')
 }
};

// ES6 - omit colon : and `function` keyword 

const myObject = {
  letUsCode () {
    console.log('Learning about Objects!')
  }
};

myObject.letUsCode();
// returns:
Learning about Objects!
```

### Nested Objects
- objects may have other objects as properties, and those objects may also have objects within them
- chain objects to access the nested properties or methods

- use the property name and colon syntax
- use curly braces to enclose the object

  ```
  const object = {
    // this is an object property of the 'object'
    _newObject : {
      key : value,
      anotherKey : 'another value
    }
  }
  ```
---
## Accessing Properties and Methods in an Object

### Dot Notation (Member Operator) `.`

#### Dot Notation Syntax
- write name of the object
- use the dot operator `.`
- write property name (key) after the dot
- end the statement with a semicolon `;`
- if an attempting to access a property that doesn't exist operator returns `undefined`

*Example:*
   ```
   destination.name;
   ```

### Bracket Notation `[]`
- *must* use bracket notation when accessing keys that have numbers, spaces, or special characters in them
  - See above, creating an object literal, that keys with numbers, spaces or special characters will already be enclosed in quotes
- can use a variable inside the brackets to select the keys of an object
  - helpful when working with functions

#### Square Bracket Syntax
  - pass the property name (key) between brackets `[]` as a string enclosed in quotation marks `''`
  - used when a variable is used in place of a property name
  - end with a semi-colon `;`

*Example:*
```
destination['name'];
```


### Modifying Key-Value Pairs
- objects are mutable
- if the property already exists, the new value will replace the existing one
- if there is no property with that name, a new property will be added to the object

#### Property Assignment Syntax
- Dot Notation/Assignment Operator: `.`

   `objectName.property = 'newValue';`

- Bracket Notation: `[]`

  `objectName['Property Change'] = 'newValue';`

- delete a property with the `delete `operator

   `delete objectName.property;`  
  Or:  
   `delete objectName['property two'];`

- clear the value of the property without deleting the property key  

  `objectName.property = '';`

#### `this` keyword
  - references the calling object and provides access to its properties when the object's property would otherwise be outside the scope of the method
  - every JavaScript function or method has a `this` context
  - for a function defined inside of an object, `this` will refer to that object itself
  - for a function defined outside of an object, `this` will refer to the global object (`window` in a browser, `global` in Node.js
  - avoid using arrow functions with the `this` keyword, as arrow functions inherently bind, or tie, an already defined `this` value to the function itself that is NOT the calling object. 

#### `Object.keys()` function
 - return a list of an object's properties/keys

    `Object.keys(objectName);`

 #### `Object.assign()` function
 - copies all properties from one object to another

     `Object.assign(source, target);`

#### Iterating through Objects
- use `for ... in` syntax
- can be used to iterate over the keys of an object 
- one of the properties from the object is assigned to the variable of that loop in each iteration 
*Example:*
```
for (let variableName in outerObject.innerObject) {
  console.log(`${variableName}: ${outerObject.innerObject[variableName].propertyName}`)
};
```

#### Privacy in Objects
- only certain properties should be mutable or able to change in value
-  place an underscore `_ `before the name of a property that should not be altered.

### Passing Objects as Arguments
- when objects are passed as arguments to functions or methods, they are **passed by reference**, not by value
- primitive data types are passed by value and not mutable
- means that the object itself (not a copy) is accessible and **mutable** (can be changed) inside that function

### Looping through objects using `for...in`
- executes a block of code for every property in an object
- assign a variable for a key in the object's property
- loop through the object keys using that variable

*Example:* (from Codecademy course)

```
let spaceship = {
    crew: {
    captain: { 
        name: 'Lily', 
        degree: 'Computer Engineering', 
        cheerTeam() { console.log('You got this!') } 
        },
    'chief officer': { 
        name: 'Dan', 
        degree: 'Aerospace Engineering', 
        agree() { console.log('I agree, captain!') } 
        },
    medic: { 
        name: 'Clementine', 
        degree: 'Physics', 
        announce() { console.log(`Jets on!`) } },
    translator: {
        name: 'Shauna', 
        degree: 'Conservation Science', 
        powerFuel() { console.log('The tank is full!') } 
        }
    }
}; 

for (let crewMember in spaceship.crew) {
  console.log(`${crewMember} : ${spaceship.crew[crewMember].name}`)
};

// logs:
captain : Lily
chief officer : Dan
medic : Clementine
translator : Shauna

for (let crewMember in spaceship.crew) {
  console.log(`${crewMember} : ${spaceship.crew[crewMember].degree}`)
};

// logs:
captain : Computer Engineering
chief officer : Aerospace Engineering
medic : Physics
translator : Conservation Science
```


### Getter Method
- used to respect the intention of properties prepended with `_`
- use the `get` keyword followed by a function (method)
- use `this` keyword to access the object's internal properties (the `_` prepended property)
- can perform an action on the data when getting a property
- can return different values using conditionals
- easier for other developers to understand
- don't need to be called with parentheses (so they look the same as properties when called)
- properties cannot share the same name as the getter/setter function-will result in an infinite call stack error

*Example:*  
```
// the object containing a getter method
const person = {
  _firstName: 'Jane',
  _lastName: 'Smart',

  // ----the getter method starts---- //
 get fullName() {
    if (this._firstName && this._lastName){
      return `${this._firstName} ${this._lastName}`;
    } else {
      return 'Missing a first name or a last name.';
    }
  // ----the getter method ends---- //
  }
  // To call the getter method: 
person.fullName; // 'Jane Smart'
  ```

#### Setter Method
- reassign values of existing properties within an object
- used to respect the intention of properties prepended with `_`
- all setters need at least one parameter
- benefits to using setter method:
   - checking input
   - ability to perform actions on properties
   - clear intention for object's purpose
- do not need to be called with a set of parentheses (assigned value becomes method's parameter)
- syntax for a setter looks the same as reassigning the value of a property

*Example:*  
```
// the object containing a setter method
const person = {
  _age: 37,
  // ----the setter method starts---- //
  set age(newAge){
    if (typeof newAge === 'number'){
      this._age = newAge;
    } else {
      console.log('You must assign a number to age');
    }
  }
  // ----the setter method ends---- //
};

// calling the setter method
person.age = 40;
```


#### Factory Functions
- returns an object 
- can be reused to make multiple object instances
- may have parameters that customize the returned object

*Example:*
```
const widgetFactory = (paramA, paramB) => {
  return {
    paramA: paramA,
    paramB: paramB,
    methodSample() {
      //some code here using paramX
    }
  }
};

//--call the widgetFactory function to make a widget object --//

const majorWidget = widgetFactory('widgetA', 'widgetB', 'paramX');

//-- returns a widget object with these parameters:--//

const majorWidget = {
  paramA : 'widgetA',
  paramB : 'widgetB',
  methodSample(paramX) {
    //some code here using paramX
  }
};
```

#### Destructuring: Property Value Shorthand (ES6)
- shortcut for assigning properties to variables in a factory function (ES6)
- property value shorthand: when the property's key and value share the same name remove the` key :` portion to destructure the object

#### Destructured Assignment
- create a variable that matches the name of an object’s key, 
- wrap it in curly braces `{ }` and assign to it the object  
*Example:*  
 *(before destructuring)*  
   `const newVariable = obj.propertyName`  
   `// newVariable = propertyValue`  

  *(after destructuring)*  
   **variable name needs to be exactly the same as the property name in the object**   
    `const {newVariable} = obj;`  
    `console.log(newVariable);`  
    `// prints propertyValue`
#### Array.from
 -  convert a collection of items in an object to a real array   
 ```
 let arrayish = {0: "one", 1: "two", length: 2};
 let array = Array.from(arrayish);
 console.log(array);
 // output is: [ 'one', 'two' ]
 ```
#### Built-in Object Methods
- `Object.assign()`: Copies the values of properties from one or more source objects to a target object
  
  -  *Example:*  
     - `const returnedTarget = Object.assign(target, source);`
    
  - *Example:*
     - target values can be entered as [key, value] pairs
     - `const newObject = Object.assign({attribute1: true, color: azure}, sourceObject);`
- `Object.entries()`: Returns an array containing all of the [key, value] pairs of a given object's string properties  

- `Object.keys()`: Returns an array containing the names of all the object's string properties

- Full list of built-in methods at [MDN Object Instance Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object#Methods)
 # **Global Objects** 

 ![curly-left](../img/curly-left.svg)![curly-right](../img/curly-right.svg)
 ## String Object

Used to work with text stored in variables and objects
- Property
  - `.length` -returns the number of characters (code units) in the string
- Methods
  - `.toUpperCase()` - converts all letters to uppercase
  - `.toLowerCase()` - converts all letters to lowercase
  - `.slice` -returns a copy of the string defined by beginning and ending indices, (ending is optional, if no ending is given the rest of the array to end is returned), original string remains unchanged
  - `.indexOf` -returns the index of the first letter or letters matching the value of the argument(s), if no matching element is found returns -1 , original string remains unchanged
  - `.trim` -removes whitespace from the start and end of a string
  - `.padstart` -takes desired and length and padding character as arguments
  - `.split` -take apart a string with an occurence of another string
  - `.join` -connect strings
  - `.repeat` creates a new string containing multiple copies of the original string joined together 
  - `.startsWith()` - returns a Boolean true or false if the argument matches the first letter of the string
  - `.replace()` - replaces current string with a new string  
  *Example*  
      - `string.replace('current string', 'replacement string');`

![bird creature](../img/bird-creature.svg)
## Number Object
Helpful in financial calculations and animations
- Methods:
  - `isNaN()`
  - `toFixed()`
  - `toPrecision()`
  - `toExponential()`
  - `isInteger()`  
 
 ![check mark](../img/checkmark.svg)  
## Math Object
Resulting number is typically stored as a variable
- Property:
  - `Math.PI`
- Methods:  
  - `Math.round()`
  - `Math.sqrt(n)`
  - `Math.ceil()`
  - `Math.floor()`
  - `Math.random()`

![x-mark](../img/x-mark.svg)
## Date Object
  ##### Use the Date() object constructor
  ##### Will hold today's date and time by default
1. First, create in instance of the date object:  
     `var today = new Date();`
2. Then use any of its properties or methods:
     `var year = today.getFullYear();`
- Methods: (more on page 137 of Duckett textbook)
  - `getDate()`
    - returns the day of the month (1-31)
  - `setDate()`
    - sets the day of the month (1-31)
  - `setDay()`
    - returns the day of the week (0-6)
  - `getFullYear()`
    - returns the year (4 digits)
  - `setFullYear()`
    - sets the year (4 digits)
  -  `toDateString()`
     - returns 'date' as a human readable string
  -  `getTime()`
     - Number of milliseconds since January 1, 1970, 00:00:00 UTC, and a negative number for any time before
Number of milliseconds in a year: 31,556,900,00 (not a leap year)


## Console Object
  - Method
     - `.log()` - information inside the parentheses will get printed, or logged, to the console.  


![worm creature](../img/worm-creature.svg)
## Document Object
  - tree-like structure that organizes the elements on a web page and allows scripting languages to access them
  -  the `document` keyword points to the root node of the Document Object Model (DOM), `<html>`
  #### Properties:

  - `.documentElement` : refers to the object representing the `<html>` tag
  - `.head` and `.body` : for these elements that are present on every web page
  - `.innerHTML` : access and set the contents of an element
  - `.style` : used to access the inline style of an HTML tag
      - use camelCase for style properties instead of hyphens
      - values of the properties are strings (enclose in apostrophes)
  - `.hidden` : hides the selected element by assigning it as `true` or `false`  
     - **not** the same as setting the CSS visibility property to `hidden`
  - `.onclick` : assign a function to run on a click event on an element
  -  `.firstChild` : access to the first child of that parent element
  - `.parentNode` : access the parent element of the variable 
  - `.childNodes` : holds an array-like object, with a `length` property and properties labeled by numbers to access the child node
  - `.children`  : contains only element nodes, not text nodes
  - `.nodeValue`  : holds the string of text the node represents
  - **Accessing Size and Position in JavaScript:**
      - `offsetWidth`
      - `offsetHeight`
      - `clientWidth`
      - `clientHeight`
      - `getBoundingClientRect`
   
  #### Methods:
  - `.querySelector()` : used to specify a CSS selector and then return the first element that matches the selector
     - selector can be a tag `<></>`, a `.class` or `#id`
  - `.querySelectorAll()` : returns a `NodeList` containing all the matching elements
     - returned object is not live
     - use `Array.from` to convert to an array
  - `.getElementsByTagName(` : collects all elements with the given tag name that are descendants (direct or indirect children) of that node and returns them as an array-like object'
  - `.getElementsByClassName()` : searches through the contents of an element node and retrieves all elements that have the given string in their `class` attribute
  - `.getElementByID()` : used to access elements directly by their id
  - `.createElement(tagName)` : creates a new element based on the specified tag name passed into it as an argument
      - creates an empty element with no inner HTML
      - **process appending:** assign created element to be the child of an element that already exists on the DOM
  - `.appendChild()` : add a child element as the last child node
  - `.removeChild()` : removes a specified child node from a parent node
  - `.replaceChild()`  : used to replace one child node with another
    - a new node and the node to be replaced as arguments
    - expects the new node as its first argument
  - `.createTextNode()`  : removes an images and adds a new text node to replace it
  - `.getAttribute()` : access an element by its attribute name, used for not commonly used, non-standard attributes created by the programmer
     - recommended that nons-standard attributes be prefixed with `data-` to distinguish them from standard attribues
     - `class` attribute is accessed under `className` in JavaScript
     - use `getAttribute` to access it under `class`