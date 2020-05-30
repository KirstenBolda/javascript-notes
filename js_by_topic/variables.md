## **Variables**
---
## Variable: 
- Container for a value, 
- Provide a way of labeling data with a descriptive name 
- Variables are not the same as values, they *contain* values and represent them with a name
- Three things one can do with variables:
     1. Create the variable
     2. Store or update information stored in the variable
     3. Reference information stored in the variable
- Declared with `var`, `let` and `const` keywords
   - ES6's `let` and `const` are preferred variable keywords
- Naming rules for variables:
    - Cannot begin with a number
    - Are case sensitive
    - Cannot be the same as a keyword
- `let` and `var` can be reassigned or declared without assigning a value
- `const` cannot be reassigned and must have a value assigned when it is declared
    
### Values
- Immutable values: 
  - numbers 
  - strings 
  - Booleans

- Object values (mutable): properties can change, a single object value can have different content at different times
- even simple values can have both methods and properties
- Boolean object is rarely used
### Data Types:

  - Primitive: (simple data type)
    - Number
    - String
    - Boolean
    - Null
    - Undefined
    - Symbol
  - Object (complex data type)
    - Arrays
        - set of key/value pairs where the key is the index number
    - Functions
        - callable
        - classified as first-class objects because they have both properties and values

### Truthy and Falsy Values
- every value in JavaScript can be treated as either true or false
- check if a variable exists and see if the variable has been assigned a value.
#### Falsy Values
- `false`
- `0`
- `''` empty string
- division by zero, `NaN`
- variable with no assigned value

#### Truthy values
- `true`
- numbers other than zero
- strings with content
- number calculations
- `'true'` written as a string
- `'zero'` written as a string
- `'false'` written as a string