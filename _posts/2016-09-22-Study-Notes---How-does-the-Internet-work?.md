---
layout:     post
title:      "Study Notes - How does the Internet work?"
subtitle:   ""
date:       2016-09-22
author:     "Haotian"
header-img: "img/post-bg-2015.jpg"
tags:
    - Study Notes
---



# How does the Internet work?

The **Internet** is the backbone of the Web, the technical infrastructure that makes the Web possible. At its most basic, the Internet is a large network of computers which communicate all together.



>  Internet is a way to connect computers all together and ensure that, whatever happens, they find a way to stay connected.



### A simple network

A router likes a signaler at a railway station, it makes sure that a message sent from a given computer arrives at the right destination computer. 

![router](https://mdn.mozillademos.org/files/8445/internet-schema-3.png" )

 

### A network of networks

A router is like a computer, so we can connet two routers together.

![router to router](https://mdn.mozillademos.org/files/8449/internet-schema-5.png)

* To connect our network to the telephone infrastructure, we need a special piece of equipment called a modem.
* The next step is to send the messages from our network to the network we want to reach. To do that, we will connect our network to an Internet Service Provider (ISP)
* An ISP is a company that manages some special routers that link all together and can also access other ISPs' routers.


![ISP](https://mdn.mozillademos.org/files/8453/internet-schema-7.png)

### Finding computers

Any **computer** linked to a network has a **unique address** to identify it, called an "**IP address**" (where IP stands for Internet Protocol).

`192.168.2.10`

To make things easier, we can alias an IP address with a human readable name called a **domain name**. 



### Internet and the web

As you might notice, when we browse the Web with a Web browser, we usually use the domain name to reach a website.

The Internet is an infrastructure, whereas the Web is a service built on top of the infrastructure.



> The notes and pictures take from below:
>
> https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work

