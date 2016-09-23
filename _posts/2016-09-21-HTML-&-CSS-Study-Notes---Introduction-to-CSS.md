---
layout:     post
title:      "HTML & CSS Study Notes - Introduction to CSS"
subtitle:   ""
date:       2016-09-21
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - HTML
    - CSS
    - HTML & CSS Study Notes
---



# Unit 4 Introduction to CSS

* HTML file in index.html
* The stylesheet.css tab contains all the CSS styling information: where HTML elements should go, what color they should be, how big they should be, and more.



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

![Screen Shot 2016-09-21 at 11.03.48 PM](/img/in-post/Screen Shot 2016-09-21 at 11.03.48 PM.png)



## 1 What CSS is

CSS (which stands for **Cascading Style Sheets**) is a language used to describe the appearance and formatting of your HTML.

A **style sheet** is a file that describes how an HTML file should look.

We say these style sheets are **cascading** because the sheets can apply formatting when more than one style applies. For instance, if you say all paragraphs should have blue font, but you specifically single out one paragraph to have red font, CSS can do that!



*index.html*

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>Fancy Fonts</title>
	</head>
	<body>
		<p>I'm a paragraph written in red font, but one of my words is <span>blue</span>!</p>
	</body>
</html>
```

*stylesheet.css*

```css
p {
	color: red;
}

span {
	/*Write your CSS here!*/
	color: blue;
	
}
```

 ![Screen Shot 2016-09-21 at 11.08.20 PM](/img/in-post/Screen Shot 2016-09-21 at 11.08.20 PM.png)

### 1.1 Why separate form from function?

There are two main reasons for separating your form/formatting (CSS) from your functional content/structure (HTML):

1. You can apply the same formatting to several HTML elements without rewriting code (e.g. `style="color:red"`:) over and over
2. You can apply similar appearance and formatting to several HTML pages from a single CSS file



### 1.2 Two ways to put CSS

We previously showed you how to do inline styling with HTML, like so:

`<p style="color:red">Red font!</p>`

With a single CSS file, you only have to make the change in one place!



There are two ways to put CSS in one place.:

This **first** is to put your CSS between` <style></style>` tags, right in the same file as your HTML. These `<style>` tags go inside the `<head></head>` of your webpage:

```html
<!DOCTYPE html>
<html>
	<head>
		<style>
			p {
				color: purple;
			}
		</style>
		<title>Result</title>
	</head>
	<body>
		<p>Check it out! I'm purple!</p>
	</body>
</html>
```

 ![Screen Shot 2016-09-21 at 11.16.28 PM](/img/in-post/Screen Shot 2016-09-21 at 11.16.28 PM.png)



The **second** is to write your CSS in a totally separate file.

You do this by putting a `<link>` tag between the `<head>...</head>` tags of your HTML page. Your `<link>` tag needs three attributes:

1. A` type` attribute that should always be equal to `"text/css"`
2. A` rel `attribute that should always be equal to `"stylesheet"`
3. A `href` attribute that should point to the web address of your CSS file



*index.html*

```html
<!DOCTYPE html>
<html>
	<head>
	    <link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>Result</title>
	</head>
	<body>
		<p>I want to be SIZE 44 font!</p>
	</body>
</html>
```

*stylesheet.css*

```css
p {
	font-size: 44px;
}
```

 ### 1.3 Self-closing tags

Self-closing tags:

 use a single set of `<>`s to be the opening and closing tags. Like:

`<link type="text/css" rel="stylesheet" href="CSS file address"/>`

`<img src="web address"/>`



## 2 CSS Syntax

The general format looks like this:

```css
selector {
    property: value;
}
```

A **selector** can be any HTML element, such as `<p>`, `<img>`, or `<table>`. You just take off the <>s.

A **property** is an aspect of a selector. For instance, you can change the `font-family`, `color`, and `font-size` of the text on your web pages (in addition to many more).

A **value** is a possible setting for a property. `color` can be red, blue, black, or almost any color; `font-family` can be a whole bunch of different fonts; and so on.

You need to end each property-value with a semi-colon (`;`). 

### 2.1 One selector, many properties

```css
p {
    font-family: Arial;
    color: blue;
    font-size: 24px;
}
```

Remember: end each property-value pair with a semicolon!

**Please note**: If you have adjusted your browser's zoom, tests involving font-size and height will not work correctly. To remedy this, please type Command+0 or Ctrl+0 to reset your view.



### 2.2 Many selectors, many properties Example

*index.html*

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>I Know Kung Fu (er, CSS)</title>
	</head>
	<body>
		<div>
			<h3>What's CSS for?</h3>
			<p>CSS is for styling HTML pages!</p>
			<h3>Why use it?</h3>
			<p>It makes webpages look <span>really rad</span>.</p>
			<h3>What do I think of it?</h3>
			<p>It's awesome!</p>
		</div>
	</body>
</html>
```

*stylesheet.css*

```css
/*You can do this! Write your CSS below.*/
h3 {
    color: red;
}

p {
    font-family: Courier;
}

span {
    background-color: yellow;
}
```

*Shown*

![Screen Shot 2016-09-22 at 1.50.57 PM](/img/in-post/Screen Shot 2016-09-22 at 1.50.57 PM.png)

**Notice:**

it's important to remember to put a semicolon (`;`) at the end of each line.



### 2.3 Color commentary

 It's also a good idea to write **comments** as you go along. 

HTML comments look like this:

`<!--I'm a comment!-->`

CSS comments, on the other hand, look like this:

`/*I'm a comment!*/`



## 3 More Details

* Hexadecimal counting is **base-16**. Each digit can be the numbers 0 through 9 **or the letters a through f**!

  eg. `color: #8B1C62;`

* Search for "hex color palette" or "hex color picker" with your favorite web browser to find a bunch of options!

* Hex values always start with a pound sign (`#`), are up to six "digits" long, and are **case-insensitive**: that is, they don't care about capitalization. `#FFC125` and `#ffc125` are the same color.

* **px (for "pixels")**; A pixel is a dot on your computer screen.

  * A pixel is a dot on your computer screen.
  * The `font-size` unit **em** is a **relative measure**: one em is equal to the default font size on whatever screen the user is using.
  * * That makes it great for smartphone screens
  * Don't confuse these with the` <em></em>` tags we use for emphasis!

  ```html
  <!DOCTYPE html>
  <html>
  	<head>
  		<title>Result</title>
  	</head>
  	<body>
  		<p style="font-size: 1em">One em!</p>
  		<p style="font-size: 0.5em">Half an em!</p>
  		<p style="font-size: 2em">TWO EM!</p>
  	</body>
  </html>
  ```

* Most computers will understand popular fonts like Verdana, Courier, and Garamond, but each individual computer has different fonts installed on it.

* CSS has some built-in defaults meant to ensure your users see what you intend. They are:

  1. serif**: A font with little decorative bits on the ends of the strokes that make up letters. Do a search on "serif" to see what we mean.**
  2. sans-serif**: A plain-looking font, like this one. It doesn't have the little doohickies on the ends of letters like a serif font does.**
  3. cursive**: A scripty font! It looks like cursive writing. 

  ​

  eg. serif , sans-serif , cursive

  ![Screen Shot 2016-09-22 at 2.30.38 PM](/img/in-post/Screen Shot 2016-09-22 at 2.30.38 PM.png)

* You don't have to jump straight to a default value like `cursive` or `sans-serif`: you can tell CSS to try several, going from one to the next if the one you want isn't available.

  For example:

  ```css
  p {
      font-family: Tahoma, Verdana, sans-serif;
  }
  ```

  > CSS will first try to apply Tahoma to your paragraphs. If the user's computer doesn't have that font, it will try Verdana next, and if that doesn't work, it will show a default sans-serif font.



### Review:

We've covered:

* What CSS is
* Why we separate form from function
* CSS syntax, including (multiple) selectors, (multiple) property-value pairs, and comments
* Details of how colors, font sizes, and font families work



## 4 Selecting HTML Elements

### 4.1 Background color, height, and width

Use `<div>` to build your own blocks.

There are three properties you'll need to set values for:

1. `background-color`, which you set to a color or hex value
2. `height`, which you set to a value in pixels
3. `width`, which is also measured in pixels



*index.html*

```html
<!DOCTYPE html>
<html>
	<head>
	<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>Result</title>
	</head>
	<body>
		<div></div>
	</body>
</html>
```

*stylesheet.css*

```css
/*Add your CSS below!*/

div {
    background-color: #cc0000;
    height: 100px;
    width: 100px;
}
```

 ![Screen Shot 2016-09-22 at 4.01.18 PM](/img/in-post/Screen Shot 2016-09-22 at 4.01.18 PM.png)

### 4.2 Bordering on insanity

Many HTML elements support the `border` property. This can be especially useful with tables.

```css
td {
    height: 50px;
    border: 1px dashed blue;
}

table {
    border: 1px solid black;
}
```

 ![Screen Shot 2016-09-22 at 4.07.37 PM](/img/in-post/Screen Shot 2016-09-22 at 4.07.37 PM.png)

### 4.3 Links and text decoration

Links also have a property, `text-decoration`, that you can change to give your links a little more custom flair.

*index.html*

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>Result</title>
	</head>
	<body>
		<p>The below link goes to Google!</p>
		<a href="http://www.google.com/">Google</a>
	</body>
</html>
```

*stylesheet.css*

```css
/*Add your CSS below!*/
a {
    color: #cc0000;
    text-decoration: none; /*No blue and underline*/
}
```

![Screen Shot 2016-09-22 at 4.14.06 PM](/img/in-post/Screen Shot 2016-09-22 at 4.14.06 PM.png)

## 5 CSS: An Overview

*index.html*

```html
<!DOCTYPE html>
<html>
	<head>
	    <link type="text/css" rel="stylesheet" href="stylesheet.css" />
		<title>Result</title>
	</head>
	<body>
	    <h1>This is a title</h1>
	    <p>This is a paragraph</p>
	    <img src="http://bit.ly/NnVbxt">
     	<p></p>
	    <a href="www.baidu.com">Link</a>
	</body>
</html>
```

*stylesheet.css*

```css
h1 {
    font-family: Verdana, sans-serif;
    color: #576D94;
}

p {
    font-family: Garamond, serif;
    font-size: 18px;
    color: #4A4943;
}

img {
    border: 1px solid #4682b4;
    height: 100px;
    width: 300px;
}

a {
    text-decoration: none;
    color: #cc0000;
}
```

*shown:*

![Screen Shot 2016-09-22 at 10.51.51 PM](/img/in-post/Screen Shot 2016-09-22 at 10.51.51 PM.png)





> **Notes taking from** 
> *www.codecademy.com*