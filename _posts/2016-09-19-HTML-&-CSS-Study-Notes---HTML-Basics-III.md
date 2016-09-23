---
layout:     post
title:      "HTML & CSS Study Notes - HTML Basics III"
subtitle:   ""
date:       2016-09-19
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - HTML
    - CSS
    - HTML & CSS Study Notes
---

## **UNIT 3: **HTML STRUCTURE: TABLES, DIVS, AND SPANS

In this course, we'll cover some important structural aspects of HTML: `<table>`s, `<div>`s, and `<span>`s!

### 1 What are tables?

We use them to store tabular data so it is easy to read.

There are many tags associated with tables, but it all starts with the `` tag, so let's add that first.

#### Rows of information

>  A table is just a bunch of information arranged in rows and columns.

We use the `<tr>` tag to create a **table row**.

#### A single column

We've added a single `<td>` ("table data") cell to the first row, essentially creating a single column. 

Example:

![Screen Shot 2016-09-18 at 10.00.13 PM](/img/in-post/Screen Shot 2016-09-18 at 10.00.13 PM.png)

Whole Table:

![Screen Shot 2016-09-18 at 10.05.38 PM](/img/in-post/Screen Shot 2016-09-18 at 10.05.38 PM.png)



#### Head of the table

To make our table look a little more like a table, we'll use the `<thead>` and `<tbody>` tags. These go within the <table> tag and stand for table head and table body, respectively.



 **Notice** that we use <th></th> for the table heading cells instead of<td></td>.

```html
<thead>
  <tr>
    <th>
      Name
    </th>
    <th>
      Favorite Color
    </th>
  </tr>
</thead>
```



Example:

```html
<html>
    <head>
        <title>Table Time</title>
    </head>
    
    <body>
        
        <table border="1px">
            <thead>
                <tr>
                    <th>
                    Famous Monster
                    </th>
                    <th>
                    Birth Year
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>King Kong</td>
                    <td>1933</td>     
                </tr>
                
                <tr>
                    <td>Dracula</td>
                    <td>1897</td>
                </tr>
                
                <tr>
                    <td>Bride of Frankenstein</td>
                    <td>1935</td>
                </tr>
            </tbody>
        </table>
        
    </body>

</html>
```



Shown:

![Screen Shot 2016-09-19 at 11.41.53 AM](/img/in-post/Screen Shot 2016-09-19 at 11.41.53 AM.png)

#### Naming your table

We want to add a title row that goes all the way across the top.

To do so, we need to use the colspan attribute for the `<th>` tag. By default, table cells take up 1 column. If we want a table cell to take up the space of 3 columns instead of 1, we can set the `colspan` attribute to 3.

```<th colspan="3">3 columns across!</th>```



#### Style that head!

`<th style="font-size:12px; color:red"></th>`



Example:

```html
<html>
    <head>
        <title>Table Time</title>
    </head>
    
    <body>
        
        <table style="border-collapse:collapse;">
            <thead>
                <tr>
                    <th colspan="2" style="color:red"><em>Famous Monsters</em> by <em>Birth Year</em></th>
                </tr>
                <tr style="border-bottom:1px solid black;">
                    <th style="padding:5px;"><em>Famous Monster</em></th>
                    <th style="padding:5px;border-left:1px solid black;"><em>Birth Year</em></th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td style="padding:5px;">King Kong</td>
                    <td style="padding:5px;border-left:1px solid black;">1933</td>     
                </tr>
                
                <tr>
                    <td style="padding:5px;">Dracula</td>
                    <td style="padding:5px;border-left:1px solid black;">1897</td>
                </tr>
                
                <tr>
                    <td style="padding:5px;">Bride of Frankenstein</td>
                    <td style="padding:5px;border-left:1px solid black;">1944</td>
                </tr>
            </tbody>
        </table>
        
    </body>

</html>
```



Results:

 ![Screen Shot 2016-09-19 at 12.06.31 PM](/img/in-post/Screen Shot 2016-09-19 at 12.06.31 PM.png)



#### Recap

What can you do now?

1. Write an HTML comment
2. Create a list (ordered and unordered)
3. Make text stand out using <em> and <strong>
4. Change the color, size, and alignment of text using the style attribute
5. Create HTML tables



### 2. 'Div'ide and conquer

One of the most versatile structure tags available to you is the `<div>` `</div>` tag. Short for "division," `<div>` allows you to divide your page into containers (that is, different pieces). 



Also, just like with images, you can make `<div>`s clickable by wrapping them in ` <a>` `</a>` tags.



Example:

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Result</title>
	</head>
	<body>
	    <a href="yinhaoti.github.io">
		<div style="width:50px; height:50px; background-color:red"></div>
		<div style="width:50px; height:50px; background-color:blue"></div>
		<div style="width:50px; height:50px; background-color:green"></div>
		<div style="width:50px; height:50px; background-color:yellow"></div>
		</a>
	</body>
</html>
```

Result:

 ![Screen Shot 2016-09-19 at 1.13.16 PM](/img/in-post/Screen Shot 2016-09-19 at 1.13.16 PM.png)





#### Spantastic

``<span>`` allows you to control styling for smaller parts of your page, such as text. For example, if you always want the first word of your paragraphs to be red, you can wrap each first word in `<span>` `</span>` tags and make them red using CSS!



#### Recap

Great work! In addition to what you've already learned, you now know how to:

1. Divide up your webpage for easy styling with `<div>` tags
2. Select pieces of text and change their properties using `<span>` tags

 ![Screen Shot 2016-09-19 at 1.19.48 PM](/img/in-post/Screen Shot 2016-09-19 at 1.19.48 PM.png)



### 3.Clickable Photo Page

You can use a table to create a beautifully formatted grid of photos.

You'll notice we've included an extra file in this project: stylesheet.css. You'll be learning about CSS in the next lesson and project, but we thought you might like a sneak peek here. This file will help format your HTML to keep it looking great.



```html
<!DOCTYPE html>
<html>
	<head>
		<link type="text/css" rel="stylesheet" href="stylesheet.css" />
		<title>My Photo Page</title>
	</head>
	<body>
	    <table>
	        <thead>
	            <th>My Pic Wall</th>
	        </thead>
	        <tbody>
	            <tr>
	                <td>
	                   <a href="http://codecademy.com"> <img src="http://2zpt4dwruy922flhqyznip50.wpengine.netdna-cdn.com/wp-content/uploads/2014/12/lock-and-stock-photos.jpg" /></a>
	                </td> 
	                <td>
	                    <a href="http://codecademy.com"><img src="http://bootstrapbay.com/blog/wp-content/uploads/2014/05/unslpash-desert-road_uvsq5s.png" /></a>
	                    
	                </td>
	                <td>
	                    <a href="http://codecademy.com"><img src="http://static.bigstockphoto.com/images/homepage/2016_bigstock_picks.jpg" /></a>
	                </td>
	            </tr>
	            <tr>
	                <td>
	                <a href="http://codecademy.com"><img src="https://dpcs.ftcdn.net/r/pics/353e487d2ac989a50a65ad3219ed2f56d801c339/all/fader/27870409.jpg" /></a>
	                </td>
	                <td>
	                <a href="http://codecademy.com"><img src="http://img06.deviantart.net/25de/i/2012/134/3/1/037_by_koko_stock-d4zq28i.jpg" /></a>
	                </td>
	                <td>
	                <a href="http://codecademy.com"><img src="http://bootstrapbay.com/blog/wp-content/uploads/2014/05/unslpash-desert-road_uvsq5s.png" /></a>
	                </td>
	            </tr>
	            <tr>
	                <td>
	                <a href="http://codecademy.com"><img src="http://img06.deviantart.net/25de/i/2012/134/3/1/037_by_koko_stock-d4zq28i.jpg" /></a>
	                </td>
	                <td>
	                <a href="http://codecademy.com"><img src="http://img06.deviantart.net/25de/i/2012/134/3/1/037_by_koko_stock-d4zq28i.jpg" /></a>
	                </td>
	                <td>
	                <a href="http://codecademy.com"><img src="http://bootstrapbay.com/blog/wp-content/uploads/2014/05/unslpash-desert-road_uvsq5s.png" /></a>
	                </td>
	            </tr>
	        </tbody>
	    </table>
	
	
	</body>
</html>
```

![Screen Shot 2016-09-21 at 10.52.20 PM](/img/in-post/Screen Shot 2016-09-21 at 10.52.20 PM.png)

> **Notes taking from** 
> *www.codecademy.com*

