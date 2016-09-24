---
layout:     post
title:      "HTML & CSS Study Notes - CSS Classes and IDs"
subtitle:   ""
date:       2016-09-23
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - HTML
    - CSS
    - HTML & CSS Study Notes

---



# Unit 5 CSS Classes and IDs

## 1.1 All HTML elements are selectors

All HTML elements are selectors. eg. HTML tags `<h1></h1>` with the CSS selector `h1`, `<p></p> `with `p`.

Thus, any HTML element can be a CSS selector.

```css
body {
    background-color: #C6E2FF;
}
```



## 1.2 Multiple Selectors

 it's possible to nest HTML elements inside one another, like so:

```html
<div>
    <div>
        <p>I like tacos!</p>
```

So you can  grab `<p>`s that are inside two <div>s, and not all <p>s:

```css
div div p {
    /*CSS stuff!*/
}
```



## 1.3 One selector to rule them all

You can use `*` **universal selector** to change the every element on HTML page.

```css
* {
    border: 2px solid black;
}
```



## 1.4 Example

*index.html*

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>Strut Your Stuff!</title>
	</head>
	<body>
		<p>I'm about to become a lovely shade of teal.</p>
		<p>Me, too!</p>
		<p>I think I'll do the same.</p>
		<div>
			<p>We're going to become a truly striking scarlet!</p>
			<p>I was thinking more vermillion.</p>
			<p>No, crimson!</p>
		</div>
	</body>
</html>
```



*stylesheet.css*

```css
/*Add your CSS below!*/
p {
    color: #00E5EE;
}

div p {
    color: #CC0000;
}

* {
    border: 2px dashed #3A5FCS;
}
```

*shown:* 

![Screen Shot 2016-09-23 at 4.33.25 PM](/img/in-post/Screen Shot 2016-09-23 at 4.33.25 PM.png)





## 2.1 Branching

Think of an HTML document as a tree: elements "branch out" from the main trunk.

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>The Great Tree of HTML</title>
	</head>
	<body>
		<div id="p1">P</div>
		<div id="p2">P</div>
		<div id="p3">P</div>
		<div class="space"></div>
		<div id="title">Title</div>
		<div id="div">Div</div>
		<div class="space"></div>
		<div id="head">Head</div>
		<div id="body">Body</div>
		<div class="space"></div>
		<div id="html">HTML</div>
	</body>
</html>
```

```css
div {
	border-radius: 5px;
	border: 2px solid #6495ED;
	background-color: #BCD2EE;
	height: 18px;
	text-align: center;
	font-family: Garamond, serif;
}

#p1 {
	display: inline;
	position: relative;
	margin-left: 138px;
}

#p2 {
	display: inline;
	position: relative;
	margin-left: 10px;
}

#p3 {
	display: inline;
	position: relative;
	margin-left: 10px;
}

#div {
	display: inline;
	position: relative;
	margin-left: 70px;
	margin-top: 10px;
}

#title {
	display: inline;
	position: relative;
	margin-left: 50px;
}

#body {
	display: inline;
	position: relative;
	margin-left: 25px;
}

#head {
	display: inline;
	position: relative;
	margin-left: 65px;
}

#html {
	width: 50px;
	position: relative;
	margin-left: 93px;
}

.space {
	opacity: 0;
}
```

 ![Screen Shot 2016-09-23 at 4.37.13 PM](/img/in-post/Screen Shot 2016-09-23 at 4.37.13 PM.png)

## 2.2 Parents, children, and siblings

* `<html>` tag as the trunk of the tree, its immediate branches—`<head>` and `<body>`—as its **children**. `<html>` is their **parent** element.
* Because they are both immediate children of `<html>` (that is, they are both only one element away), they are **siblings**.

```html
<!DOCTYPE html>
<html> <!--The trunk of the tree!-->
	<head> <!--Child of html, parent of title,
		   sibling of body-->
		<title></title> <!--Immediate child of head,
						child of head AND html-->
	</head>
	<body> <!--Child of html, parent of p,
		   sibling of head-->
		<p></p> <!--Immediate child of body,
				child of body AND html-->
	</body>
</html>
```



## 2.3  Branch to Branch

You can reach an element that is a child of another element like this:

`div div p { /* Some CSS */ }`

that is grabbing any `<p>` that is nested somewhere inside a `<div>` that is nested somewhere inside another `<div>`



Also, ff you want to grab direct children—that is, an element that is directly nested inside another element, with **no elements in between**—you can use the `>` symbol, like so:

div > p { /* Some CSS */ }



**Example:**

*index.html*

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>Ultimate Text Challenge</title>
	</head>
	<body>
		<p>Introduction: Cascading with CSS</p>
		<div>
			<p>Synopsis: When you set a property of a selector like 'p' to a certain value, that value applies to <em>all</em> p tags.
			If, however, you change that same property to a different value for a more specific instance of p,
			that change will <em>override</em> the 'general rule'.
			</p>
			<ul>
				<li><p>If you say p { font-family: Garamond}, all 'p's will have the font Garamond.</p></li>
				<li><p>BUT if you say li p {font-family: Verdana}, 'p's outside of 'li's will be
					   in Garamond, and 'p's INSIDE 'li's will be in Verdana.
				</p></li>
				<li><p>The more specific your selectors are, the higher importance CSS gives to the styling you apply!</p></li>
			</ul>
		</div>
		<p>Summary: Greater specificity makes CSS prioritize that particular styling.</p>
	</body>
</html>
```

*stylesheet.css*

```css
/*Add your CSS below!*/
p {
    font-family: Garamond;
}

body > p {
    font-weight: bold;
}

div > p {
    color: #7AC5CD;
}

ul li p {
    color: #000000;
    text-decoration: underline;
}
```

*Shown:* ![Screen Shot 2016-09-23 at 4.57.46 PM](/img/in-post/Screen Shot 2016-09-23 at 4.57.46 PM.png)





**Notice:**  learn more about cascading.

* certain selectors `ul li p{}` will "override" others `p{}`.
* There are two selectors that are even more specific than nested selectors like the ones above: classes and IDs. 



## 3 Class and ID Selectors

There are two important selectors you can use in addition to the universal selector and HTML elements: **classes** and **IDs**.

### 3.1 Class

You can simply apply the **same class** to all those HTML elements, then define the styling for that class in the CSS tab.

HTML with the `word` class and an equals sign

```html
<div class="square"></div>
<img class="square"/>
<td class="square"></td>
```

CSS (classes are identified in CSS with a dot `.`

```css
.square {
    height: 100px;
    width: 100px;
}
```

### 3.2 IDs

**IDs,** on the other hand, are great for when you have **exactly one element** that should receive a certain kind of styling.

HTML: with the word `id` and an equals sign

```html
<div id="first"></div>
<div id="second"></div>
<p id="intro"></p>
```

CSS:  identified in CSS with a pound sign (`#`)

```css
#first {
    height: 50px;
}

#second {
    height: 100px;
}

#intro {
    color: #FF0000;
}
```

### 3.3 Example

*index.html*

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>Result</title>
	</head>
	<body>
		<h2 id="intro">Introduction</h2>
		<h3 class="standout">Classes and IDs in CSS</h3>
		<p class="standout">Classes and IDs are super easy in CSS. You're using them right now!</p>
		<h3>Regular HTML Selectors</h3>
		<p>If you don't bother with a class or ID, an HTML element just gets
		   the regular CSS styling for that element—or the default styling if you
		   don't specify any particular styling on the stylesheet.
		</p>
	</body>
</html>
```

*stylesheet.css*

```css
/*Add your CSS below!*/
#intro {
    color: #B83C3A;
}

.standout {
    color: #F7AC5F;
    font-family: Verdana;
}
```

*Shown:*

![Screen Shot 2016-09-23 at 11.09.28 PM](/img/in-post/Screen Shot 2016-09-23 at 11.09.28 PM.png)



## 4 Pseudo-Class Selectors

A **pseudo-class selector** is a way of accessing HTML items that aren't part of the document tree.

Using **pseudo selectors**, you can control the appearance of **unvisited** and **visited links**—even links the user is **hovering over** but hasn't clicked!

The CSS syntax for pseudo selectors is:

```css
selector:pseudo-class_selector {
    property: value;
}
```

**Example:**

.css

```css
a:hover {
	color: #cc0000;
	font-weight: bold;
	text-decoration: none;
}
```

shown: (when you **hover your mouse over** the link)

![Screen Shot 2016-09-23 at 11.36.19 PM](/img/in-post/Screen Shot 2016-09-23 at 11.36.19 PM.png)

#### 4.1 Links

There are a number of useful pseudo-class selectors for links, including:

`a:link`: An unvisited link.
`a:visited`: A visited link.
`a:hover`: A link you're hovering your mouse over.

```css
a:link {
    text-decoration: none;
    color: #008B45;
}

a:hover {
    color: #00FF00;
}

a:visited {
    color: #EE9A00;
}
```

#### 4.2 Child

Another useful pseudo-class selector is `first-child`.

It's used to apply styling to only the elements that are the **first children** of their parents.

```css
p:first-child {
    color: red;
}
```

Make all paragraphs that are the first children of their parent elements red.



Also, we have **Nth child**: select *any* child of an element after the first child with the pseudo-class selector `nth-child`.

```css
p:nth-child(2) {
    color: red;
}
```



##### Example:

html

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title></title>
	</head>
	<body>
		<div>
			<p>I'm the first child!</p>
			<p>We're not.</p>
			<p>We're not.</p>
			<p>We're not.</p>
			<p>We're not.</p>
			<p>We're not.</p>
			<p>We're not.</p>			
		</div>
	</body>
</html>
```

css

```css
/*Add your CSS below!*/
p:first-child {
    font-family: cursive;
}

p:nth-child(2) {
    font-family: Tahoma;
}

p:nth-child(3) {
    color: #CC0000;
}

p:nth-child(4) {
    background-color: #00FF00;
}

p:nth-child(5) {
    font-size: 22px;
}
```

shown:

![Screen Shot 2016-09-23 at 11.51.42 PM](/img/in-post/Screen Shot 2016-09-23 at 11.51.42 PM.png)





**Also**, we can use a `Parent :nth-child ` (remember to leave a space inside) to indicate the child.

* If you don't have a space it means "find the `body` tag that is an nth-child"

* If you have a space it means "find the nth-child of the `body` tag".



*index.html*

```html
/*Add your CSS below!*/
.fancy {
    font-family: cursive;
    color: violet;
}

#serious {
    font-family: Courier;
    color: #8C8C8C;
}

body :nth-child(4) {
    font-size: 26px;
}
```

*stylesheet.css*

```css
/*Add your CSS below!*/
.fancy {
    font-family: cursive;
    color: violet;
}

#serious {
    font-family: Courier;
    color: #8C8C8C;
}

body :nth-child(4) {
    font-size: 26px;
}
```

*shown:*

![Screen Shot 2016-09-24 at 12.52.36 AM](/img/in-post/Screen Shot 2016-09-24 at 12.52.36 AM.png)





> **Notes taking from** 
> *www.codecademy.com*