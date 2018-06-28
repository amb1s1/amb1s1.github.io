---
layout: post
title: '642-832 TSHOOT Test Tips - Layer 3 OSPF Issues '
date: '2011-05-16T16:17:00-04:00'
tags:
- ospf
- tshoot
- ccnp
- ccnp test
- cisco
- cisco switch
- cisco network
- cisco test
- network
- tutorial
- tshoot test
tumblr_url: http://gomezd.com/post/5552393737/ospf-issues
---
                                            OSPF Issues
Access-list blocking protocol 89 – sh access-list
Neighbor statement that configured for Non-Broadcast Network - sh ip ospf [interface interface id]
Area 0 not configure on a multiple OSPF Network - sh ip ospf database
Areas not physically or virtually connect to Area 0 (Every area needs to connect to area 0 either physically or virtually connect) - sh ip ospf virtual-link
Missing the Subnet keyword when doing redistribution ex. redistribute eigrp 10 subnets - sh run | sec ospf


           Mismatch configurations - The following must match between the OSPF neighbors to have OSPF adjacency
Subnet
Area
Network Type
Hello/Dead Timers
MTU
Stub Flag
Authentications
The above issued can be fiund with the following command - Sh ip ospf [interface interface id]Sh CommandsSh ip routeSh ip ospf neighborSh ip ospf [interface interface id]Sh ip ospf virtual-link
Debug commandDebug ip ospf packet
 
