---
title: "NET-1111 - Cisco 1 - Intro to Networks"
excerpt: "Collection of things from Hocking College's NET-1111 class" # <br/><img src='/images/500x300.png'>"
collection: portfolio
---

<a id="week_01"></a><br><br>
# Week 1 – Introduction to Networking & Course Setup

**Description:**  
We were introduced to networks and the general devices that make up networks.  We were also introduced to Cisco Packet Tracer.

**Artifacts:**  
- Lab Assignment: Make a simple network with two hosts and a switch.  Ping between the hosts.
<img src='/images/Week_01-NET-1111-Cisco_Packet_Tracer.png'>  

**Reflection:**  
My first impressions of networking come from using modem’s and connecting to local Bulletin Board systems.  I was hooked.  My dad brought home a bunch of old PC's and ARCNet NIC’s from his work.  And I hooked those up using the IPX and TCP/IP protocols.  Also the internet was just emerging via local ISP’s.  I got my first account with a local company named Green Apple in Lancaster, Ohio.  Eventually, I upgraded my ARCNet network to Ethernet.  At 16 I worked at a local computer shop installing and upgrading networks and servers for local businesses and doing support for the local ISP.

And today networking affects us to an even greater degree.  Everything seems to be online.  For example: the brake controller we just bought for our vehicle!  We had to login to an app to configure it.
I think it’s a little overboard to be honest.

I hope to learn how to configure cisco switches and routers.  I’ve used active HP switches before to configure things like VLANs.  I’m familiar with home-based routers like Linksys where you can put tailored versions of linux on them, like DD-WRT or Tomato and configured things like VPNs.  I’ve configured firewalls with PF and PFSense on unix.

**AI Use Note:**  
I haven't used AI yet this course.

<a id="week_02"></a><br><br>
# Week 2 – Networking Components, Types and Connections

**Description:**  
We were tasked to represent our home network in Cisco Packet Tracer.  I couldn't find a smart tv and I suppose there are bluetooth devices, like speakers that aren't being represented.

**Artifacts:** 
<img src='/images/NET-1111/Week_02_NET-1111-Home_Network.png'>  
<img src='/images/NET-1111/Week_02_NET-1111-Home_Network_PING.png'>  

**AI Use Note:**
I haven't used AI.

<a id="week_03"></a><br><br>
# Week 3 – Ethernet Fundamentals, Cabling, and Switching

**Description:**  
In a lab we were tasked to make a network that uses Star Topology and to verify L2/L3 connectivity.  
The prompt for this entry is this:
Polished post: “Star Topology” + screenshots from Lab.
Use what you did in Lab (Day 1) assignment for this entry. Explain what a star topology is, what devices are required, what connections are used, and what you had to configure on the end devices to get them connected.

The star topology is the name of a network topology or network configuration that consists of nodes that are connected to a central location.  Each node is singularly connected with a wire to a central point looking like a spoke connected to a hub like on a wagon-wheel. This hub can be two devices, namely a switch or a hub.  Technically though, the device that is a hub is a relic of technology and no longer in widespread use.  This wagon-wheel type configuration appears to some to look like a star, hence it's name: "Star Topology".  Other topologies exist, like the "Bus Topology" which consist of a single line of nodes, appearing like a bus or a "Ring Topology" which connects nodes in a circle, looking like a ring.  Each network topology has it's own significance within networking techology.  Each node in a "Star Topology" constists of an end-device like a PC, Laptop, Printer, or etc.  Each end-device is assigned a MAC address, or Media Access Control address from it's manufacturer.  This address talks on Level 2 of the network.  Similarly, each device assigned either manually or automatically (with DHCP services) it's own IP Address. This address talks on Level 3 of the network. 

**Artifacts:** 
<img src='/images/NET-1111/Week_02_NET-1111-Home_Network.png'>  
<img src='/images/NET-1111/Week_02_NET-1111-Home_Network_PING.png'>  

**AI Use Note:**
I haven't used AI.
