---
layout:     post
title:      "HTML & CSS Study Notes - HTML Basics II"
subtitle:   "Using list and styling"
date:       2016-09-17
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - HTML
    - CSS
    - HTML & CSS Study Notes
---

## **UNIT 2: **HTML STRUCTURE: USING LISTS

In this course, we'll take it to the next level:

* Making ordered and unordered lists
* Changing font size, color and type
* Changing the background color
* Aligning the text



## 2.1 Indentation is your friend

 **indentation**—that is, the amount each line is spaced in from the margin.

* helps make your code more readable!

```html
<!DOCTYPE html>
<html>
	<head>
		<title></title>
	</head>
	<body>
	</body>
</html>
```

## 2.2 Ordered lists & Unordered lists

An **ordered list** is simply a list that is numbered, like the one below.

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Ordered Lists</title>
	</head>
	<body>
		<h1>List of my favorite things</h1>
		<ol> ## ordered list, blow is every element inside list
			<li>Raindrops on roses</li>
			<li>Whiskers on kittens</li>
			<li>Bright copper kettles</li>
			<li>Warm woolen mittens</li>
		</ol>
	</body>
</html>
```

An **unordered list** is made of bullet points:

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Unordered Lists</title>
	</head>
	<body>
	    <h1>Some random thoughts</h1>
	    <p>What I want to do</p>
	    <ul> ## unordered lists
	        <li>run</li>
	        <li>study</li>
	        <li>improve</li>
	        <li>happy</li>
	    </ul>
	</body>
</html>
```

Also, we can **have lists inside a list - Nested**

**Notice:** When you nest tags, the last tag you open is the first one you close.

```html
<ul><li>Tacos!</li></ul>
```

**Example:**

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Nested lists</title>
	</head>
	<body>
		<ol>
			<li>Dad's interests
				<ul>
					<li>football</li>
					<li>knitting</li>
				</ul>
			</li>
			<li>Mom's interests
				<ul>
					<li>hating football</li>
					<li>skydiving</li>
				</ul>
			</li>
		</ol>
		<ul>
		    <li>Favorite Boys</li>
		        <ol>
		            <li>a</li>
		            <li>b</li>
		            <li>c</li>
		        </ol>
		    <li>Favorite Girls</li>
		        <ol>
		            <li>d</li>
		            <li>e</li>
		            <li>f</li>
		        </ol>
		</ul>
	</body>
</html>
```



**显示结果如下：**  ![Screen Shot 2016-09-17 at 6.17.38 PM](/img/in-post/Screen Shot 2016-09-17 at 6.17.38 PM.png)

