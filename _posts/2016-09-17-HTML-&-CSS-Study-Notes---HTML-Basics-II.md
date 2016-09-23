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



**Result shown below：**  
<img src="/img/in-post/Screen Shot 2016-09-17 at 6.17.38 PM.png" width="350"/>



## 2.3 Styling and font

HTML is the skeleton of the webpage, and CSS lets you give the skeleton some skin and makeup.

It is possible to do some **inline CSS**. This simply means we can do some styling in our HTML file without worrying about a separate CSS file.

### **Making comments**.

Before we dive into fonts, it's important to learn about making comments. 

``` <!-- This is an example of a comment! --> ```



Also, We can give tags more instructions by including **attributes** in the opening tag.  For example, you saw this with`src` in `<img>` and `href` in `<a>`.

### **Font Size**

`<p style="font-size: 12px"> `  ## px is pixels.

For example:

```
<!DOCTYPE html>
<html>
	<head>
		<title>First font size change</title>
	</head>
	<body>
		<p style="font-size: 10px"> Some text for you to make tiny! </p>
		<p style="font-size: 20px"> Some text for you to make normal size!</p>
		<p style="font-size: 40px"> Some text for you to make super big!</p>
	</body>
</html>
```

### Font color

What is awesome about the**style** attribute is that we use it a lot! And we can use it with many different tags, not just `<p>`. Let's now change the colors of our text in a heading.



To change the color of text, simply add the style attribute in the opening tag:

`<h2 style="color:red">`

if you want to change the color *and* the size of the text:

`<h2 style="color: green; font-size:12px">`

**Notice: A full list of available colors can be found [here.](http://www.w3.org/TR/css3-color/#svg-color)**



Example:

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Changing the colors!</title>
	</head>
	<body>
		<h1 style="color: green; font-size: 12px">Big Heading</h1>
			<p style="color: violet">A giant bear and a little duck were friends.</p>
			<p style="color: red; font-size: 10px">But the bear got hungry and ate the duck.</p>
	</body>
</html>
```



### Font family

`<h1 style="font-family: Arial">Title</h1>`

**Notice: [Here's a list](http://www.w3.org/TR/CSS21/fonts.html#generic-font-families) of available fonts.**

```html
    <!DOCTYPE html>
<html>
	<head>
		<title>Loving the font changes</title>
	</head>
	<body>
		<h1 style="font-family: Arial">Big title</h1>
		 <ol>
		 	<li style="font-family: Arial; font-size: 16px">This item is big Arial.</li>
		 	<li style="font-family: Verdana; font-size: 12px">This item is medium Verdana.</li>
		 	<li style="font-family: Impact; font-size: 10px">This item is small Impact.</li>
		 </ol>
	</body>
</html>
```



### Recap

Use the style attribute for paragraphs, headings, and even links.

`<p style = "font-size:14px; color: orange; font-family: Bodoni">`

More specific example:

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Putting it all together</title>
	</head>
	<body>
		<p style="font-size: 20px; color: blue; font-family: Arial">A truly spectacular paragraph!</p>
	</body>
</html>
```



### Background color

We can use the `style` attribute again, and set it equal to`"background-color: red"` (or whatever color you want).

```html
<p style="background-color: red;">Hello!</p>
```

Example:

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Sexy background color!</title>
	</head>
	<body style="background-color: brown">
		<h3>Favorite Football Teams</h3>
			<ol style="background-color: yellow">
				<li>The Hawthorn Football Club</li>	
				<li>San Franscisco 49ers</li>
				<li>Barcelona FC</li>
			</ol>			
	</body>
</html>
```

Results:

![Screen Shot 2016-09-18 at 5.09.19 PM](/img/in-post/Screen Shot 2016-09-18 at 5.09.19 PM.png)



### Aligning the text

we again use the **style** attribute. And then we use "text-align:left" (or right, or center) to determine the location of the text.

```html
<h1 style="text-align:center">
```

Example:

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Sexy background color!</title>
	</head>
	<body>
		<h3 style="text-align:center">Favorite Football Teams</h3>
			<ol>
				<li style="text-align:left">The Hawthorn Football Club</li>	
				<li style="text-align:center">San Franscisco 49ers</li>
				<li style="text-align:right">Barcelona FC</li>
			</ol>			
	</body>
</html>
```

Result: ![Screen Shot 2016-09-18 at 5.13.19 PM](/img/in-post/Screen Shot 2016-09-18 at 5.13.19 PM.png)



### Strong words!

 if we want to make them **bold**: Surround those words with opening tag `<strong>` and closing tag `</strong>`.

Example:

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Viva La Revolution!</title>
	</head>
	<body>
		<p>Do you hear the people <strong>sing</strong>?</p>
		<p>No I don't. I'm <strong>too</strong> busy eating cake.</p>
	</body>
</html>
```

Result:

 ![Screen Shot 2016-09-18 at 5.16.35 PM](/img/in-post/Screen Shot 2016-09-18 at 5.16.35 PM.png)



### Emphasize words!

Aside from bolding words, we often want to *italicize* words for**em**phasis. (Hint, hint.):

Surround the word or words with the opening tag `<em>` and closing tag `</em>`.

Example:

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Some nice practice</title>
	</head>
	<body>
		<p>Hey, don't say <em>that</em>!</p>
		<p>I am <em>so</em> tired.</p>
	</body>
</html>
```

Result: ![Screen Shot 2016-09-18 at 5.19.59 PM](/img/in-post/Screen Shot 2016-09-18 at 5.19.59 PM.png)

## Summary

This has been an incredibly busy lesson, and you've covered a lot. Congratulations! We have learned how to:

1. Make ordered and unordered lists
2. Change the color, size and type of font
3. Add comments to our HTML file
4. Change the page's background color
5. Align text
6. Bold and italicize text







>**Notes taking from** 
>*www.codecademy.com*

