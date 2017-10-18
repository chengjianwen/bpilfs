# Introduction to PPPD
PPP (Point-to-Point Protocol) is a protocol to provide Internet connections over serial lines.
# Package Information
*	Download (HTTP): https://www.samba.org/ftp/ppp/ppp-2.4.7.tar.gz
*	Download MD5 sum: 78818f40e6d33a1d1de68a1551f6595a 
*	Download size: 672 KB
# Installation of PPPD
Install pppd by running the following commands:

    ./configure --prefix=/usr &&
    make
Now, as the root user:

    make install
# Contents
## Installed Programs:
pppd, pppdump
## Installed Library:
minconn.so
openl2tp.so
passprompt.so
passwordfd.so
pppol2tp.so
radattr.so
radius.so
radrealms.so
winbind.so
