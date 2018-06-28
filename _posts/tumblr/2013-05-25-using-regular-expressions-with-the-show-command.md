---
layout: post
title: Using regular expressions with the ‘Show’ command | CiscoZine
date: '2013-05-25T12:27:00-04:00'
tags:
- CCNA
- CCNP
- network
- network engineer
- cisco
- cisco network
- cisco router
tumblr_url: http://gomezd.com/post/51310610075/using-regular-expressions-with-the-show-command
---
Using regular expressions with the ‘Show’ command | CiscoZineShow command using regular expression
This is an option that I think most of the Engineers rarely use.
Example of when this was use to me:
I needed to confirm that all configuration for a specific vrf were remove. The problem was that the delete vrf was named ssdata and the new vrf was hrssdata. So when I search with a regular pipe:
show run | in ssdata 
I was getting command for hrssdata. I looked online and the solution was using regular expression, so I used the following:
show run | in _ssdata_ 
here is a great link to learn more about regular expressions
Using regular expressions with the ‘Show’ command | CiscoZine: “”
