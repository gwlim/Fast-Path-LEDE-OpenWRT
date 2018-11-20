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

Changes
-------
Latest Linux Kernel 4.4.163

Updated GCC toolchain to 6.5

Backported Wireless/TCP Performance patches, upstream commits that improves system performance are tested and backported not full kernel versions to reduce bloat

Use of LTO on most packages and kernel modules

Optimized compiler flags, js and minified CSS

Add more frequently requested VPN packages

Package list in Above 64MB
--------------------------

luci luci-app-ddns luci-app-sqm luci-app-upnp luci-proto-relay luci-proto-3g

kmod-usb-acm kmod-usb-serial-ipw kmod-usb-serial-option kmod-usb-serial-qualcomm 
kmod-usb-serial-sierrawireless kmod-usb-serial-wwan kmod-usb-net-cdc-eem 
kmod-usb-net-cdc-ether kmod-usb-net-cdc-mbim kmod-usb-net-cdc-ncm kmod-usb-net-cdc-subset 
kmod-usb-net-hso kmod-usb-net-huawei-cdc-ncm kmod-usb-net-kalmia kmod-usb-net-qmi-wwan 
kmod-usb-net-sierrawireless 

kmod-sched-cake luci-app-openvpn openvpn-openssl luci-proto-wireguard luci-app-nlbwmon 
luci-app-wireguard luci-app-shadowsocks-libev shadowsocks-libev shadowsocks-client wireguard ipset 
kmod-sit kmod-ip6-tunnel kmod-nat46 kmod-ppp kmod-mppe kmod-pptp kmod-gre kmod-pppol2tp kmod-l2tp 

FAQ
---

Cannot install packages with Kernel Dependencies?

Due the use of stronger stackprotector protection, newer Linux Kernel Version and updated GCC compiler, incompatbilities with upstream Kernel Modules is expected and cannot be resolved.
If you have any Kernel Module request drop a message in issues.

What is the difference between 64MB and Above vs Below 64MB?

Due to the increase in kernel size as well as compiler protections and O2 optimization flags and additional packages, memory usage for OpenWrt has increased.
Routers that has 64MB RAM by default can use both version which routers that has only 32MB RAM should use below 64MB.


Request Firmware Support
------------------------

You can request support for your custom device by opening an issue however I will be only adding support to supported architectures like:
AR71xx where I can more or less gurantee the workability of the firmware as I have a lot of devices based on this architecture.

JPerf NAT Benchmark on a TP-WR1043NDv1 Atheros AR9132@430MHZ
------------------------------------------------------------
![alt text](https://raw.githubusercontent.com/gwlim/Fast-Path-LEDE-OpenWRT/master/bench.PNG)

