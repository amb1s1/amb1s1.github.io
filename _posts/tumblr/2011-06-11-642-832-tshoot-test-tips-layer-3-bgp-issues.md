---
layout: post
title: '642-832 TSHOOT Test Tips - Layer 3 BGP Issues '
date: '2011-06-11T00:08:00-04:00'
tags:
- tshoot
- tshoot test
- network
- CCNP
- ccnp test
- cisco
- bgp
tumblr_url: http://gomezd.com/post/6293535665/642-832-tshoot-test-tips-layer-3-bgp-issues
---
                                         BGP ISSUES
Issues Peering your neighbor router
3. Since TTL for EBGP is 1 (IBGP is 255) if you want peer to a router that is not one hop away, you will need to use the Multihop command
2. Access List blocking TCP 179 - sh access-list
3. Routers have to have ip reachability (Rip, EIGRP, Static Route….) if the   router   is not directly connect to be able to establish peering - sh ip route

BGP peers must agree on the following attribute
1. Peer Address
2. Unique RID (Router ID - loop interface)
3. ASN (autonomous system number)

Important command to know
1. show ip bgp neighbors
2. show ip route
3. show ip bgp summary
