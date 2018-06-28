---
layout: post
title: '642-832 TSHOOT test Tips - Layer 2 issues '
date: '2011-05-03T14:27:00-04:00'
tags: []
tumblr_url: http://gomezd.com/post/5165387435/layer2iissues
---
       
 TSHOOT test in general can be   overwhelming, but if you take the  entire test and look at it from one technology at a time, it can be  really easy. I’m going to start to point out issues that we may counter with different technologies base on the TSHOOT blueprint.On my first post I’m going to start with layer 2 issues.
    Layer 2 issues:
Misconfiguration of the trunk encapsulation (Dot1q, ISL) - sh interface trunk
Misconfiguration of the port mode (Trunk and Access) - sh vlan, sh int switchport
Vlan not allowed on the trunk port - sh interface trunk
Adding an Vlan to a switchport and without adding a Vlan is not in the Vlan Datatabse - sh vlan brief 
Duplex and Speed mismatch - sh log and sh interface and the interface that you want to see
VTP Issues 
VLAN Failing to propagate to in the topology - sh vtp status
Wrong VTP Mode - Having a device in transparent mode between a client and a server can cause problem - sh vtp status
Wrong MD5 digest password - Sh vtp passwor4d - sh vtp status *note the MD5 password sometime look the same, but the hash is different (sh vtp status), the way to fix that is by removing the password and apply the password again. 
Dot1Q issue only - Native Vlan Mismatch - sh interface switchport 
    8. Issues with DTP (Dynamic Trunk Protocol) - sh interface switchport
dynamic mode auto + dynamic mode auto = No Trunk
dynamic mode on + dynamic mode Nonegotiate=  No trunking
dynamic mode Auto + dynamic mode desirable= Trunk
dynamic mode on + dynamic mode auto= Trunk
                                Etherchannel Layer 2 Issues:
Misconfiguration between the members
All members has to have identical configurations *tips always configure the etherchannel configuration with the interface range command.
    2. Issues with the negotiation protocols (LACP(open standar) and PAgP(Cisco)
PAgP two modes - Desirable and Auto
LACP two modes - Active and Pasive
On is turning statical the etherchannel on
The etherchannel can’t be mismatch with two type of negotiation protocols
     3. Issues with PAgP Negotiation Protocol
Desirable + Desirable = Etherchannel is going to be Up
Desirable + Auto = Etherchannel is going to be Up
Auto + Auto = Etherchannel is not going to be Up
     4. Issues with LACP Negotiation Protocol
Active + Active = Etherchannel is going to be Up
Active + Passive = Etherchannel is going to be Up
Passive + Passive = Etherchannel is not going to be Up
Command for Etherchannel Troubleshooting:
sh interface trunk
sh etherchannel summary
sh etherchannel port-channel
                                     STP (Spanning Tree Protocol)
High port utilization ( a loop can cause this issue) - sh processes cpu 
BPDU Issues propagating 
Trunk link have to be established on all interfaces participating in the spanning tree sh interface trunk
    2. Misconfiguration of the STP mode PVST, MST and Rapid-PVST - sh spanning-tree vlan vlan#
3. STP not anable on the vlan - sh spanning-tree vlan and the vlan #
                                              Conclusion
It may look big, but with couple of commands you can see a most of the problems.
Next Tutorial is going to be Layer 3 EIGRP Issues. Thanks
