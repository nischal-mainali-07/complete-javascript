## Code Execution in JavaScript

As a programmer, it is essential to understand what happens behind the scenes when JavaScript runs your code, so that when you encounter a bug, you know exactly where to look.

### There are Two Phases of Execution

1. *Memory Creation Phase*
2. *Code Execution Phase*

Let's dive into each one.

---

### 1. Memory Creation Phase

In this initial phase, the JavaScript engine scans through the entire code **before executing a single line**. It looks for all variable and function declarations — `var`, `let`, and `const` — and allocates memory for them.

- Variables declared with `var` are stored in memory with the value `undefined`.
- Variables declared with `let` and `const` are also hoisted, but they are placed in a **Temporal Dead Zone (TDZ)** — meaning they exist in memory but cannot be accessed until the line where they are declared is reached.

> This is why accessing a `var` variable before its declaration gives you `undefined`, while accessing a `let` or `const` variable before its declaration throws a `ReferenceError`.

---

### 2. Code Execution Phase

Once the memory allocation is complete, the JavaScript engine executes the code **line by line**. As each line runs:

- Variables that were holding `undefined` now receive their actual assigned values.
- JavaScript automatically determines the data type of each value at this stage, since JS is a **dynamically typed** language.

---

### Practical Demo Using Chrome DevTools

To see this in action, we write code in our [`script.js`](https://raw.githubusercontent.com/nischal-mainali-07/complete-javascript/refs/heads/main/code/script.js) and [`Index.html`](https://raw.githubusercontent.com/nischal-mainali-07/complete-javascript/refs/heads/main/code/Index.html) files.

We then go live and open **DevTools → Sources tab**, where we can step through execution using the debugger.

The images below show a step-by-step walkthrough of how variables move from `undefined` (memory phase) to their actual values (execution phase).

[Console Debugger Steps](http://127.0.0.1:5500/code/CodeExecution.html)

---

### A Note on the `defer` Attribute

Since we have linked our script inside the `<head>` element:

```html
<script src="script.js"></script>
```

We should add the `defer` attribute:

```html
<script src="script.js" defer></script>
```

**Why?** Without `defer`, the browser stops parsing the HTML as soon as it encounters the `<script>` tag, fetches the file, and executes it — which can cause issues if the script tries to access HTML elements that haven't loaded yet.

With `defer`, the browser **downloads the JS file in parallel** while continuing to parse the HTML. The script only **executes after the HTML is fully parsed**. This ensures the DOM is ready before your JavaScript runs.