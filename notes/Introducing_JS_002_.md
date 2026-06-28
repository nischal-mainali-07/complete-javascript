###### Page: 002

Here we are again, Hope you have read [JS History](JsHistory_001_.md)

Lets jump on Data Types....

You might be thinking DataTypes?? Directly?

So, Yes DataTypes Directly...

Before JS you might have/have not (Doesnt matter) learned Other languages and you might have observed them explaining how to take INPUT & display OUTPUT....

But, But, But... we dont need that in JS...

We have HTML & CSS to take the input and display output... (HTML and CSS are basically used to handle user interaction and display content on the frontend)

Naturally, the next question arises... Then what does `console.log()` function do?
isint it display output?

The answer to that question is **yes**, it does display output, but it isint made for user rather it is created for developers to test and debug.

##### DataTypes

We have **Primitive** and **Non-Primitive** DataTypes.

Here, we are going to learn Primitive types first — we'll cover Non-Primitive later.

> **Quick Tip:** To check the DataType of any value, use `typeof`. For example:
> ```js
> typeof "hello"  // Output: "string"
> ```

---

**1. String**

There are three ways to represent a String:

- `" "` — Double quotes
- `' '` — Single quotes
- `` ` ` `` — Backticks

Both single and double quotes are equivalent and interchangeable for defining string literals. So then the question arises — why do we have Backticks?

The answer becomes clear with an example. Look at these two cases:

```js
console.log(" He said, " Character is power" ")  // ❌ Problem!
console.log(' He isn' t Lying')                  // ❌ Problem!
```

Can you spot the issue?

In the **first** case, the interpreter sees `" He said, "` as one string and `Character is power" "` as something else — the syntax breaks. In the **second** case, the single quote inside `isn't` closes the string early.

Another limitation: neither single nor double quotes support **multi-line strings**.

This is where `` ` ` `` **Backticks** come in. They are used for **Template Literals**, which:
- Allow **embedded expressions** using `${expression}`
- Support **multi-line strings** natively

```js
let name = "Madhav"
console.log(`Hello, ${name}!
Welcome to JavaScript.`)
// Output:
// Hello, Madhav!
// Welcome to JavaScript.
```

---

**2. Number**

You might have come across `Int` and `Float` in other languages like Java or C++, but in JS all numeric values fall under a single DataType — **Number**.

This also includes special values:
- `Infinity` — Positive Infinity
- `-Infinity` — Negative Infinity
- `NaN` — Not a Number (result of an invalid operation, e.g. `"abc" / 2`)

---

**3. Boolean**

A Boolean can hold one of two values: **`true`** or **`false`**.

It is primarily used for making decisions in your code and is the result of comparison or logical operations.

```js
5 > 3   // true
5 === 4 // false
```

---

**4. Undefined**

`undefined` is a keyword. Any variable that is declared but not assigned a value falls under **Undefined**.

```js
let x;
console.log(x); // undefined
```

---

**5. Null**

`null` is a special value **intentionally assigned** by a programmer to represent the absence of any object value. Think of it as placing an "Empty" label on a box.

Interestingly, in JavaScript:

```js
typeof null // "object"
```

This is actually a **bug** in JavaScript. They could have fixed it, but by the time it was discovered, so many websites had already been built around this behaviour that fixing it would have caused them to break.

---

**6. BigInt**

Used for very large numbers that exceed the safe integer limit of the `Number` type — i.e., beyond **2⁵³ - 1**.

```js
let big = 9007199254740991n  // Notice the 'n' at the end
```

---

**7. Symbol**

*(Honest note: I didn't fully understand this one yet, so here's the definition — we'll revisit it later.)*

A `Symbol` is a **unique and immutable** primitive value, used as a unique identifier for object properties. Its main purpose is to prevent **name collisions** when multiple parts of code work with the same object.