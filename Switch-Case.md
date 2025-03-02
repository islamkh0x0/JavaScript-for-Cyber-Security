### **Switch Statement in JavaScript**

The `switch` statement in JavaScript is used for decision-making when you need to compare a variable against multiple possible values. Instead of writing multiple `if-else` statements, a `switch` can make the code more readable and efficient.

#### Example
The `switch` has one or more `case` blocks and an optional default.
It looks like this:
```
let a = 2 + 2;

switch (a) {
  case 3:
    alert( 'Too small' );
    break;
  case 4:
    alert( 'Exactly!' );
    break;
  case 5:
    alert( 'Too big' );
    break;
  default:
    alert( "I don't know such values" );
}
```

The alert here will be Exactly!
Here the `switch` starts to compare `a` from the first `case` variant that is `3`. The match fails.
Then `4`. That’s a match, so the execution starts from `case 4` until the nearest `break`.
**If there is no `break` then the execution continues with the next `case` without any checks.**

An example without `break`:
```
let a = 2 + 2;

switch (a) {
  case 3:
    alert( 'Too small' );
  case 4:
    alert( 'Exactly!' );
  case 5:
    alert( 'Too big' );
  default:
    alert( "I don't know such values" );
}
```
In the example above we’ll see sequential execution of three `alert`s: 4, 5, default.


Now if we want to convert the first Example from `switch` to `if, else` To compare them

will be like this
```
let a = 2 + 2;

if (a === 3) {
    alert('Too small');
} else if (a === 4) {
    alert('Exactly!');
} else if (a === 5) {
    alert('Too big');
} else {
    alert("I don't know such values");
}

```
