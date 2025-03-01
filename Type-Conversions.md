## Type conversions (Number(), String(), Boolean()).  
### String Conversion  

String conversion happens when we need the string form of a value.
For example, `alert(value)` does it to show the value.
We can also call the `String(value)` function to convert a value to a string:

```
let x = true;
alert(typeof x); // boolean

value = String(x); // now value is a string --> "true"
alert(typeof x); // string
```

String conversion is mostly obvious. A `false` becomes `"false"`, `null` becomes `"null"`, etc.

---
### Numeric Conversion

Numeric conversion in mathematical functions and expressions happens automatically.
For example, when division `/` is applied to non-numbers:
```
alert( "6" / "2" ); // 3, strings are converted to numbers
```

We can use the `Number(value)` function to explicitly convert a `value` to a number:
```
let str = "123";
alert(typeof str); // string

let num = Number(str); // becomes a number 123 without ""

alert(typeof num); // number
```

Explicit conversion is usually required when we read a value from a string-based source like a text form but expect a number to be entered.

If the string is not a valid number, the result of such a conversion is `NaN`. For instance:

```
let age = Number("an arbitrary string instead of a number");

alert(age); // NaN, conversion failed
```

##### There is Rules For Numeric conversion --> 
Number(true) --> 1  
Number(false) -->0  
empty String : Number("") --> 0  

---
### Boolean Conversion

Boolean conversion is the simplest one.
##### The conversion rule -->

- Values that are intuitively “empty”, like `0`, an empty string, `null`, `undefined`, and `NaN`, become `false`.
- Other values become `true`.

```
alert( Boolean(1) ); // true
alert( Boolean(0) ); // false

alert( Boolean("hello") ); // true
alert( Boolean("") ); // false

alert( Boolean("0") ); // true
alert( Boolean(" ") ); // spaces, also true (any non-empty string is true)
```

