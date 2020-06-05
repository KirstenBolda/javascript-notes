# Conditionals

Types of conditionals:

- `if`, `else if`, and `else`, statements
- comparison operators
- logical operators
- truthy vs falsy values
- `switch` statement

---
## `if` statement
- runs a block of code if condition evaluates to `true`

**`if` statement syntax:**
- `if` keyword followed by parentheses `()`
- a code block (block statement) enclosed in curly braces `{}`
- the parentheses enclose a condition that evaluates to `true` or `false`
- if the condition evaluates to `true`, the code block executes
- if the condition evaluates to `false` the code block does not execute

*Example:*
```
if(sunny) {
   console.log('Wear sunscreen!');
}
```
---
## `if` ... `else` statement
- runs a block of code when the `if` condition evaluates to `true` and a different block of code when the condition evaluates to `false`
- used to automate solutions to binary decisions (yes/no questions)
- uses the `else` keyword after the `if` statement code block 

**`if` ... `else` statement syntax:**
- has its own code block wrapped in another set of curly braces
- when the condition for the `if` block doesn't execute, the `else` condition will execute the associated code block

*Example:*
```
if(sunny) {
   console.log('Wear sunscreen!');
} else {
   console.log('Sunscreen optional.');
}
```
## Ternary Operator
- shorthand syntax for an `if ... else` statement
- can be used for conditions that evaluate to `true` or `false`

**Ternary Operator Syntax:**
- the condition entered before the question mark `?`
- two expressions separated by a colon `:` follow the question mark `?`
- if the condition evaluates to `true` the first, left side, expression executes
- if the condition evaluates to `false`, the second, right side, expression executes
---
## `else if` statements
- allow for more conditions to be added in case of more than two possible outcomes
- `else if` comes after the initial `if` condition and before the final `else` statement
- `else if` can be the last statement (`else` is not required, but don't put a condition behind `else`)
- first condition that evaluates to `true` when the code is read from top to bottom will be the block that gets executed


--- 
## Comparison Operators
- used to compare values in conditional statements  
   - have two values to be compared
   - the values are separated by an operator
- compare the value on the left with the value on the right 
- ask "Is left value (comparison operator) than/to right value?"
   - if 'yes' evaluate `true`
   - if 'no' evaluate `false`

**Comparison operators:**
- Relational operators:
  - less than: `<`
  - greater than: `>`
  - less than or equal to: `>=`
  - greater than or equal to: `>=`
- Equality operators:
  - is equal to: `===`
    - Identity-strict equality   
  - is not equal to: `!==`
    - Non-identity-strict inequality

*Example:*
```
let weather = 'sunny';

if(weather !== 'sunny') {
   console.log('Wear sunscreen!');
} else {
   console.log('Sunscreen optional.');
}
```
---
## Logical Operators
 - work with boolean values
 - used in conditional statements to add another layer of logic to the code

 **Logical Operators:**
  - `&&` : the and operator
    - **both** conditions must evaluate to `true` for the condition to execute
  - `||` : the or operator
    - only **one** of the conditions must evaluate to `true` for the condition to execute
  - `!`  : the not operator
      - reverses, or negates, the value of the boolean
*Example:*
```
let weather = 'sunny';
let activity = 'golf';

if(weather == 'sunny' && activity === 'volleyball') {
   console.log('Wear sunscreen!');
} else {
   console.log('Sunscreen optional.');
}
// returns 'Sunscreen optional.'
```
---
## Truthy and Falsy
 - evaluate non-boolean data types inside a condition
 - check if a value exists, but not concerned with the specific value

 **Falsy Values:**
  - `0`
  - Empty strings: `''` or `""`
  - `null` : no value at all
  - `undefined` : declared variable lacks a value
  - `NaN`, Not a Number

#### Short Circuit Evaluation
 - In a boolean condition, JavaScript assigns the truthy value to a variable if you use the `||` operator in your assignment
 - Because `||` or statements check the left-hand condition first, the variable will be assigned the actual value if it is truthy
 - the variable will be assigned the default value, the right hand condition, if the value is falsy

*Example:*

`let defaultName = username || 'Stranger';`  

Because || or statements check the left-hand condition first, the variable `defaultName` will be assigned the actual value of `username` if is truthy, and it will be assigned the value of `'Stranger'` if `username` is falsy.

---

## `switch` keyword

- provides an alternative syntax that is easier to read and write for a large number of values

**Switch Syntax:**
- switch keyword initiates the statement
- the variable that each case will compare is enclosed in parentheses `()`
- the code block contains all the `case`s and is enclosed in curly braces `{}`
- each `case` keyword precedes a value that is compared with the variable's assigned value
- if the values match the code following the colon `:` is executed
- the `break` keyword exits the code, no more cases will be checked (if `return` is used, break is not needed)
- a `default` keyword on the last line precedes code that will run if there are no matching cases in the code block

 ```
  let pets = 'cat';

  switch (pets) {
    case 'dog':
      console.log('Woof');
      break;
   case 'fish':
      console.log('whoosh');
      break;
   case 'cat':
      console.log('Meow');
      break;
   default:
     console.log('Invalid pet');
     break;
}
```


#### Control Flow
- Conditional statements: `if` , `else` , `switch`
- Looping statements: `while` , `do` , `for`
- `switch` statement: a way to check an expression against multiple values. 