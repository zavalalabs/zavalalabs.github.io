---
title: Goodbye Hyper-V (Free) It was nice knowing you! 🖥️
date: 2024-05-07 01:00:00 +/-TTTT
categories: [Home Lab, Servers]
tags: [virtualization, server, hyper-v]     # TAG names should always b lowercase

---




# So long old friend

This will be a short and sweet post, as Hyper-V Free, aka *Hype-V Server,* was sunset in 2019, with support ending earlier this year, **Jan. 9th, 2024**.  While the free standalone server was a great stripped down operating system, it was a pain to get up and running and manage. So in some ways it's a good thing that the free version is sunset. Managing Hyper V without the GUI was hard to get going. 

For most home lab folks, you can't beat free, and you can't beat something that should be “easy” to get started with. When it came to installing the server, it was easy as pie! Just hope you didn't have much to manage after that. Loading Hyper-V Manager in Windows 10 or Windows 8 was where the pain really started. You had to remote connect to the server and hope that no certificates were in the way. Shockingly, you always would run into some type of authentication or PowerShell error. 

Once connected, you could *try* to get something going, but it would take a little to do. (At least for me) 

I had gotten a few VMs to run on it and even got a shocking uptime of 7 days! (I know, I know, I should have gotten a screenshot.) However, spinning up actual workloads always seemed like a long shot. 

### Pain Points

- No GUI
- Clustering required a domain of some sort
- Certificates were always "untrusted." 
- GPU passthrough supported? (It may have been, but I never got it working.)

### What worked

- It was free
- It was a great way to get get used to “server core” and PowerShell. 
- Did I mention it was free?

# What's Next?

The journey to a new hypervisor will be documented in a few posts. Take a look at the #Virtualization tag for more!

Until next time!