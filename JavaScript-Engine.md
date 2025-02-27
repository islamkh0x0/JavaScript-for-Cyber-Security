### In order to know how JavaScript works, we must know what JavaScript Engine is.
A **JavaScript engine** is a program that **interprets and executes JavaScript code** inside a web browser or server. Every modern browser has its own JavaScript engine that **parses, compiles, and runs JavaScript efficiently**.
- Google Chrome --> V8 Engine
- Mozilla Firefox --> SpiderMonkey Engine
- Microsoft Edge --> Chakra Engine
### From here we can know how The JavaScript Working.
When you load a webpage, JavaScript runs inside the **JavaScript Engine** of the browser or on the **server**, It follows a specific execution process:
1. **Parsing:** The engine reads JavaScript code and converts it into an **Abstract Syntax Tree (AST)**.
2. **Compilation:** Modern JavaScript engines use **Just-In-Time (JIT) compilation** to convert JS code into machine code for faster execution.
3. **Execution:** The JavaScript Engine executes the code line by line using the **Call Stack** and **Event Loop**
