# Loops

### Three common types of Loops:

- `for`
  - use syntax of a `for` loop is ideal when we know how many times the loop should run
  - most common loop
  - the condition is usually a counter
- `while`
  - when we want a loop to execute an undetermined number of times, `while` loops are the best choice.
- `do while`
  - `do...while` will run at least once whether or not the condition evaluates to `true`

#### `for` Loop

 - contains three expressions, usually all three with the same **iterator variable**, separated by `;` inside the parentheses:
    
    1. an initialization starts the loop and can also be used to declare the **iterator variable**.
    2. a stopping condition is the condition that the **iterator variable** is evaluated against— if the condition evaluates to true the code block will run, and if it evaluates to false the code will stop.
    3. an iteration statement is used to update the **iterator variable** on each loop.

  *Example:*
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
#### `while` Loop
 - creates a loop that is executed as long as a specified condition evaluates to `true`
 - will continue to run until the condition evaluates to `false`
 - condition is specified before the loop, and usually, some variable is incremented or altered in the `while` loop body to determine when the loop should stop
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
2
```
#### Looping in Reverse
- set the iterator variable to the *highest* value in the initialization expression
- set the stopping condition to *less than* the desired end of the loop
- *decrease* the iterator after each iteration  
*Example:* (above loop in reverse)
  ```
    for (let x = 8; x >= 0; x--) {
     console.log(x);
   }
    // output is below:
    8
    7
    6
    5
    4
    3
    2
    1
    0
 #### Looping Through an Array
 - Goes over arrays one element at a time by running the counter over the length of the array
 - use the array’s .length property in its condition

 *Example:*
```
const pets = ['cat', 'dog', 'lizard', 'parakeet'];
for (let i = 0; i < pets.length; i++){
  console.log(pets[i]);
}
// outputs:
cat
dog
lizard
parakeet
 ```

#### Nested Loops
- A loop running inside another loop 
- Used for comparingn elements of two different arrays
- Each time the outer loop runs, the inner loop completes all iterations.

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

#### Performance Issues
- Loops with a lot of items can slow page load times
- If a condition never returns false, (infinite loop) code doesn't stop running until browser runs out of memory
- variables that don't change within the loop should be defined outside of the loop so they are not recalculated each time the loop runs

