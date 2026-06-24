###### Page: 002

Here we are again, Hope you have read [JS History](JsHistory.md)

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

We have Premetive and Non-Premetive DataTypes

Here, we are going to learn Premetive type first... Later we will understand non-premetive also.

To know the DataType of any object just type ```typeof hello ``` it will give you the dataType, in this case String. 

1. **String** : There are three ways to represent string:
   - `" "` (Double quotes)

   - `' '` (Single quotes)

   - `` ` ` `` (Backticks)

   What I could understand is that.... Both single and double quote are Equivalent and interchangable for defining string leterals.. 
   Then the question arise then why do we have `` ` ` `` (Backticks) the answer to it is simple.... Imagine you have two Strings ``` 1. console.log(" He said," Character is power" ") ```
   and ```2.  console.log(' He isi'nt Lying')``` Can you spot the problem???

   So in the 1st String if we wanted to quote something within the String it isint possible as the interpreter gives error, it treates ` " He said," ` (Focus on Quotes)as is one string and ` Character is power" "` is the other one and the Syntax seems to be wrong. and its not possible to write multiple line of String with these Quotes... Both for Single and Double Quotes.
    
   But `` ` ` `` Backticks on the other hand are used for template literals, which define a literal String allows embeded expression and multiline Strings. 

2. **Number** 
      -  You might have came across ``Int`` and ``Float`` in other languages like java and C++ but in JS all of them falls under same DataType i.e., **Numbers**
         - Positive Infinity, Negative Infinity, NaN  
          
3. **Boolean**
      - It have one of two Values **TRUE** ``0`` OR **FALSE** `` 1`` It is primarily used for making decision in your code and is the result of Comparision or logical operation. 

4. **Undefined**
      -  It is a keyword, any thing(variable) that is not defined/ not available in our programm that falls under **Undefined** 

5. **Null**
      -  Null is a special value intentionally assigned by a programmer to represent the absence of any object value. Its like placing and "Empty" label on the box.
      Interestingly, in javaScript the DataType of null is actually considered to be an Object, which is a bug.

      They could have fix it but at that time already so many website were build and if they fix it, So many website might get crashed. 

6. **BigInt**
      -  Very large numbers falls under BigInt 2<sup>53-1</sup>

7. **Symbol**
Even i didnt understood this one so this defination is from google. 
   -  It is a unuque and immutable premitive value used as a unique identifier for object properties to prevent name collisions                             