---
title: Thunderbolt: You May Be Doing it Wrong
date: 2026-04-10 08:00:00 -0600
categories:
  - IT
tags:
  - sysadmin
  - thunderbolt
  - usb-c
  - hardware
  - peripherals
  - in-progress
description: "Not all usb-c cables are thunderbolth and not all thunderbolt is the same, do you know the difference?"
---

# Thunderbolt! Its Lightning Fast, Right? (Not Always)

## USB-C is Not Thunderbolt

Too often this causes confusion amung the consumer market, and if you open youtube and type in "USB-C"  there will be plenty of people talking for at minimum 5 minutes about the differnences. So lets save a little time and get to the point. USB-C is a type of connector, while Thunderbolt is a technology that can use the USB-C connector. Not all USB-C cables support Thunderbolt, and not all Thunderbolt devices use USB-C connectors. So, just because you have a USB-C cable doesn't mean it supports Thunderbolt speeds or features.

## Thunderbolt Technology is a certification/standard, not a specific product

Thunderbolt as a technology introduced by Intel in collaboration with apple, is a high-speed data transfer protocol that can support multiple types of data, including video, audio, and power delivery. It is designed to provide fast data transfer speeds and versatile connectivity options. However, not all devices that use Thunderbolt technology are the same. There are different versions of Thunderbolt (Thunderbolt 1, 2, 3, and 4), each with its own specifications and capabilities. So, when you see a device labeled as "Thunderbolt," it's important to check which version it supports to understand its capabilities.

Thunderbolt was not always using the USB-C connector. Thunderbolt 1 and 2 used the Mini DisplayPort connector, while Thunderbolt 3 and beyond (at the time of writing) use the USB-C connector. This means that if you have a Thunderbolt 1 or 2 device, it will not be compatible with USB-C cables or ports without an adapter. Conversely, Thunderbolt 3 and 4 devices can use USB-C connectors, but they may not support all the features of Thunderbolt if connected to a non-Thunderbolt USB-C port.

USB-C stands for "Universal Serial Bus Type-C" and is a reversible connector that can support various protocols, including USB 3.1, USB 3.2, and Thunderbolt 3 and 4. However, the presence of a USB-C connector does not guarantee that the device supports Thunderbolt technology. Always check the specifications of the device to confirm whether it supports Thunderbolt and which version it uses. With the addption of the USB-C connector, from phones to laptops, to peripherals, it has become a common standard for connectivity, and usually this means, no your mouse is not a thunderbolt device. That USB-C port on your laptop? Well that can be anything at this point. 

### How do you know if your device supports Thunderbolt?

Per industry standards, reputable manufacturers will label their products clearly if they support Thunderbolt technology. Look for the Thunderbolt logo (a lightning bolt) on the device or in the product specifications. The logo it's self is hard to miss in some instances, if you look at the side of your ultralite laptop, it hardly has room for any labels, so look closly around the USB-C Port, if you dont see the lightning bolt, its not a Thunderbolt port. 

Take a look at this diagram from intel, "One Thunderbolt(TM) port; Everything  USB-C can do, and more!"

![alt text](TBPort.png)

The SS symbol stands for SuperSpeed, which is a USB 3.1 feature, and that SS sybol come with 5, 10, 20,DP. All of these mean something different. 5 = 5 Gbps, 10 = 10 Gbps, 20 = 20 Gbps, DP = DisplayPort. So if you see a USB-C port with the SS symbol and a number, it means it supports that specific USB speed, NOT Thunderbolt. 

SS encased in a battery still stands for SuperSpeed, but it also indicates that the port supports power delivery, which is a feature of USB-C. This type of port usually can provide to power higher power demands, so, this one is the one to use for your portable monitor or charging your perihperals while transferig data. Again this is NOT Thunderbolt.

20 and 40 with the usb icon indicates that the port supports USB 3.2 Gen 2x2, which can provide data transfer speeds of up to 20 Gbps. This is a high-speed USB connection, but it is not Thunderbolt. (also offered in a battery icon variant as well)

If you see those individual labels on a port thats the de-mistification of the port. 

Thunderbolt encopases all of those featrues, over one single cable