---
layout:     post
title:      "HTML & CSS Study Notes - HTML Basics"
subtitle:   ""
date:       2016-09-17
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - HTML
    - CSS
    - HTML & CSS Study Notes
---

## UNIT 1: INTRODUCTION TO HTML

* HTML stands for **HyperText Markup Language**, **Hypertext** means "text with links in it.
* A **markup language** is a programming language used to make text do more than just sit on a page: it can turn text into images, links, tables, lists, and much more.
* CSS—**Cascading Style Sheets**. Think of it like skin and makeup that covers the bones of HTML

### 1.1 Basic Format

```html
<!DOCTYPE html> 
# Always put on the first line. This tells the browser what language it's reading (in this case, HTML).
<html> 
# Start 
Any text you like
<strong>Feel free to change this text!!!.</strong> 
# made our text bold!
</html> 
# End

```

### 1.2 Basic terminology

1. Things inside `<>`s are called **tags**.

2. Tags come in pairs: openning tag and a closing tag

   eg.  ``` <html>```   ``` </html>```

3. tags like parenthese: open one then you should close it

4. Tags also nest

    eg. ```<first tag><second tag>Some text!</second tag></first tag>```

### 1.3 Made Paragraphs

* an HTML file has both a head and a body
* Head - put information about your HTML file, like its title
* Body - put your content, such as text, images, and links. The content in the body is what will be visible on the actual page.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Webpage</title>
  </head>
  
  <body>
    <p>First paragraph</p>
    <p>Second paragraph</p>
  </body>
</html>

```

### 1.4 Body Elements

Inside the Body, HTML has headings. 

There are six heading sizes:

```
<h1> - The CEO
<h2> - VP
<h3> - Director
<h4> - Middle management
<h5> - Lowly assistant
<h6> - Gets coffe for everyone
```

For example:

```html
<!DOCTYPE html>
<html>

	<head>
		<title>
			Headings & Paragraphs
		</title>
		
	</head>
	<body>
		
		<h1>
		This is heading tags
		</h1>
		<p>
		This is the paragraph 1
		</p>
		<p>
		This is the paragraph 2
		</p>
	</body>
</html>
```

-----

Also we have **hyperlinks** to send user to another part of your website.

```<a href="https://www.codecademy.com">My Favorite Site!</a>```

Then we can **Add images**:

```html
<img src="url"/>
```

And add **link to images**:

​	Placing one HTML tag inside of another is called **nesting**.

```html
	<a href="http://yinhaoti.github.io">         <img src="https://s3.amazonaws.com/codecademy-blog/assets/f3a16fb6.jpg" />
	</a>
```

Example:

```html
<!DOCTYPE html>
<html>
	<head>
		<title>hey</title>
	</head>
	<body>
     ## A hyperlink
    <a href="https://www.codecademy.com">My Favorite Site!</a>
     ## An image
	<img src="https://s3.amazonaws.com/codecademy-blog/assets/f3a16fb6.jpg" />
     ## An image with link
	<a href="http://yinhaoti.github.io">         <img src="https://s3.amazonaws.com/codecademy-blog/assets/f3a16fb6.jpg" />
	</a>
	</body>
</html>
```



### 2.1 Build Your Own Webpage

Example in the **index.html** file

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Result</title>
	</head>
	<body><h1>YEAH SANDWICHES</h1>
	<img src="http://bit.ly/RhrMEn" />
		<p>I like eggs.</p>
		<p>And ham!</p>
		<p>But mostly sandwiches.</p>
      <a href="website URL">text</a>
	</body>
</html>
```



An HTML page is sort of like a house, an HTML page needs a frame:

 In this case, your frame is made of``` <!DOCTYPE>```, ```<html>```, ```<head>``` and  ```<body>``` tags.





**Notes taking from** 

www.codecademy.com

