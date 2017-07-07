# Fast Path for LEDE/OpenWRT

Source
------

https://github.com/gwlim/mips24k-ar71xx-lede-patch

https://github.com/gwlim/mips74k-ar71xx-lede-patch

https://github.com/gwlim/mpc85xx-lede-patch

The repository contain firmware images compiled from the above sources.
Fast Path mainly improve Network Address Translation in IPv4 Routing
The Fast Path implementation is based on QCA Shortcut-Fe implementation
It also contains compiler optimization for the mips24kc,mips74kc and mpc8548 architecture.

FAQ
---
Problem: PPPoE cannot access certain websites
Go to Network > Firewall > General Settings > Turn on MSS clamping


