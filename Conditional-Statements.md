### Conditional statements: if, else, ternary operator (?).

JavaScript conditional statements allow you to execute specific blocks of code based on conditions. If the condition is met, a particular block of code will run; otherwise, another block of code will execute based on the condition.

##### 1. Using if Statement
The if statement is used to evaluate a particular condition. If the condition holds true, the associated code block is executed.

```
let x = 20;

if (x % 2 === 0) {
    console.log("Even");
}

if (x % 2 !== 0) {
    console.log("Odd");
};
```

---
##### 2. Using if-else Statement
Use `else` to specify a block of code to be executed, if the same condition is false

```
let age = 25;

if (age >= 18) {
    console.log("Adult")
} else {
    console.log("Not an Adult")
};
```

---
##### 3. else if Statement
Use `else if` to specify a new condition to test, if the first condition is false

```
if (time < 10) {  
  greeting = "Good morning";  
} else if (time < 20) {  
  greeting = "Good day";  
} else {  
  greeting = "Good evening";  
}
// the result is Good evening
```
---

##### 4. JavaScript Ternary Operator
The Ternary Operator in JavaScript is a shortcut for writing simple if-else statements. It’s also known as the Conditional Operator because it works based on a condition. The ternary operator allows you to quickly decide between two values depending on whether a condition is true or false.

##### How Does the Ternary Operator Work?
The ternary operator works with three parts:
- ****Condition:**** A statement that returns true or false.
- ****Value if True:**** What happens if the condition is true?
- ****Value if False:**** What happens if the condition is false?

****Syntax:****
condition ? trueExpression : falseExpression

Example --> 

```
let age = 60;

let res = (age > 59) ? "Adult" : "Not Adult";

console.log(res);
// res --> Adult
```

if we want to convert it to normal if condition will be like that -->
```
let age = 60; 
let res;

if (age > 59) {
	res = "Adult"; 
} else {
	res = "Not Adult"; 
} 
console.log(res);
// res --> Adult
```

##### Nested Ternary Operators
multiple Conditional operators

```
let marks = 95;
let res = (marks < 40) ? "Unsatisfactory" :
          (marks < 60) ? "Average" :
          (marks < 80) ? "Good" : "Excellent";

console.log(res);

// res --> Excellent
```

