# Introduction to RP-PPPoE
PPPoE (Point-to-Point Protocol over Ethernet) is a protocol used by many ADSL Internet Service
Providers.

Roaring Penguin PPPoE is a PPPoE client for Linux.
# Package Information
* Download (HTTP): https://www.roaringpenguin.com/files/download/rp-pppoe-3.12.tar.gz
* Download MD5 sum: 216eb52b69062b92a64ee37fd71f4b66
* Download size: 234 KB
# RP-PPPoE Dependencies
## Required
pppd-2.4.7
# Installation of RP-PPPoE
Install rp-pppoe by running the following commands:

    cd src
    ./configure --prefix=/usr &&
    make
Now, as the root user:

    make install
# Configuring RP-PPPoE
## Setup Script
    pppoe-setup
# Contents
## Installed Programs:
pppoe, pppoe-server, pppoe-relay, pppoe-sniff
## Installed Scripts:
pppoe-connect, pppoe-start, pppoe-status, pppoe-stop,
pppoe-setup
## Installed Library:
libobex-capability.so
libobex-folder-listing.so
