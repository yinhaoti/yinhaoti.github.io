---
layout:     post
title:      "Study Notes - How the Web works?"
subtitle:   ""
date:       2016-09-23
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - Study Notes
---

### Clients and servers

Computers connected to the Web are called clients and servers.

![client_server](https://mdn.mozillademos.org/files/8973/Client-server.jpg)

Client: Computer connected to WIFI, Web-accessing app (Chrome)

Servers: 	Computers that store webpages





Let's imagine that the Web is a road. On one end of the road is the client, which is like your house. On the other end of the road is the server, which is a shop you want to buy something from.

In addition:

* **TCP/IP**: Transmission Control Protocol and Internet Protocol are communication protocols that define how data should travel across the Web.  In our example, this is like a car or a bike (or your own two feet).
* **DNS**: Domain Name System Servers are like an address book for websites.
* **HTTP**: Hypertext Transfer Protocol is an application protocol that defines a language for clients and servers to speak to each other. This is like the language you use to order your goods.
* **Component files**: A website is made up of many different files, which are like the different parts of the goods you buy from the shop. These files come in two main types:
  * **Code files**: Websites are built primarily from HTML, CSS, and JavaScript, though you'll meet other technologies a bit later.
  * **Assets**: This is a collective name for all the other stuff that makes up a website, such as images, music, video, Word documents, and PDFs.



###  The process:

1. Browser goes the DNS server and find the real address of the server
2. Browser sends a HTTP request message to ask a copy of the website to the client.
3. All data between the client and server is sent across internet connection using TCP/IP.
4. After server approves client's request, the server send an acception message, and start to send website files - small chunks called data packets.
5. Browser assembles the small chunks and display.



### DNS explained:

* Real web address is IP like  63.245.217.105.
* Domain Name Servers are special server that match a **IP address** to a web address(`www.baidu.com`)

### Packets explained:

we used the term "packets" to describe the format in which the data is sent from server to client. 

* data is sent as thousands of small chunks, so many users can download the same website at the same time.
* If web sites were sent as single big chunks, only one user could download one at a time.

> The notes and pictures token from:
>
> https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works