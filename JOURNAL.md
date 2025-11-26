---
title: Linux Pico
author: Kai Pereira
description: Making a Pi Pico that can run Linux
created_at: 2025-11-24
---
## Sorting out the kinks

I really want to make my first SBC that I can learn a lot of skills from, while not making it completely overcomplicated, or just the complexity doesn't justify the price. Something not like absurdly powerful, but also useful and cool!

I have this idea for a sort of development board, in the Pi Pico form factor, that could run Linux and also have lots of storage aswell as ethernet. This could make a cool low-power hobby home-server that could be used for things like streaming, storage offload, appliances, by exposing an NVMe SSD.

An NVMe SSD, is conveniently 22mm wide, which is approximately how large the Pi Pico is, so I think it would be really cool if it was a drop-in replacement for the Pi Pico, just more expensive but way more useful.

I've seen this board, the Pico Plus which is a kind meant more for computing, but I really don't see much use case for this thing, compared to a more NAS style SBC, that could actually be used for practical home applications and much more niche:

![[Pasted image 20251124152719.png]]

So the idea is simple: Pi Pico form factor, PCIe NVMe SSD and GbE, with a focus on home-style computation instead of hardcore NPU computation.

Now based off of these criteria, I need to find some small MPU's that will be good! A couple of them that I've found are the: 
- STM32MP257, a small, fine pitch MPU with PCIe and ethernet, a bit expensive though
- Rockchip RK3566, a classic, but has too many features I won't use
- RK3562, this is basically the RK3566, but smaller and with less features, which is actually a really good option!
- SAMA5D2, high performance, low power, I thought this initially had PCIe, but it actually has PCI 5, which is just a security standard and not actually the interfact, so it's not a good choice!
- 

