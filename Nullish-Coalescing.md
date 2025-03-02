### Nullish coalescing operator '??'

The `??` operator returns the first argument if it is not **Nullish** (`null` or `undefined`).
Otherwise it returns the second argument.
The common use case for `??` is to provide a default value.

For example, here we show `user` if its value isn’t `null/undefined`, otherwise `Anonymous`:
```
let user;

alert(user ?? "Anonymous"); // Anonymous (user is undefined)
```
this mean if the user undefined make a Default value for it as an Anonymous

Here’s the example with `user` assigned to a name
```
let user = "islam";

alert(user ?? "Anonymous"); // islam (user is not null/undefined)
```

We can also use a sequence of `??` to select the first value from a list that isn’t `null/undefined`.
```
let firstName = null;
let lastName = null;
let nickName = "Hacker";

// shows the first defined value:
alert(firstName ?? lastName ?? nickName ?? "Anonymous"); // Hacker
```
