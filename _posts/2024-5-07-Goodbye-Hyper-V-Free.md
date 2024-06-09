---
layout: post
title: Goodbye Hyper-V (Free) It was nice knowing you! 🖥️
categories: [Virtualization, Server, Hyper-V]
---




# So long old friend

This will be a short and sweet post, as Hyper-V free aka *Hype-V Server* was sun set in 2019 with support ending earlier this year, **Jan. 9th 2024**.  While the free standalone server was a great stripped down operationg system, it was a pain to get up and running and manage. So in some ways its a good thing that the free version is sunset. Managing hyper-v with out the GUI was a hard one to get going. 

For most home lab folks you cant beat free and you cant beat something that should be "easy" to get started with. When it came to installing the server, it was easy as pie! Just hope you didnt have much to manage after that. Loading Hyper-V manager in windows 10 or Windows 8  was where the pain really started. You had to remote connect to the server and hope that no certificates were in the way. Shockingly you always would run into some type of authentication or pwoershell error. 

Once connected you could *try* to get something going but it would take a little to do. (At least for me) 

I had gotten a few VMS to run on it and even got a shocking uptime of 7 days! (I know, I know, I should have gotten a screen shot) However, spinning up actual workloads always eemed like a long shot. 

### Pain Points

- No GUI
- Clustering required a domain of some sort
- Certificates were always "Un trusted"
- GPU passthrough supported? (It may have been, but I never got it working)

### What worked

- It was free
- It was a great way to get get used to "server core" and powershell
- Did I mention it was free?

# What's Next?

The journy to a new hypervisor will be documented in a few posts. Check out the #Virtualization tag for more!

Till next time!