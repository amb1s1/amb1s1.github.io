---
layout: post
title: '642-832 TSHOOT Test Tips - Layer 3 EIGRP issues '
date: '2011-05-04T20:03:00-04:00'
tags:
- tshoot
- topology
- tshoot test
- cisco
- CCNP
- ccnp test
- cisco test
- lab
- eigrp
- routing
- eigrp routing
- network
- lab
- tutorial
tumblr_url: http://gomezd.com/post/5203197381/layer3eigrpissues
---
LAYER 3 EIGRP Issues

Access list issues blocking protocol 88 – sh access-list


Misconfiguration of the network and neighbor statements – One side has a network statement and the other neighbor – sh ip route eigrp – sh run | section eigrp


Device in different subnet – sh ip int brief


Different ASN (Autonomous system Number) - sh ip eigrp interface


Authentication problem – sh run | section eigrp *tips even if you see that the password is the same, does not mean it is the same because one of the password can have a space on the password, but you won’t see it. If you see authentication problem on the debug (debug eigrp packets) you have to remove and add the password – really tricky right.


Different K values (metric weights)


Redistribution issues –  Redistribution into EIGRP does not have a default value – We need to add the default value or add the metrics. 


Example: redistribute rip metric 1 1 1 1 1

 
Things to know about EIGRP
Type:  Distance Vector
Algorithm: Dual
AD (Admin Distance): 90/170(External)/5 (summary)
Standard: Cisco proprietary
Protocol: IP/88
Authentication: MD5
Multicast: 224.0.0.10
EIGRP is not as big as Layer 2 issues. Remember we can have tons of problems, but I’m trying to narrow the issues with the most common one.
