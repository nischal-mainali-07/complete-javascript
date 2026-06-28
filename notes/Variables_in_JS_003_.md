# Variables in JavaScript

---

## What are Variables?

When you were in high school, we had maths as a subject and more or less we heard the word **variables** — so what is it? We will learn again...

Remember those maths problems where we use *"let x be the number of apples/umbrellas etc..."*

**Why did we use x?**

We used x, a, y because we were not sure of the value, and the value might change — that's why we called them **variables**, something that *varies*.

---

## Variables in JavaScript

Same concept here in JS. We use variables to store some value — like name, age, city and stuff.

**Why do we do that?**

In our RAM memory, which is like a grid of storage locations, the OS (Operating System) checks the available space and assigns a memory location. Now imagine you want to know what you stored — how will you get the data back? You need something to tell the OS *"I need this"* — that's where variables come into play.

Say you write:

```js
let name = 'Andrew'
```

Now when you say:

```js
console.log(name)
```

You will get `Andrew`. Here we use `name` as a variable to access what we stored. So basically, **variables are labels to the memory location where we store something**.

<img src="/notes/Images/LET.png" width="600" alt="VS code let Variable"/>
<img src="/notes/Images/let console.png" width="600" alt="Console's Output"/>

---

## Three Ways to Declare a Variable

- the keyword **`let`**
- the keyword **`const`**
- the keyword **`var`**

So if variables are all about storing data, then why do we have three types?

Let's understand **scope** first, before diving into each type.

---

## What is Scope?

In BGMI we use a Scope — what does it do? We use it to see how far our enemy is. We have 2x, 4x, 6x and 8x — on increasing x we can see a longer distance, we can see further.

**So what does BGMI have to do with JavaScript?**

In JS, Scope works the same way — it tells you **how far you can use your variable**.

`{ }` curly braces are basically blocks (ifs, for loops, etc.). When you store data inside a block, it's up to you where you want to access it:

- If you want to access a variable **only within the block** it was created in, we call it **Block Scoped** — `let` and `const` fall under this.
- If you declare a variable using `var`, it **ignores the block** and leaks out of it — but it is still limited to the **function** it is written inside. That's why `var` is called **Function Scoped**.

---

## `let`

```js
let name = 'Rahul'
```

You can declare and initialize at the same time.

```js
let name
name = 'Rahul'
```

You can also declare a variable first and initialize it later.

---

## `const`

```js
const name = 'Rahul'
```

You declared and initialized here. But can you declare without initializing in `const`?

```js
const name       // ❌ This will throw an error
name = 'Rahul'
```

**The answer is no.**

You have to declare and initialize `const` at the same time — it's fixed and must be initialized. If you don't initialize it the moment you declare it, JS throws:

```
Missing initializer in const declaration
```

---

## `var`

It works almost the same as `let`:

```js
var name = 'Rahul'
```

You can declare and initialize at the same time.

```js
var name
name = 'Rahul'
```

You can also declare first and initialize later.

---

## So What's the Catch with `var`?

**First** — the scope issue we discussed above.

**Second** — **Hoisting**.

When you use `var`, JavaScript automatically moves the declaration to the top of its scope and sets it as `undefined` before your code even runs. So even if you try to use a `var` variable before you declared it, it won't throw an error — it will just give you `undefined`.

But with `let` and `const`, if you try to access them before their declaration, JS throws a **ReferenceError** — because they sit in what is called a **Temporal Dead Zone (TDZ)** until the line where you declared them is reached.

```js
console.log(a)  // undefined  ✅ (var is hoisted)
var a = 10

console.log(b)  // ❌ ReferenceError (let is in TDZ)
let b = 10
```
---
Lastly,
###### Rules For naming variables. 
1. **Capital Letters:** *A* to *Z*
2. **Small Letter:** *a* to *z*
3. **Digit:** *0* to *9* (But we can't start variable name with digits)
4. **No Special Characters :** Accept ```_``` and ```$``` (We can use this two character "_" and "&" anywhere while naming variables.)
5. It Is prefferd to name you variable in such a way where we can draw sense out of it (e.g. ```sellingPrice``` and ```costPrice``` rather than ```x``` and ```y```), also By convention, JavaScript variable names are written in camelCase.
6. We aren't allowed to use Reserved Key words to name our variables.
---