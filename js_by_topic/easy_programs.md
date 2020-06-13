# Simple Programs 

                
![Bug Eyes](../img/bug-eyes-creature.svg)  For Newbie Programmers!
---

### **Adding all the numbers in an array using a `for` loop**
- note: this can also easily be accomplished using the `reduce` iterator method

```
// 1. Create an array with the numbers to be added:

   const numbers = [2, 6, 12, 8, 9];

// 2. Initialize the variable that will contain the total:

    let sum = 0;  

// 3. Write the for loop with a stopping condition that ends at the last item in the array:* 

     for (i = 0; i < numbers.length; i++) {
    sum += numbers[i]
     }

// 4. Log the result to the console:

      console.log(sum);  
```
---
### **Separate a paragraph into an array of single words**

```
// 1. Create a variable with the paragraph in a string: 

   let words = 'Locavore vexillologist green juice, selvage cray bitters ramps edison bulb jianbing subway tile chartreuse actually readymade. Before they sold out quinoa glossier, blog umami vegan affogato cornhole helvetica mixtape. Gluten-free typewriter copper mug, lo-fi beard jean shorts tacos street art fashion axe hammock.';

// 2. Create another variable and apply the .split method to the paragraph using a space as the parameter:

   const splitWords = words.split(' ');

// 3. log the new array of separated words:

   console.log(splitWords);

// 4. Bonus: console.log the length of the new array to count the words:

   console.log(splitWords.length);
```
---
### **Create an array of the first letters of each word in an array**

```
// 1. Create an array of words:

   let randomWords = ['Locavore', 'vexillologist','green','juice', 'selvage', 'Gluten-free','typewriter', 'copper', 'affogato', 'jean', 'quinoa', 'tile','tacos', 'hammock' ];

// 2. Create a new array and use the .map iterator to loop through the word array:

  let firstLetter = randomWords.map(  )

// 3. Create a callback function to list the first letter in each word's string

   let firstLetter = randomWords.map( initial => {
    return initial[0];
  })

// 4. log the new array of first letters to the console

   console.log(firstLetter);

```
---
### **Generate a random whole number between 1 and 100**

```
// Generate a random decimal between 0 (inclusive) and 1 (exclusive) using Math.random()

Math.random();

// Multiply the random decimal by 100 to generate random decimals in the 0 to 100 range

Math.random() * 100;

// Round down the random decimal to a random whole number using the Math.floor method

Math.floor(Math.random() * 100);

// log the result to the console

console.log(Math.floor(Math.random() * 100;));
```
---
### **Log the elements of an array inside an object to the console**






