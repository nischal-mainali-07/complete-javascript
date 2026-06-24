## History of JS

###### While writing these notes, I myself am learning. There may be some errors but the notes below are in best knowledge of mine. These notes are for someone who has just started learning — all the problems I have faced and doubts I had are covered here.

---

When it comes to the History of JS, there were a couple of events that we need to understand.

Do you know **NETSCAPE** (now Mozilla)?

![Netscape Logo](Images/Netscape-Logo.png)

NETSCAPE happens to be the First Commercially Successful Browser that Popularized the web for public use, and they say that 90% of users used NETSCAPE as their Preferred Browser.

*MARC ANDREESSEN & JIM CLARK*, the Founder and Co-Founder of Netscape, were determined to make the Web Interactive, so they hired **BRENDAN EICH** in **1995**.

**BRENDAN EICH** is the creator of JavaScript. He developed the First Prototype of JS in **10 DAYS**.  
Initially it was named **Mocha**, then **LiveScript**, and today we know it as **JAVASCRIPT**.

You might think — why is it named JAVASCRIPT when it has nothing to do with JAVA?

Yes, it's true that it has nothing to do with JAVA, yet they named it JAVASCRIPT because the word JAVA was really popular... it was strategically chosen to capture the immense hype and popularity.  
Also, Netscape made a deal with **SUN MICROSYSTEMS** (now ORACLE) to use the name JAVASCRIPT, linking their new language to the fame of SUN's JAVA.

---

#### CONFLICT STARTED

It all started when Netscape released JavaScript in **1995**. It was a huge success, making web pages interactive for the first time...

Like in every story, when something good is happening, there are conflicts.  
So, after all the achievements, Netscape had to face trouble... and what was it?

**Microsoft.** Yes, Microsoft decided to create their own version of the language called **JScript** for Internet Explorer 3.0.

Because Microsoft developed their own version without Netscape's collaboration, the two implementations were largely incompatible, leading to a lot of frustration for developers who had to write different code for each browser.

---

### What was the solution?

So, Netscape went to **ECMA** (European Computer Manufacturers Association). ECMA is a body that creates standards for computers. Netscape submitted JavaScript in late **1996** to have it Standardized. This led to the creation of the **ECMAScript Standard**, which ensures a unified standard that all browsers can follow.

Hence JavaScript became the most popular Scripting language.

Emphasizing how popular JS became — here we have a law, **Atwood's Law**:

> *"Any application that can be written in JAVASCRIPT will eventually be written in JAVASCRIPT."*

---

### Jeff Atwood

**Jeff Atwood** is known as the co-founder of **Stack Overflow** (and Stack Exchange).  
He gained a significant following through his widely read coding blog.

📖 [Coding Horror — Jeff Atwood's Blog](https://blog.codinghorror.com/)

###### Console in the Browser.
**Refer a video in this case**

[Youtube](https://www.youtube.com/watch?v=-lBfLogYtZk&list=PLfEr2kn3s-bo4LwlbyZugHPavhcdW8YMC&index=6)

Still i am writing for your understanding. 

1. Create a folder in you VS Code say **WebDev** and create Two files ```index.html``` and ```script.js```now link the .js file in html file ``` <script src="script.js"></script> ``` inside ``` <head>``` we could place ``` <script src="script.js"></script> ``` anywhere in our code but for now we are inserting it on ```<head>``` It has its own Pros and Cons... Reffer the image below. 
![Visual Studio .html ScreenShot](/notes/Images/Screenshot%202026-06-25%20013628.png)
Create .js file and Type ``` console.log("Hello World")```
![Visual Studio .js ScreenShot](/notes/Images/Screenshot%202026-06-25%20013644.png)

2. Go live (Use extention Live server) in the ```.html ``` file now you will see![Browser Screen Shot](/notes/Images/Screenshot%202026-06-25%20014310.png)
3. Now Right Click and Click on inspect.
4. You will see devloper tools interface. 
5. click on Console 

6. We can write java Script code and see output as well, You could call it console but its called REPL(Read,Eval,Print,Loop)
whatever you typed in .js file will be visible here. 
