### Hello World in JS

We can print "Hello World" in multiple ways using JavaScript, but for now, we’ll take a simple look at them. Later, we will explain everything here in more detail.

### Using `console.log()`

First, we have something called the **console log**.

> The **console log** is a debugging tool in JavaScript that allows developers to print messages, test code, and debug applications. It is part of the browser’s Developer Tools and helps developers see the output of their scripts.

To print "Hello World" using the console, we use:
`console.log("Hello World");`

You can try this by opening the browser console (`Ctrl + Shift + i` in Chrome) and typing the above command.

---

### Using `document.write()` and `document.writeln()`

We can also print "Hello World" directly on a web page using:
`document.write("Hello World");`
Or
`document.writeln("Hello World");`

> `document.write()` adds content to the web page dynamically, while `document.writeln()` works similarly but adds a newline (`\n`) at the end of each statement.

It’s important to note that **any JavaScript code can be executed in the console** as well. This means we can run `document.write("Hello World");` directly in the browser console, but it is more commonly used inside an HTML file.

---

### Writing "Hello World" in an HTML Page

Another way to display "Hello World" is by embedding JavaScript inside an **HTML file** using the `<script>` tag:

``` 
<body>     
	<script>
		document.write("<h1>Hello World</h1>");
	</script>
</body>
```

When you open this HTML file in a browser, **"Hello World"** will appear on the page.

---

This is a basic introduction to printing "Hello World" in JavaScript. We will go into more detail about these methods and when to use them later.
