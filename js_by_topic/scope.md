# Scope 
 - defines where variables can be referenced
 - certain variables are either accessible or inaccessible, depending on whether they are declared inside or outside a block of code

**Block:**
- code found inside a pair of curly braces `{}`
- used in `function`s and `if` statements
- helps group one or more statements together
- defines the scope of variables


**Global Scope:**
- variables declared outside of blocks
- accessible  to every part of the program

**Global Variables:**
- variables declared outside of blocks
- can be accessed by code inside or outside of blocks
- global variables are in the global namespace, where variables are accessible from anywhere in the program
- global variables remain available for the duration of the program

**Block Scope:**
- variables declared inside of blocks
- only accessible to the code between the curly braces `{}`

**Local Variables:**
- variables declared inside of blocks
- only available to the code in the same block

**Scope Pollution:**
- too many global variables in the global namespace rapidly filling up the global namespace
- or reuse of variables across different scopes
- creates difficulties with tracking variables
- potential for accidents and unexpected behavior in the code

**How good scoping improves code:**

- organizes code into discrete sections
- clarifies which variables are associated with parts of the program
- code is modular, thus easier to maintain
- saves memory, as variables don't exist after the block runs


![worm creature](../img/worm-creature.svg)

