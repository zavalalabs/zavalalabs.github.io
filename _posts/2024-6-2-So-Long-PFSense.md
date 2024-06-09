---
layout: post
title: So Long PFSense 👋
categories: [Networking, Server, OPNSense, PFSense]
---
# Background
The time has come the walrus said... to say goodbye to PFSense.

A decision I did not make lightly, but one that had to be made. After about 10 years of running PFSense as the head of my main network, I finally had to jump ship from Nettate's PFSense OS line. Recently my latest PFSense box started making rough sounds and started giving me that oh-so-familiar "I'm about to die" feeling. So I started looking at what my options were. 

For years I had been wanting a 1U appliance/server instead of a Dell SFF system that had been saved from the scrap pile years ago. It worked well for its time and gave me some headaches when I installed a 4x1Gbe NIC in it from the HP server parts bin I had. (I had to disconnect the DVD drive from both power and data to keep the unit from power failing at boot.)  So I decided to buy yet another mini-computer that I have been deploying as part of my Proxmox clusters in my home lab. The hardware I've been using has worked out stunningly well for the cluster and I wanted to see if it would work as the firewall. 

Off to Amazon, I go to buy the same unit I've been using, thinking that it would work just fine with PFSense and my migration would be as painless as possible. To my slight surprise, PFSense was not all that happy with the hardware. Moving from Intel to AMD was a bit of a shock to the OS's system. Mainly due to the 2.5Gb NIC that comes as part of the unit. That interface was not recognized by PFSense and I was not able to get it to work.

With not many options on the market for what I was looking for, I decided to try out OPNSense. With the hopes that the latest kernel version and driver support would see the 2.5Gbe nic.

# OPNSense

To my total surprise after loading the OPNSense installer, the 2.5Gbe NIC was found and my days were off to a better start. Both the 1Gbe and 2.5Gbe NICs were found natively without having to do any weird porting or installing from random repositories. Which we all can agree is a good thing. 

## Migration time!

The only thing that was left to do was to migrate my current configurations from PFSense over to OPNSense, which in the early days of the fork was supposed to be "easier" than what it appears to be now. However, I have no confirmation that it was easier or harder. I only know from trying how difficult the porting over of the PFSense config was over to OPNSense.

In some failed attempts I tried to restore the PFSense config file to OPNSense, but that was a no-go. Interface assignments would get lost on reboot and VLANs would get assigned to the incorrect interfaces. So, I ended up using a project on github to convert the configuration into a markdown format for my documentation system. Then leveraging that documentation to manually configure OPNSense.

After a few hours of stumbling around with the new interface of OPNSense, I was able to get the firewall up and running and able to get my VLans configured with the correct parent interfaces. 


# Closing thoughts

Moving to OPNSense was not something I wanted to do, but it was something that had to be done. I am happy with the move and move past using LAGG interfaces to try and get "2Gbe" speeds. The 2.5Gbe NIC is a welcome addition to the network and I am happy to have it... for now. In the future, I may look at moving to a 10Gbe NIC and see if that will work with OPNSense in a different unit.