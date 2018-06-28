---
layout: post
title: Redundancy Protocols - HSRP, VRRP and GLBP
date: '2011-07-17T01:54:00-04:00'
tags:
- hsrp
- vrrp
- glbp
- tshoot
- ccnp
- cisco
- cisco test
- redundancy protocol
- routing
- router
- switch
tumblr_url: http://gomezd.com/post/7715028398/redundancy-protocols-hsrp-vrrp-and-glbp
---
 Issues with Redundancy Protocols
Technologies:
HSRP:
Hot Standby Router Protocol - Created by Cisco
VRRP:
Virtual Router Redundancy Protocol - Created by IETF - Standard work with multiple vendors
GLBP:
Created by Cisco
Issues:
1. Client using the wrong gateway ip address - ipconfig for pc and ifconfig for mac
2. Wrong device acting as the active device - sh standby brief - The device that we want to be active has to have a higher priority number.
3. Missmatch authentication - sh run [interface]
 NOTE: Make sure that if a key-chain is on the interface, that the key-chain was created on the global config.
4. The Active device doesn’t gain the Active after reboots - sh standby brief
5. Wrong group number - sh standby brief
Good Show command to know:
show standby brief - harp 
show glbp brief - glbp
 show vrrp brief - vrrp
show standby [interface] - hsrp
show glbp [interface] - glbp
show vrrp [interface] - vrrp
Debug standby terse - hsrp
Debug glbp terse - glbp
Debug vrrp event - vrrp
sh run interface [interface]
note: This is only redundancy protocol troubleshooting. You still need to know the other technologies to be able to fix any issues with redundancy protocol. Example, if layer 1 is not working HSRP, VRRP or GLBP are not going to work.
