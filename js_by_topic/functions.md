# Functions

- a reusable block of code that groups together a sequence of statements to perform a specific task
- Grouping together sets of statements that perform a task helps to organize the code  
- Offer a way to store the steps needed to perform a task for eventual deployment  
- Functions are *first class objects*, which can have properties and methods like other objects

 #### Function Declaration Syntax: 
 - function declaration binds a function to an identifier
 - `function` keyword, 
 - the name of the function or its identifier 
 - parentheses `()` with function parameters, if any 
 - function body, the block of statements (semi-colon `;` after each statement) required to perform a specific task enclosed in curly brackets `{ }`
 - no semi-colon `;` after the last curly bracket

 #### Function Execution Syntax: (Function Call)
 - function name
 - parentheses `()` with values or variables as arguments, if any
 - semicolon `;`

## Default Parameters (ES6)
- allow parameters to have a predetermined value in case there is no argument passed into the function or if the argument is undefined when called 
- Use the `=` operator to assign a default value to a parameter: 

#### Default Parameters Syntax: (ES6)
- `function` keyword
- function name
- parentheses `()` with a parameter and equals `=` assigned to a default value
- function body in curly brackets `{}`

*Example:*

  ```
  function greeting (name = 'honored guest') {
    console.log(`Welcome, ${name}!`);
  }
  // call the function with no argument
  greeting();
  // will log 'Welcome, honored guest!'

  // call the function with an argument
  greeting('William Shakespeare');
  // will log 'Welcome, William Shakespeare!'
  ```
## Return
-  use a return statement to pass back information from the function call
- stops execution of the function
- code that follows the `return` statement will not be executed

#### Return statement syntax:
- `return` keyword
- the value to be returned
- semicolon `;`

*Example:*
```
function dessertServings(numGuests, cakes) {
  return ((cakes * 12)/ numGuests);
}

dessertServings(36, 6);
// logs 2 servings
```

## Helper Functions
- function being called within another function 
- breaks large tasks and breaks them into smaller, more manageable tasks
- makes the program easier to read (because the function has a descriptive name) 
- only edit the program in only one place if something changes   

Link provided by Code Mentor:  
[What's a helper function?](https://web.cs.wpi.edu/~cs1101/a05/Docs/creating-helpers.html) 

*Example:*  
```
// the helper function calculates number of pieces per cake
function piecesOfCake(cakes, numPieces) {
  return cakes * numPieces;
}

piecesOfCake(5, 12);
// logs 60

// the function calculates the cost of each piece of cake based on the price of baking the entire batch
function costPerServing(cakes, numPieces) {
  return 500 / piecesOfCake(cakes, numPieces);
}

costPerServing(5, 10);
// logs 10
```

 ## Function Expression
 - alternative to the function declaration format
 - can't be called before the interpreter gets to that statement
 - they are executed when the interpreter encounters them  

#### Function Expression syntax:
- declare a variable as the function's identifier
- common practice to use `const` as the keyword to declare the variable (ES6)
- assign an *anonymous function* as the variable's value
- use the `function` keyword
- parentheses `()` for parameters
- curly braces `{}` to enclose the function body
- semicolon after last curly brace `;`

*Example:*

```
const calculateWeight = function(volume, density) {
  const weight = volume * density;
  return weight;
}
```
#### Invoking a Function Expression syntax:

- enter the name of the variable for the function
- parentheses `()` with any relevant parameters
- semicolon `;`

*Example:*  

```
calculateWeight(volume, density);
```

---

**Anonymous Functions:** 
- don't have a name, are used in **function expressions** 
---

## Arrow Functions (ES6)

#### Arrow Functions syntax:
- use the special “fat arrow” `() =>` notation
- don't need the `function` keyword
- include the parameters inside the `( )` and then add an arrow `=>` that points to the function body surrounded in curly brackets `{ }`  
- use a semicolon after the outer brackets `;`

*Example:*
   ```
  const calculateSpeed = (distance, time) => {
    const speed = distance / time;
    return speed;
  };
   ```
## Concise Body Arrow Functions
 - if a function takes zero or multiple parameters, parentheses `()` are required
 - functions with a single parameter don't need the parameter enclosed in parentheses

 #### Zero Parameters syntax: 
 `const myFunct = () => { some code; };`  
 #### One Parameter syntax:  
 `const myFunct = x => { some code; };`  
 #### Two or More Parameters syntax:  
 `const myFunct = (x, y) => { some code; };`

 #### Implicit Return
 - a function body composed of a single-line block does not need curly braces
 - whatever that line evaluates will be automatically returned
 
 *Example:* 
 - Single Line Code Block with Return Statement: 
```
const myFunct = x => { 
   some code;
   return value;
  };
```

*Example:*  
- Single-Line Block with Implicit Return:

 ```
 const myFunc = x => some code;
 ```


## Higher-Order Function
  - accepts other functions as arguments and/or return functions as output, 
  - gives programmers the ability to build **abstractions**
  - allows more modular code

##  Callback Function
- called during the execution of the higher-order function
- pass in the function itself by typing the function name without the parentheses
- don't evaluate the return value of that function call

### Built-in Math Functions
*Examples:*
- `Math.max`
- `Math.min`
- `Math.random`
- `Math.floor`
- `Math.ceiling`

### Functions Built into Browser
*Examples:*
- `alert();`
- `confirm();`
- `prompt();`