## Operators
---

### Types of Operators
- Assignment Operators: assign a value to a variable
- Arithmetic Operators: perform basic math
- String Operators: combine two strings
- Comparison Operators: compare *values* and return `true` or `false`
- Logical Operators: combine *expressions* and return `true` or `false`

#### Assignment Operators
 - assign a value to the variable  
 *Example:*

     `pet = 'cat';`
#### Arithmetic Operators
- mathematical operators that can be used with numbers
- `+` , `-` , `/` , `*` , `++` , `--` , `%`
- multiplication and division operations are performed before addition and subtraction
- use parenthesis to control the order in which operations are performed
- using arithmetic operators on a string will result in 'not a number':  `NaN`

#### Comparison Operators
  - Condition with one operator and two operands 
  - each operand can be a single value or variable or an expession 
  - will evaluate to a Boolean value (true or false)
  - Types of comparison operators: 
    - `<`  less than
    - `>`  greater than
    - `<=` less than or equal to
    - `>=` greater than or equal to
    - `===` is equal to (strict, both *data **type** and **value*** are the same)
    - `!==` is not equal to  (strict, both *data **type** and **value*** are not the same)

#### Logical Operators
- used to evaluate the results of more than one comparison operator
- Three logical operators:
   - And Operator:
     - `&&` is only true if both values are true (is a Binary Operator)
     - tests more than one condition
  - Or Operator:
    - `||` is true of either one of the values is true (is also a Binary Operator)
    - tests at least one condition
  - Not Operator:
    - `!` flips the value given to it (and is a Unary Operator)
    - inverts the state of an expression

#### Short Circuit Evaluation
- since logical expressions evaluate left to right, if the first (left-side) condition provides enough information to conclude the evalation, the second (right-side) condition is not evaluated

*Example:*
- `let defaultName = username || 'Stranger';`

- Because `||` or statements check the left-hand condition first, the variable `defaultName` will be assigned the actual value of `username` if is truthy, and it will be assigned the value of `'Stranger'` if `username` is falsy.


#### Conditional Operator (also called Ternary Operator)
  - first value ahead of `?` determines whether middle or last value will be returned (is a Ternary Operator)
  - `true ? 1 : 2;`

#### String Operators
 
- concatenate two or more strings using the `+` symbol 

*Example:*

```
let firstName = 'Misty';
let lastName = 'Grey';
let name = firstName + ' ' + lastName;
console.log(name);
// logs Misty Grey
```

#### String Interpolation
 - embed variables into strings using template literals (ES6)
 - use backticks to wrap the template literal

``` 
const firstName = 'Misty';
console.log(`Hi, my name is ${firstName}.`);
// Output: Hi, my name is Misty.
```
#### Member Operator
- object name, then **dot notation**, then the object's property or method 

*Example:*

```
const croissant = breakfastMenu.bakedGoods;
```
#### Shorthand Mathematical Assignment Operators

- `w = w + 1;` is the same as `w += 1;`
- `w = w - 1;` is the same as `w -= 1;`
- `w = w * 1;` is the same as `w *= 1;`
- `w = w / 2;` is the same as `w /= 1;`
- Increment Operator increases the value of the variable by 1:
  - `a = a + 1;` is the same as `a++;`
- Decrement Operator decreases the value of the variable by 1:
  - `b = b - 1;` is the same as `b--;`

#### Increment and Decrement Operators
 - increment operator `++`
   - increases the value of the variable by one
 - decrement operator `--`
   - decreases the value of the variable by one
#### Remainder Operator: `%`
The remainder operator returns the remainder after dividing two numbers. For example, `4 % 2` returns `0`, and `5 % 3` returns `2`.  
The remainder operator is commonly used to find out if a value is even or odd. Even values will have a remainder `0`.

#### Ternary Operator

*Example:*

`walkSignal === 'Walk' ? console.log('You may walk!') : console.log('Do not walk!');`

#### `typeof` Operator
 Checks the data type of a value and a returns a string indicating the data type: (this is a Unary Operator as it takes only one value)
```
let b = 42;
console.log(typeof b);
// returns 'number'
```
#### `delete` Operator
- Unary operator that, when applied to an object property, will remove the named property from the object  
*Example:*
```
delete anObject.left;
```