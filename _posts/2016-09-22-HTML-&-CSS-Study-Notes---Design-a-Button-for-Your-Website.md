---
layout:     post
title:      "HTML & CSS Study Notes - Design a Button for Your Website"
subtitle:   ""
date:       2016-09-22
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - HTML
    - CSS
    - HTML & CSS Study Notes

---

#### 1 Design a Button for Your Website

we'll need to create our button. We'll do this with <div></div> tags.

#### 2 Shaping your button 

This involves a new property called **border-radius**. This property modifies the corners of HTML objects; it's how you get those cool rounded buttons!

#### 3 Positioning your button

* `margin`: auto; is the CSS you use to tell the browser: "Hey! Make sure to set equal margins on each side of this HTML element." When the margins are equal, the object is centered.
* `text-align`: center; is how you center text elements.

#### 4 Adding the link

you may have noticed that we used <span></span> tags to create a different font color for "Facebook!", like so:

`<a href="https://facebook.com">Friend us on <span>Facebook!</span></a>`



#### 5 Result

`index.html`

```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css"/>
		<title>About Me</title>
	</head>
	<body>
		<img src="https://s3.amazonaws.com/codecademy-blog/assets/46838757.png"/>
		<p>We're Codecademy! We're here to help you learn to code.</p><br/><br/>
		<div>
			<a href="www.baidu.com">button on <span>baidu</span></a>
		</div>
	</body>
</html>
```

`stylesheet.css`

```css
img {
	display: block;
	height: 100px;
	width: 300px;
	margin: auto;
}

p {
	text-align: center;
	font-family: Garamond, serif;
	font-size: 18px;
}

/*Start adding your CSS below!*/
div {
    height: 50px;
    width: 120px;
    border: 2px solid #6495ED;
    background-color: #BCD2EE;
    border-radius: 15px;
    margin: auto;
    text-align: center;
}

a {
    text-decoration: none;
    color: White;
    font-family: Arial;
}

span {
    color: red;
}
```



*Shown:*

![Screen Shot 2016-09-22 at 11.26.06 PM](/img/in-post/Screen Shot 2016-09-22 at 11.26.06 PM.png)









> **Notes taking from** 
> *www.codecademy.com*