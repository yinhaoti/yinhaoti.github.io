---
layout:     post
title:      "HTML & CSS Study Notes - CSS Element Positioning"
subtitle:   ""
date:       2016-09-24
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - HTML
    - CSS
    - HTML & CSS Study Notes
---



# 1 The Box Model

As we mentioned, elements populate the page in what's known as the **CSS box model.** Each HTML element is like a tiny box or container that holds the pictures and text you specify.

## **Display** property

We can change all this with the first positioning property we'll learn: the **display** property. We'll learn about four possible values.

**block**: This makes the element a block box. It won't let anything sit next to it on the page! It takes up the full width.

```css
div {
	height: 50px;
	width: 100px;
	border: 2px solid black;
	border-radius: 5px;
	/*Add your CSS here!*/
	display: block;
}
/*  Our <div>s were block elements by default */
```

![Screen Shot 2016-09-24 at 12.11.33 PM](/img/in-post/Screen Shot 2016-09-24 at 12.11.33 PM.png)

**inline-block**: This makes the element a block box, but will allow other elements to sit next to it on the same line.

```css
display: inline-block;
```

![ ![Screen Shot 2016-09-24 at 12.11.33 PM](/Users/haotianyin/Documents/GitHub/yinhaoti.github.io/img/in-post/Screen Shot 2016-09-24 at 12.11.33 PM.png)](/img/in-post/Screen Shot 2016-09-24 at 12.10.11 PM.png)

**inline**: This makes the element sit on the same line as another element, but without formatting it like a block. It only takes up as much width as it needs (not the whole line).

```css
display: inline;
```

![Screen Shot 2016-09-24 at 12.14.14 PM](/img/in-post/Screen Shot 2016-09-24 at 12.14.14 PM.png)

**none**: This makes the element and its content disappear from the page entirely! 

```css
display: none;
```

 ![Screen Shot 2016-09-24 at 12.15.54 PM](/img/in-post/Screen Shot 2016-09-24 at 12.15.54 PM.png)



# 2 Margins, Borders, and Padding

<img src="https://s3.amazonaws.com/codecademy-blog/assets/ae09140c.png"/>

* The **margin** is the space around the element. The larger the margin, the more space between our element and the elements around it. We can adjust the margin to move our HTML elements closer to or farther from each other.

* The **border** is the edge of the element. It's what we've been making visible every time we set the border property.

* The **padding** is the spacing between the content and the border. We can adjust this value with CSS to move the border closer to or farther from the content.

* The **content** is the actual "stuff" in the box. If we're talking about a <p> element, the "stuff" is the text of the paragraph.

* You'll see abbreviations like TM, TB, and TP in the diagram. These stand for "top margin," "top border," and "top padding."

  ​

## 2.1 Margin

Let's start with our margins. Adjusting our margins not only moves our element relative to other elements on the page, but also relative to the "walls" of the HTML document.

```css
margin: auto;
/* automatically put equal left and right margins on our element, centering it on the page.*/
```

![Screen Shot 2016-09-24 at 12.21.31 PM](/img/in-post/Screen Shot 2016-09-24 at 12.21.31 PM.png)



Specify a particular margin:

```css
margin-top: /*some value*/
margin-right: /*some value*/
margin-bottom: /*some value*/
margin-left: /*some-value*/
```

Set an element's margins **all at once**: you just start from the top margin and **go around clockwise** (going from top to right to bottom to left).

```css
margin: 20px 50px 10px 5px;
```

![Screen Shot 2016-09-24 at 12.24.11 PM](/img/in-post/Screen Shot 2016-09-24 at 12.24.11 PM.png)

## 2.2 Borders

```css
	border: 4px solid #FF0000;
```

![Screen Shot 2016-09-24 at 12.26.06 PM](/img/in-post/Screen Shot 2016-09-24 at 12.26.06 PM.png)

## 2.3 Padding

The **padding** is the space between your **border** and your **innermost layer**: the actual content.

Padding can be set in two ways:

* individually

  ```css
  padding-top: /*some value*/
  padding-right: /*some value*/
  padding-bottom: /*some value*/
  padding-left: /*some-value*/
  ```

* all in one declaration

  ```css
  padding: value value value value;
  ```

If you want your padding to be the same for all four sides, you can declare that value only once - `padding: 10px`.

## 2.4 Negative values

You give it a `margin-left` of `20px`, it puts twenty pixels between the left margin of that `<div>` and the side of the screen.

If you want to move an element in the other direction, you can give CSS a negative value: `margin-left: -20px` will move the element twenty pixels to the left.



# 3 Floating

Using **floats** is to tell where the element go on the page.

```css
float: right;
```

 ![Screen Shot 2016-09-24 at 1.35.57 PM](/img/in-post/Screen Shot 2016-09-24 at 1.35.57 PM.png)



**Float for two:**

```css
div {
	height: 300px;
	width: 300px;
	border: 2px solid black;
	border-radius: 5px;
	background-color: #308014;
	/*Add your CSS here!*/
	float: right;
	
}

p {
	font-family: Verdana, sans-serif;
	font-size: 20px;
	width: 280px;
	/*Add your CSS here!*/
	float: left;
	
}
```

![Screen Shot 2016-09-24 at 1.37.56 PM](/img/in-post/Screen Shot 2016-09-24 at 1.37.56 PM.png)





### Clearing elements

`clear` the other elements on the page!

* If you tell an element to `clear: left`, it will immediately move below any floating elements on the left side of the page
* If you tell it to `clear: both`, it will get out of the way of elements floating on the left and right!

```css
element {
    clear: /*right, left, or both*/
}
```

 Example:

```css
#footer {
	height: 50px;
	background-color: #69D2E7;
	/*Add your CSS here!*/
	clear: both

}
```

![Screen Shot 2016-09-24 at 1.46.36 PM](/img/in-post/Screen Shot 2016-09-24 at 1.46.36 PM.png)

# 4 Abosolute, Relative, and Fixed Positioning

If you don't specify an element's positioning type, it defaults to `static`.

This just means "where the element would normally go." If you don't tell an element how to position itself, it just plunks itself down in the document. 

**Notice**: the html files used in those subtitles is:

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>Result</title>
	</head>
	<body>
		<div id="outer"><div id="inner"></div></div>
	</body>
</html>
```



## 4.1 Absolute positioning

 When an element is set to `position: absolute`, it's then positioned in relation to the **first parent element** it has that doesn't have `position: static`. If there's no such element, the element with `position: absolute` gets positioned relative to` <html>`.

To show you how this works, we've set the `#outer` div to have `absolute positioning`. This means that when you position the `#inner` div, it will be relative to` #outer`. (If #outer had the default positioning of `static`, then `#inner` would get positioned relative to the entire HTML document.)

```css
div {
	height: 100px;
	width: 100px;
	border-radius: 5px;
	border: 2px solid black;
}

#inner {
	height: 75px;
	width: 75px;
	background-color: #547980;
	/*Add your CSS here!*/
	position: absolute;
	margin-left: 20px;
	
}

#outer {
	height: 1500px;
	width: 150px;
	background-color: #45ADA8;
	position: absolute;
	margin-left: 100px;
}
```

![Screen Shot 2016-09-24 at 2.24.35 PM](/img/in-post/Screen Shot 2016-09-24 at 2.24.35 PM.png)

Above the inner part is relative to outer part, margin left length is 20px away from outer part border.

## 4.2 Relative positioning

**Relative** positioning is more straightforward: it tells the element to move relative to where it would have landed if it just had the default `static` positioning.

```css
div {
	height: 100px;
	width: 100px;
	border-radius: 5px;
	border: 2px solid black;
}

#inner {
	height: 75px;
	width: 75px;
	background-color: #547980;
	/*Add your CSS here!*/
	position: relative; /*relative to static position*/
	margin-left: 200px; 
	
}

#outer {
	height: 1500px;
	width: 150px;
	background-color: #45ADA8;
	position: absolute;
	margin-left: 100px;
}
```

![Screen Shot 2016-09-24 at 2.35.27 PM](/img/in-post/Screen Shot 2016-09-24 at 2.35.27 PM.png)



## 4.3 Fixed positioning

**fixed** positioning anchors an element to the browser window—you can think of it as **gluing the element to the screen**. If you **scroll up and down**, the fixed element stays put even as other elements scroll past.

```css
position: fixed;
```



# 5 Made your own page

*index.html*

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>Result</title>
	</head>
	<body>
		<div id="header">
			<div id="navbar">
				<ul>
					<li>Home</li>
					<li>About Me</li>
					<li>Plans for World Domination</li>
					<li>Contact</li>
				</ul>
			</div>
			<h2>About Me</h2>
		</div>
		<div id="left">
		<img src="https://s3.amazonaws.com/codecademy-blog/assets/puppy-main_zps26d178c5.jpg"/>
		<p>I am the angriest puppy in the world. This has been scientifically proven in several clinical trials.</p>
		</div>
		<div id="right">
		<table>
			<th colspan="3">My Bros</th>
			<tr>
				<td><img src="https://s3.amazonaws.com/codecademy-blog/assets/puppy-1_zps5666b8e7.jpg"/></td>
				<td><img src="https://s3.amazonaws.com/codecademy-blog/assets/puppy-2_zps1539e6b2.jpg"/></td>
				<td><img src="https://s3.amazonaws.com/codecademy-blog/assets/puppy-3_zps4692eafa.png"/></td>
			</tr>
			<tr>
				<td><img src="https://s3.amazonaws.com/codecademy-blog/assets/puppy-4_zps63ff5aa8.jpg"/></td>
				<td><img src="https://s3.amazonaws.com/codecademy-blog/assets/puppy-5_zps0ee0d2c8.jpg"/></td>
				<td><img src="https://s3.amazonaws.com/codecademy-blog/assets/puppy-6_zpsc4450a60.jpg"/></td>
			</tr>
			<tr>
				<td><img id="bottom_left" src="https://s3.amazonaws.com/codecademy-blog/assets/puppy-7_zps26e8a8d9.jpg"/></td>
				<td><img src="https://s3.amazonaws.com/codecademy-blog/assets/puppy-8_zps9a1469be.jpg"></td>
				<td><img id="bottom_right" src="https://s3.amazonaws.com/codecademy-blog/assets/puppy-9_zps3bab7732.jpg"/></td>
			</tr>
		</table>
		</div>
		<div id="footer">
			<div id="button">
				<p>Send me an <span class="bold">e-mail</span>!</p>
			</div>
		</div>
	</body>
</html>
```

*stylesheet.css*

```css
body {
	background-color: #b7d1c4
}

h2 {
	font-family: Verdana;
	font-weight: bold;
	text-align: center;
	padding-top: 25px;
	padding-bottom: 25px;
	color: #acd1b2;
}

img {
	height: 170px;
	width: 170px;
	box-shadow: rgba(0,0,0,0.2) 10px 10px;

}

#navbar {
	/*Add your CSS here!*/
	position: fixed;
	margin-top: 0px;
	left:50%;
	margin-left:-254px;
}

#header {
	position: relative;
	top: -10px;
	background-color: #3c4543;
	border-top-left-radius: 15px;
	border-top-right-radius: 15px;
}

ul{
	list-style-type: none;
	position: fixed;
	margin: -10px;
}

li {
	/*Add your CSS here!*/
	display: inline;
	padding: 5px;
	border: 2px solid #000000;
	font-family: Futura, Tahoma, sans-serif;
	color: #ffffff;
	border-radius: 5px 5px;
	background-color: #cc0323
}

#left{
	/*Add your CSS here!*/
    float: left;
	width: 45%;
}

p {
	font-family: Tahoma;
	font-size: 1em;
}

#right{
	/*Add your CSS here!*/    
	float: right;
	width: 45%;
	
}

table {
	border: #000000 1px solid;
	background-color: #acd1b2;
	float: right;
	margin-right: 10px;
	border-bottom-right-radius: 15px;
	border-bottom-left-radius: 15px;
}

td {
	height: 75px;
	width: 75px;
}

td img {
	height: 75px;
	width: 75px;
	box-shadow: none;
}

th {
	font-family: Verdana;
	font-size: 1em;
	font-weight: normal;
	color: #3c4543
}

#bottom_left{
	border-bottom-left-radius: 15px;
}

#bottom_right{
	border-bottom-right-radius: 15px;
}

#footer{
	/*Add your CSS here!*/
	clear: both;
	position: relative;
	bottom: -20px;
	border-bottom-left-radius: 15px;
	border-bottom-right-radius: 15px;
	height: 75px;
	background-color: #3c4543;
}

#button{
	border: 2px solid #000000;
	float:left;
	position: relative;
	left: 229px;
	bottom: -20px;
	border-radius: 5px;
	background-color: #cc0323;
	height: 30px;
	width: 150px;
	
}

#button p{
	position: relative;
	bottom: 10px;
	font-size: 0.8em;
	color: #acd1b2;
	text-align: center;
}

.bold{
	font-family: tahoma;
	font-weight: bold;
	font-size: 1.2em;
	font-variant: small-caps;
	color: #ffffff;
}
```







> **Notes taking from** 
> *www.codecademy.com*