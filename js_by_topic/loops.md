# ![curly line left](../img/curly-left.svg) .. Loops ..   ![curly line righ](../img/curly-right.svg)

- iterate a set of instructions until a stopping condition is met
- create efficient coded to automate processes for scalable, manageable programs

### Three common types of Loops:

- `for`
  - use syntax of a `for` loop is ideal when we know how many times the loop should run
  - most common loop
  - the condition is usually a counter
- `while`
  - when we want a loop to execute an undetermined number of times, `while` loops are the best choice.
- `do while`
  - `do...while` will run at least once whether or not the condition evaluates to `true`
---
## `for` Loop
#### `for` Loop syntax

 - contains three expressions, usually all three with the same **iterator variable**, separated by a semi-colon `;` inside the parentheses:
    
    1. **Initialization** 
       - starts the loop 
       - can also be used to declare the **iterator variable**.
    2. **Stopping condition** 
       - condition that the **iterator variable** is evaluated against
         - if the condition evaluates to true the code block will run
         - if it evaluates to false the code will stop.
    3. **Iteration statement** 
       - used to update the **iterator variable** on each loop.

  *Example:*
   - `for` loop keyword and parentheses
   - `x` is the iterator variable
   - `x = 1` starts the loop
   - `x < 8` stops the loop
   - `x++` updates the iterator variable by one for each run through the loop
   - `console.log(x)` inside the curly brackets `{}` executes as long as `x < 8` (the stopping condition) evaluates to `true`
   ```
   for (let x = 1; x < 8; x++) {
   console.log(x);
 }
   // output is below:
 1
 2
 3
 4
 5
 6
 7
 ```
#### reverse `for` Loop syntax 

  1. Initialize the iterator variable to the *highest* value
  2. Set the stopping condition for the iterator to *less than* the desired end of the loop
  3. Update the iterator to *decrease* after each iteration

*Example:*
   - `for` loop keyword and parentheses
   - `x` is the iterator variable
   - `x = 10` starts the loop
   - `x > 0` stops the loop
   - `x--` updates the iterator variable by one for each run through the loop
   - `console.log(x)` inside the curly brackets `{}` executes as long as `x > 0` (the stopping condition) evaluates to `true`
   ```
   for (let x = 10; x > 4; x--) {
   console.log(x);
 }
   // output is below:
10
9
8
7
6
5
 ```
#### Syntax when looping through an array using `for`
- use the `.length` property in the condition
- iterator variable convention is `i`
   - short-hand for index

*Example:*

```
// an array 
const accounts = ['checking', 'savings', 'money market', 'mutual fund'];

// iterating a for loop over the array
for( let i = 0; i < accounts.length; i++) {
  console.log(`The balance in my ${accounts[i]} is:`);
}
// outputs a list of array items
The balance in my checking is:
The balance in my savings is:
The balance in my money market is:
The balance in my mutual fund is:

// in contrast, logging the array doesn't allow for applying code to the array elements

console.log(accounts);

// outputs the array in brackets
[ 'checking', 'savings', 'money market', 'mutual fund' ]
```

## Nested Loops
- A loop running inside another loop 
- Used for comparingn elements of two different arrays
- Each time the outer loop runs, the inner loop completes all iterations.

#### Syntax for nested loops

- outer loop begins with for `()` and initialization, stopping and iterator settings
- encloses next loop within curly brackets `{}`
- inner loop contains its own for `()` and initialization, stopping and iterator settings
- encloses comparison between outer and inner arrays between its curly brackets `{}`
- each iteration of the outer loop will run *all* the iterations of the inner loop

*Example:*

```
const array1 = ['A', 'B', 'C', 'D', 'E', 'F'];
const array2 = ['Q', 'J', 'B', 'Z', 'D'];
// empty array to received output of nested loops
const arrayBoth = [];

for (let i = 0; i < array1.length; i++) {
  for (let j = 0; j < array2.length; j++) {
    if (array1[i] === array2[j]) {
      // push matches into empty array
      arrayBoth.push(array1[i]);
    }
  }
}
console.log(arrayBoth)
[ 'B', 'D' ]
```
---
## `while` Loop
 - creates a loop that is executed as long as a specified condition evaluates to `true`
 - will continue to run until the condition evaluates to `false`
 - condition is specified before the loop, and usually, some variable is incremented or altered in the `while` loop body to determine when the loop should stop 

 #### Syntax for `while` loops  

1. The iterator variable is declared and initialized before the loop begins
  - since it is before the loop in exists in the global scope
2. Start the loop with the `while` keyword
3. Enclose the stopping condition, also known as the `test condition`, inside parentheses `()`
   - loop will run as long as the test condition evaluates to `true`
   - loop will stop when test condition evaluates to `false`
4. Enclose code block between curly brackets `{}`
5. **Very Important:** Increment the iterator variable at the end of the code block
   - if not incremented the stopping condition will never be met and create an infinite loop, which will freeze up the computer


*Example:*
```
let i = 0;

while (i < 3) {        
  console.log(i);
  i++;
}
// output:
0
1
2

```
---
 
 ## `Do ... While` Statements
 - piece of code runs at least once
 - then loop based on a condition until stopping condition is met

 #### Syntax for `do ... while` loops 
 1. Declare and initialize the iterator variable 
 2. Declare any other needed variables
 3. Code block after the `do` keyword is executed once
 4. Increment the iterator inside the code block
 5. End with the `while` keyword and the stopping condition inside parentheses `()`

*Example:*

```
let stampsNeeded = 1;
let stamps = 0;

do {
  console.log(stampsNeeded);
  stamps ++
} while (stamps < stampsNeeded);
// logs
1
0
```
---
## `break` keyword
- stops code in a loop from executing even if the stopping condition has not been met
- can add test conditions to stop code before stopping conditions are met

#### Performance Issues
- Loops with a lot of items can slow page load times
- If a condition never returns false, (infinite loop) code doesn't stop running until browser runs out of memory
- variables that don't change within the loop should be defined outside of the loop so they are not recalculated each time the loop runs

