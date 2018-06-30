---
layout: post
title: Python Script for pulling cisco devices running config
date: '2013-05-21T17:51:00-04:00'
tags:
- ccna
- CCNP
- ccnp test
- python
- cisco
- cisco network
tumblr_url: http://gomezd.com/post/51017882453/python-script-for-pulling-cisco-devices-running
---
OK, long time ago that I had not post anything on my blog, so I will start posting more of what I’m doing now. I started to learn how to use python to create report or to grab information from devices(Not just cisco). My manager asked to create script to grab a group of switches running config and to save it on an spreadsheet. We have a lot of branches and each branches had two switches, so what I did was to have each branch on their own tab and in this tab the two switches will have their configs in two columns. So branch1 will be in tab named branch one and switch 1 config will be on tab branch1 on column A and Switch2 will be in branch1 column B. This was show to our client and they love it(Business side love spreadsheets). 
I will post the script here, but before I do this I want to be clear. I’m not a pro in programming, I just have 6 months learning how to program. If you decide to use it, please use it at your own risk. Please make sure to check everything you dont want me to put a backdoor on your network, lol. 

#### Here is my code:
{% gist 5d29b155acd58f2874f2 %}


The format on my blog messed around with the script. Python is very tricky about space, so I uploaded my code to github with the rest of the files for this script to work. 
Here is the link for my github:

<https://github.com/amb1s1/config_pull>
