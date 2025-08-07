---
layout: post
title: OPNSense Follow up 😠
categories: [Networking, Server, OPNSense, PFSense]
---

It's been a few days since I installed OPNSense on a new mini computer that I used as a host for proxmox in my home lab. After having experience with the hardware in deploying my proxmox cluster, I decided to use the same hardware for my firewall. It would have been nice to use PFSense on this new hardware; however, as I mentioned in my previous post, PFSense does not like the non-intel hardware and the particular 2.5Gbe NIC that comes with the unit. [See my previous post for more details on that.](https://blog.chriszavala.com/So-Long-PFSense/)


> YIKES, what a mess 👎

# Issues

### 1. **Configuration Migration**

This pain point should have been my first warning sign not to proceed with the migration. Attempting to transfer the configuration file to the new system seemed like it should have worked, given that they started from the same project. Unfortunately, the projects have differed so much since their original release that the configuration files no longer match as closely as they might have at one point.  

When trying to import the configuration file, the system would get hung up on the VLANs and the WAN and LAN port assignments. The issue mostly showed up on reboots. When I got the configuration imported, the VLANS would get assigned on the WAN interface, and the WAN interface would get re-assigned to the wrong physical NIC. Not only did that occur, but it also seemed to fail at importing the users' accounts, thus rendering the unit inaccessible from any interface other than the console.

  

### 2. **VLANs**

  

I ran into a few oddities while trying to use the configuration file to set up the VLANs via the Web UI. The main oddity is that the system would show the wrong parent interface when adding the interfaces, which contradicts what I had set up via the onboard console out of the HDMI port. This was more than an annoyance as there was no way to cleanly "swap the interface. It would appear that the UI being foreign to me was adding an extra pain point. At no point during the late-night setup did I think I would figure that out? If it is in the web interface, it will become more apparent as I familiarize myself with the interface. 

Rebooting the system after fighting with the VLAN interfaces in the web UI kept resulting in multiple configuration failures and interfaces reassigned to the wrong parent interface.  The WAN interface kept getting all the internal VLANs assigned to it. It appeared to be doing so with no apparent cause other than using the configuration file to attempt to set the device up. 

Later, the fix for this issue was redoing the whole build by hand instead of using the configuration file. This was an easier process to set up the system than the hours spent trying to deal with the configuration file. At one point, I even attempted to modify the XML file from PFSense before importing it into OPNSense. This ended up being yet another failed attempt. 

  

### 3. **Firewall Rules**

 Some of the default rules created by the OS itself are odd. I ran into a few issues where the main default rules created during the initial configuration were blocking such simple things as DNS, even though a rule was made after the fact to allow for DNS to work on that network. This would be the ideal case for most people needing to create a secured network for home labs or testing. However, the biggest issue is that when the user makes a rule that would overrule the default rule, it would not work. This was a pain point as I had to go back and forth between the rules to figure out what was blocking the traffic. It was thankfully easy to find once you open the logging for the interface you are trying to troubleshoot, but it takes some weird times to actually get this to work. At one point, for the rule to work correctly, I had to remove the network entirely and recreate it to make the rulesets I wanted to have in place for them to work. This was very frustrating as this could have been an artifact 

### 4. **VPN**

  

### 5. **DNS**
