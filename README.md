# Introduction

**NOTE:** Much of this documentation is mirrored directly from the [original source](http://www.udpcast.linux.lu/).

UDPcast is a file transfer tool that can send data simultaneously to many destinations on a LAN. This can for instance be used to install entire classrooms of PC's at once. The advantage of UDPcast over using other methods (nfs, ftp, whatever) is that UDPcast uses UDP's multicast abilities: it won't take longer to install 15 machines than it would to install just 2.

UDPcast is released under the GPL 2.0 license or any later version. Parts of the code (fec.c) falls under a BSD-like license. The new boot loader contains cardmgr, which falls under the mozilla public license. All other included third-party software (busybox, dialog, lzop, udhcp, ...) falls under GPL (to the best of my knowledge. If you notice software falling under a different license, especially one with a BSD-like publicity clause, please notify me).

UDPcast can be started from the included busybox boot image for OS installations, or from the command line when using it for other purposes. Udpcast may be booted from CD, floppy media, or via the network, by uding PXE or Etherboot. A configuration file (udpcfg.txt) may be included on these boot media in order to bypass the setup menu.

# Building
## Compiling udpcast itself (server version)

1. Clone the repo:
`git clone https://github.com/TomKranenburg/udp-cast`
2. Cd into the source directory:
`cd udp-cast`
3. Compile:
`make`
4. As root, install:
`make install`

This gives you a standalone `udp-sender` and `udp-receiver`, suitable for use on a filesserver.
