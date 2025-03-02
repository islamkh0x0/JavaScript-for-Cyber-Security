### JavaScript Loops
Loops are handy, if you want to run the same code over and over again, each time with a different value.

#### The For Loop
The `for` statement creates a loop with 3 optional expressions:
```
for (begin; condition; step) {
  // ... loop body ...
}
```

##### Example:
```
for (let i = 0; i < 3; i++) { // shows 0, then 1, then 2
  alert(i);
}
```

Let’s examine the `for` statement part-by-part:

| begin     | `let i = 0` | Executes once upon entering the loop                           |
| --------- | ----------- | -------------------------------------------------------------- |
| condition | `i < 3`     | Checked before every loop iteration. If false, the loop stops. |
| body      | `alert(i)`  | Runs again and again while the condition is truthy             |
| step      | `i++`       | It increases by one with each iteration of the value.          |

#### Real-World Example: Looping Through an Array of Usernames
you have a list of usernames and you want to print each one. Instead of writing `console.log()` multiple times, you can use a `for` loop
```
let users = ["islam", "khaled", "Matar", "Macro"];

for (let i = 0; i < users.length; i++) {
    console.log("Welcome, " + users[i] + "!");
}

```

users.length it's mean length of array --> 3
so it will show all user tell rich number 4 or index 4 and stop 
and console log will show this result :

```
Welcome, islam!
Welcome, khaled!
Welcome, Matar!
Welcome, Macro!
```

---

### **While Loop in JavaScript**

The `while` loop **keeps running as long as the condition is `true`**. It is useful when you **don’t know in advance** how many times the loop will run.

##### Example (Counting Numbers)
```
let i = 1;

while (i <= 5) {  
    console.log(i);
    i++;  
}
```
 the console log will show from 1 to 5 


##### Real-World Example
```
 let password;

while (password !== "admin123") {
    password = prompt("Enter the password:");
}

alert("Access granted!");

```

- The loop keeps asking the user for input **until** they enter `"admin123"`.
- Once the correct password is entered, the loop stops, and `"Access granted!"` is shown.
**you can try it in console to see how it work**

##### Summary:

- Use `**for**` → When **you know** the number of iterations.
- Use `**while**` → When **you don’t know** how many times the loop will execute.
