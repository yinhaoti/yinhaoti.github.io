---
layout:     post
title:      "JavaScript Study Notes - Introduction to JavaScript"
subtitle:   ""
date:       2016-10-11
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - HTML
    - CSS
    - HTML & CSS Study Notes
---

JavaScript is the most widely used programming language on the web and is used on most websites.



#  1. Basic Introduction

Discover the length: `"Haotian".length`

The result would be `7`.



Also, math: `3+4`

The result woud be shown: `7`

> You can use the command line to do basic math operations.

* `*`, `/` , `+`, `-`



## 1.1 Editor and comments

The `//` sign is for comments. 

```javascript
// This is a comment that the computer will ignore. 
// It is for your eyes only!

"cake".length
```

Also, we have multi-line comment, is denoted with `/*  */`.

```javescript
/*
console.log('All of this code');
console.log('Is commented out');
console.log('And will not be executed);
*/
```



## 1.2 What can we use JavaScript for?

- make websites respond to user interaction
- build apps and games (e.g. blackjack)
- access information on the Internet (e.g. find out the top trending words on Twitter by topic)
- organize and present data (e.g. automate spreadsheet work; data visualization)



## 1.3 Interactive

![Screen Shot 2016-10-05 at 12.32.27 PM](/img/in-post/Screen Shot 2016-10-05 at 12.32.27 PM.png)



**Examples:**

```javascript
confirm("I feel awesome!");
```



Also, you can ask for input with a `prompt`.

**Examples**:

```javascript
prompt("What is your name?");
```

![Screen Shot 2016-10-05 at 12.37.42 PM](/img/in-post/Screen Shot 2016-10-05 at 12.37.42 PM.png)



## 1.4 Data types

- **Number**: write a number as numerals without quotes.
- **Strings**: Any grouping of words or numbers surrounded by single quotes: `' ... '` or double quotes `" ... "`.
- **Booleans**: either `true` or `false`.

```javascript
"hello this is wynn"
"hello this is wynn".length
// Length counts every character in the string - including spaces!
//So the result is 18
```

```javascript
23 > 10 //true
5 < 4 //false
```



## 1.5 Using console.log

You may have noticed that the **interpreter** doesn't print out every single thing it does.

`console.log() `will take whatever is inside the parentheses and *log* it to the console 

This is commonly called **printing out**.

```javascript
console.log(2*5) //10
console.log("Hello") //Hello
console.log('bacon', 'pesto');
```



## 1.6 Comparison operators

- `>`Greater than
- `<` Less than
- `<=` Less than or equal to
- `>=` Greater than or equal to
- `===` Equal to
- `!==` **Not** equal to



## 1.7 Decisions, decisions

An `if` statement is made up of the `if` keyword, a condition like we've seen before, and a pair of curly braces` { }`. If the answer to the condition is yes, the code inside the curly braces will run.



Related stuff:

* commonly used library: jQuery
* frameworks: AngularJS, ReactJS and NodeJS




## 1.8 Math Operator: modulus 

a brand new operator called – drum roll please – **the modulus** `%`.

```javascript
console.log(365%27); // 14
```



# 2. Variables

```javascript
var myName = 'Arya';
console.log(myName);
// Output: Arya
```

## 2.1 Create a Variable

`Var` is the JavaScript keyword that will create a new variable for us.

> Variables can hold any data type, like strings, numbers, and Booleans. They can also hold data types that we have not learned yet, like arrays, functions and objects (more on that later).

```javascript
var myAge = 15;
var likesChocolate = true;

console.log(myAge);
// Output: 15

console.log(likesChocolate);
// Output: true
```



## 2.2 Changing a Variable's Value

```javascript
var weatherCondition = 'Monday: Raining cats and dogs';
weatherCondition = 'Tuesday: Sunny';

console.log(weatherCondition); 
// Output: 'Tuesday: Sunny'
```



## 2.3 String Interpolation

> or insert, a variable into a string.

Putting a variable in a string uses concepts we've already learned. The JavaScript term for this idea is interpolation.

We can use the + operator from earlier to interpolate (insert) a variable into a string, like this:

```javascript
var myPet = 'armadillo';
console.log('I own a pet ' + myPet + '.'); 
// Output: 'I own a pet armadillo.'
```






> **Notes taking from** 
> *www.codecademy.com*
