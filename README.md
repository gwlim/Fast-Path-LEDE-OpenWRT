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

Use --nodeps in opkg

The builds uses the LEDE upstream repository unfortunately kernel config is hashed so any changes will make it uncompatible
