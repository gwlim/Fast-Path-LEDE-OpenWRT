# Fast Path for LEDE/OpenWRT

Source
------

https://github.com/gwlim/mips24k-ar71xx-lede-patch

https://github.com/gwlim/mips74k-ar71xx-lede-patch

https://github.com/gwlim/mpc85xx-lede-patch

The repository contain firmware images compiled from the above sources

Fast Path mainly improve Network Address Translation in IPv4 Routing

The Fast Path implementation is based on QCA Shortcut-Fe implementation

It also contains compiler optimization for the mips24kc,mips74kc and mpc8548 architecture

FAQ
---

Cannot install packages with Kernel Dependencies?

From Aug 2018 Release Onwards Kernel should be compatible with LEDE Kernel Module Packages.

Request Firmware Support
------------------------

You can request support for your custom device by opening an issue however I will be only adding support to supported architectures like:
AR71xx where I can more or less gurantee the workability of the firmware as I have a lot of devices based on this architecture.

