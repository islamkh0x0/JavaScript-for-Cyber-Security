### User interaction: alert(), prompt(), confirm().

**Note:** You can try all the code examples in the console log. As mentioned before, any JavaScript code can be executed in the console log.

JavaScript allows us the privilege to which we can interact with the user and respond accordingly. It includes several user-interface functions which help in the interaction. Let’s take a look at them one by one.

**JavaScript Window alert() Method** **:** It simply creates an alert box that may or may not have specified content inside it, but it always comes with the ‘OK’ button. It simply shows a message and pauses the execution of the script until you press the ‘OK’ button. The mini-window that pops up is called the ‘modal window’.

```
alert('HI there'); // with specified content 
alert(); // without any specified content
```

---

**JavaScript Window prompt() Method****:** Prompt is another user-interface function that normally contains two arguments.
`prompt('text', default value);`

The text is basically what you want to show the user and the default value argument is optional though it acts like a placeholder inside a text field. It is the most used interface as with it you can ask the user to input something and then use that input to build something.

**Example:** With default parameter.
```
let x = prompt('Are you Hacker?', 'Iam Hacker'); 
  
alert(x);
```

You can enter anything and it will print that, it doesn’t necessarily have to be a number. Without the default value, you have to enter something in the text field otherwise it will print a blank space simply.

**Example:**
```
let age = prompt('How old are you?'); 
  
alert(`You are ${age} years old!`);
```

---

**JavaScript Window confirm() Method** **:** The confirm function basically outputs a modal window with a question and two buttons ‘OK’ and ‘CANCEL’.

Example:
```
// confirm example  
let isHappy  = confirm('Are you Happy?'); 
alert(`You are ${isHappy}`);
```

It will print true or false based on your choice of clicking the ‘OK’ button or ‘CANCEL’ button respectively.
