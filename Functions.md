### Functions

Quite often we need to perform a similar action in many places of the script.
For example, we need to show a nice-looking message when a visitor logs in, logs out and maybe somewhere else.

Functions are the main “building blocks” of the program. They allow the code to be called many times without repetition.

We’ve already seen examples of built-in functions, like `alert(message)`, `prompt(message, default)` and `confirm(question)`. But we can create functions of our own as well.

### Function Declaration

To create a function we can use a _function declaration_.

It looks like this:
```
function showMessage() {
  alert( 'Hello everyone!' );
}
```

The `function` keyword goes first, then goes the _name of the function_, then a list of _parameters_ between the parentheses and finally the code of the function, also named “the function body”, between curly braces.

Our new function can be called by its name: `showMessage()`.
For instance:
```
function showMessage() {
  alert( 'Hello everyone!' );
}

showMessage();
showMessage();
```

The call `showMessage()` executes the code of the function. Here we will see the message two times.

This example clearly demonstrates one of the main purposes of functions: to avoid code duplication.

If we ever need to change the message or the way it is shown, it’s enough to modify the code in one place: the function which outputs it.


#### Local variables

A variable declared inside a function is only visible inside that function.
For example:
```
function showMessage() {
  let message = "Hello, I'm islam!"; // local variable

  alert( message );
}

showMessage(); // Hello, I'm islam!

alert( message ); // <-- Error! The variable is local to the function
```


#### Outer variables

A function can access an outer variable as well, for example:
```
let userName = 'John';

function showMessage() {
  let message = 'Hello, ' + userName;
  alert(message);
}

showMessage(); // Hello, John
```
The function has full access to the outer variable. It can modify it as well.

For instance:
```
let userName = 'John';

function showMessage() {
  userName = "Bob"; // (1) changed the outer variable

  let message = 'Hello, ' + userName;
  alert(message);
}

alert( userName ); // John before the function call

showMessage();

alert( userName ); // Bob, the value was modified by the function
```
The outer variable is only used if there’s no local one.

If a same-named variable is declared inside the function then it _shadows_ the outer one. For instance, in the code below the function uses the local `userName`. The outer one is ignored:
```
let userName = 'John';

function showMessage() {
  let userName = "Bob"; // declare a local variable

  let message = 'Hello, ' + userName; // Bob
  alert(message);
}

// the function will create and use its own userName
showMessage();

alert( userName ); // John, unchanged, the function did not access the outer variable
```

---

#### Parameters

We can pass arbitrary data to functions using parameters.
In the example below, the function has two parameters: `from` and `text`.
```
function showMessage(from, text) { // parameters: from, text
  alert(from + ': ' + text);
}

showMessage('Islam', 'Hello!'); // Islam: Hello! (*)
showMessage('Islam', "What's up?"); // Islam: What's up? (**)
```

When a value is passed as a function parameter, it’s also called an _argument_.

In other words, to put these terms straight:

- A parameter is the variable listed inside the parentheses in the function declaration (it’s a declaration time term).
- An argument is the value that is passed to the function when it is called (it’s a call time term).

We declare functions listing their parameters, then call them passing arguments.

In the example above, one might say: “the function `showMessage` is declared with two parameters, then called with two arguments: `from` and `"Hello"`”.

#### Default values

If a function is called, but an argument is not provided, then the corresponding value becomes `undefined`.

For instance, the aforementioned function `showMessage(from, text)` can be called with a single argument:
`showMessage("islam");`

That’s not an error. Such a call would output `"*islam*: undefined"`. As the value for `text` isn’t passed, it becomes `undefined`.

We can specify the so-called “default” (to use if omitted) value for a parameter in the function declaration, using `=`:
```
function showMessage(from, text = "no text given") {
  alert( from + ": " + text );
}

showMessage("Islam"); // Islam: no text given
```
Now if the `text` parameter is not passed, it will get the value `"no text given"`.

---

Real-World Example: Checking a User's Password
```
function authenticateUser(username, password) {
    const storedUsername = "admin";
    const storedPassword = "admin123";

    if (username === storedUsername && password === storedPassword) {
        return "Login successful! ";
    } else {
        return "Invalid credentials ";
    }
}

// Testing the function
console.log(authenticateUser("admin", "admin123")); //  Login successful!
console.log(authenticateUser("user", "password"));  //  Invalid credentials

```

**Try it to know how it's work **
