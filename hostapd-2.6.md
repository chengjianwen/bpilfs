# Introduction to hostapd
hostapd is a user space daemon for access point and authentication servers.

# Package Information
*	Download (HTTP): http://w1.fi/releases/hostapd-2.6.tar.gz 
*	Download MD5 sum: 78818f40e6d33a1d1de68a1551f6595a 
*	Download size: 1.8 MB
# Hostapd Dependencies
## Required
libnl-1.1.4
# Installation of hostapd
Install hostapd by running the following commands:

    cd hostapd
    cp defconfig .config
    sed -i 's/^#CONFIG_DRIVER_NL80211=y/CONFIG_DRIVER_NL80211=y/g' .config
    sed -i 's/^#CONFIG_IEEE80211N=y/CONFIG_IEEE80211N=y/g' .config
    sed -i 's/^#CONFIG_IEEE80211AC=y/CONFIG_IEEE80211AC=y/g' .config

    sed -i 's/^#CONFIG_ACS=y/CONFIG_ACS=y/g' .config
    sed -i 's/^#CONFIG_LIBNL32=y/CONFIG_LIBNL32=y/g' .config
    sed -i 's/^#CONFIG_TLS=openssl/CONFIG_TLS=internal/g' .config
    sed -i 's/^#CFLAGS += -I$<path to libnl include files>/CFLAGS += -I\/usr\/include\/libnl3/g' .config
    sed -i 's/^#LIBS += -L$<path to libnl library files>/LIBS += -lnl-genl-3 -lnl-3/g’ .config
    sed -i 's/^CONFIG_IPV6=y/#CONFIG_IPV6=y/g' .config
    sed -i 's/^#CONFIG_NO_ACCOUNTING=y/CONFIG_NO_ACCOUNTING=y/g' .config
    sed -i 's/^#CONFIG_NO_RADIUS=y/CONFIG_NO_RADIUS=y/g' .config
    sed -i 's/^#CONFIG_NO_ACCOUNTING=y/CONFIG_NO_ACCOUNTING=y/g'
    sed -i 's/^#CONFIG_NO_VLAN=y/CONFIG_NO_VLAN=y/g' .config
    sed -i 's/^#CONFIG_INTERNAL_LIBTOMMATH=y/CONFIG_INTERNAL_LIBTOMMATH=y/g’ .config
    sed -i 's/^#CONFIG_INTERNAL_LIBTOMMATH_FAST=y/CONFIG_INTERNAL_LIBTOMMATH_FAST=y/g’ .config

    make
Now, as the root user:
    BINDIR=/usr/sbin make install
# Contents
## Installed Programs:
hostapd, hostapd_cli
