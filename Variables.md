### Variables (let, const, var).

There are 3 types of variables in JavaScript: **var**, **let**, and **const**.

The **var** (variable) keyword was originally the only variable available, but thanks to the upgrade to ECMAScript 6 back in 2015, we now have another 2 ways of declaring a variable or data types.

**Quick Overview:**
- **let**: If a variable is going to be reassigned later within the application, this is the ideal variable type to use.
- **var**: It’s better to use either let or const for variables, but this variable type will still work and is still used in applications to this day. This variable can be updated and re-declared.
- **const**: If the variable will never change or won’t be reassigned anywhere else in the application, this keyword is the best option.

**Good things to remember:**
- The **var** variable is globally scoped and can be updated and re-declared.
- The **let** variable is block-scoped and can be updated but not re-declared.
- The **const** variable is block-scoped and cannot be updated or re-declared.

Global Scope: A variable declared outside a function. This means all scripts and functions on a web application or webpage can access this variable.
 
 Block Scope: A variable declared inside a block. This means we can use these variables inside of loops, if statements, or other declarations within curly brackets and have them be only used for that declaration instead of the entire application having access to it.
---
