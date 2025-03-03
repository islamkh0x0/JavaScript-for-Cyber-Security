# JavaScript - Browser Object Model

## Browser Object Model in JavaScript

The Browser Object Model (BOM) in JavaScript helps to interact with the browser, not just the webpage. While the DOM handles the content of the page, BOM gives you control over things like the browser window, the URL, and the Cookies.


###  `window.location` in JavaScript**

The `window.location` object in JavaScript provides details about the current page URL and allows you to modify it. It’s commonly used for getting URL information, redirecting users, or reloading the page.

---

### **Main Properties of `window.location`**

Here’s a breakdown of its key properties:

|Property|Description|Example Output|
|---|---|---|
|`window.location.href`|The full URL of the page|`"https://example.com/page.html?search=query"`|
|`window.location.protocol`|The protocol used (`http:` or `https:`)|`"https:"`|
|`window.location.host`|The domain name and port (if any)|`"example.com"` or `"localhost:3000"`|
|`window.location.hostname`|The domain name only (without port)|`"example.com"`|
|`window.location.port`|The port number (if any)|`"3000"` (if running on `localhost:3000`)|
|`window.location.pathname`|The path after the domain|`"/page.html"`|
|`window.location.search`|The query string (after `?`)|`"?search=query"`|
|`window.location.hash`|The fragment identifier (after `#`)|`"#section1"`|
|`window.location.origin`|The full URL origin (protocol + hostname + port)|`"https://example.com:8080"`|

---

### **Example: Getting URL Information**

```js
console.log("Full URL:", window.location.href);
console.log("Protocol:", window.location.protocol);
console.log("Host:", window.location.host);
console.log("Hostname:", window.location.hostname);
console.log("Port:", window.location.port);
console.log("Pathname:", window.location.pathname);
console.log("Query String:", window.location.search);
console.log("Hash:", window.location.hash);
console.log("Origin:", window.location.origin);

```

**If the page URL is:**  
 `https://example.com:8080/page.html?search=bug#results`  
This code will output:

```
Full URL: https://example.com:8080/page.html?search=bug#results
Protocol: https:
Host: example.com:8080
Hostname: example.com
Port: 8080
Pathname: /page.html
Query String: ?search=bug
Hash: #results
Origin: https://example.com:8080

```

---

### **Redirecting & Reloading the Page**

You can use `window.location` to navigate or refresh the page dynamically.

#### **1. Redirect to Another Page**
`window.location.href = "https://google.com";`  
Acts like clicking a link.

#### **2. Reload the Page**
`window.location.reload();`  
 Equivalent to pressing **F5**.

#### **3. Navigate Without Keeping History**
`window.location.replace("https://example.com");`
Unlike `href`, this removes the current page from history, so the user **can’t go back**.

---

### **Modifying URL Parts Dynamically**

You can change specific parts of the URL.
#### **1. Update the Query String**
`window.location.search = "?user=Islam&role=admin";`
Changes the query parameters.

#### **2. Change the Hash**
`window.location.hash = "#section3";`
 Scrolls to `#section3` **without reloading**.

---

#### **Example: Redirect Based on User Choice**
```html
<button onclick="goToAdmin()">Go to Admin Panel</button>
<button onclick="goToUser()">Go to User Dashboard</button>

<script>
    function goToAdmin() {
        window.location.href = "https://example.com/admin";
    }

    function goToUser() {
        window.location.href = "https://example.com/user";
    }
</script>

```
clicking a button redirects the user to a different page.


---
## JavaScript Cookies

Cookies are small pieces of data stored in the browser, mainly used for tracking user sessions, storing preferences, and authentication. JavaScript allows you to **create, read, and delete** cookies using the `document.cookie` property.

### **How Cookies Work**

A cookie is a simple key-value pair stored in the browser. Here’s an example:
```
username=Islam; expires=Fri, 31 Dec 2025 23:59:59 GMT; path=/
```
- `username=Islam` → Stores the user’s name.
- `expires=...` → Sets the expiration date.
- `path=/` → Cookie is accessible across the whole website.


### **Creating a Cookie**

You can set a cookie using `document.cookie` like this:
```js
document.cookie = "username=Islam";

```

This creates a basic cookie **without an expiration date**, meaning it will be deleted when the browser closes (a **session cookie**).

#### **Setting an Expiration Date**

To make a cookie persist, you must add an `expires` attribute.
```js
document.cookie = "username=Islam; expires=Fri, 31 Dec 2025 23:59:59 GMT";

```
This cookie will **stay** in the browser until **December 31, 2025**.

#### **Setting a Path**

If you want the cookie to be accessible across all pages, add `path=/`:
```js
document.cookie = "username=Islam; expires=Fri, 31 Dec 2025 23:59:59 GMT; path=/";

```
Without `path=/`, the cookie is **only available on the current page**.

### **Reading Cookies**

You can retrieve all cookies using:
```js
console.log(document.cookie);

```
This returns a string of all cookies:
```
"username=Islam; theme=dark; language=en"

```
Since cookies are stored as a **single string**, you may need to parse them manually.

#### **Extracting a Specific Cookie**

Example: Get the `username` cookie.
```js
function getCookie(name) {
    let cookies = document.cookie.split("; ");
    for (let i = 0; i < cookies.length; i++) {
        let [key, value] = cookies[i].split("=");
        if (key === name) {
            return value;
        }
    }
    return null;
}

console.log(getCookie("username"));  // Output: Islam

```


### **Updating a Cookie**

To update a cookie, you **set it again** with the same name but a new value.
```js
document.cookie = "username=Matr; expires=Fri, 31 Dec 2025 23:59:59 GMT; path=/";

```
The `username` cookie is now `"Matr"`.

