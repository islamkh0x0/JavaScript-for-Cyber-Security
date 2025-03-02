### Logical operators
There are four logical operators in JavaScript: `||` (OR), `&&` (AND), `!` (NOT), `??` (Nullish Coalescing). Here we cover the first three, the `??` operator is in the next lesson.

Although they are called “logical”, they can be applied to values of any type, not only Boolean. Their result can also be of any type.

| Operator | Description | Example                       |
| -------- | ----------- | ----------------------------- |
| &&       | and         | (x < 10 && y > 1) is true     |
| \|\|     | or          | (x == 5 \|\| y == 5) is false |
| !        | not         | !(x == y) is true             |

---

### Comparison Operators
Comparison operators are used in logical statements to determine equality or difference between variables or values.
Let's say that `x=5`

| ==  | equal to                          | x == 8    | false |
| --- | --------------------------------- | --------- | ----- |
|     |                                   | x == 5    | true  |
|     |                                   | x == "5"  | true  |
| === | equal value and equal type        | x === 5   | true  |
|     |                                   | x === "5" | false |
| !=  | not equal                         | x != 8    | true  |
| !== | not equal value or not equal type | x !== 5   | false |
|     |                                   | x !== "5" | true  |
|     |                                   | x !== 8   | True  |
