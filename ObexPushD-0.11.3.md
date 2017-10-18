# Introduction to ObexPushD
  obexpushd is a program that can be used to receive
files using OBEX (OBject EXchange) protocol over
Bluetooth, IrDA or network connection.

It can be used to receive files from mobile phones
and other devices.

# Package Information
  * Download (HTTP): https://downloads.sourceforge.net/project/obexpushd/0.11.3/obexpushd-0.11.3-source.tar.gz
  * Download MD5 sum: 8a7ea2db1d54b999dea6c6033e2c69ee
  * Download size: 76 KB

# ObexPushD Dependencies
## Required
[CMake-3.9.4](http://www.linuxfromscratch.org/blfs/view/cvs/general/cmake.html)
[BlueZ-5.47](http://www.linuxfromscratch.org/blfs/view/svn/general/bluez.html)
[OpenOBEX-1.7.2](http://www.linuxfromscratch.org/blfs/view/cvs/general/openobex.html)

## Optional
[xsltproc-1.1.31](http://www.linuxfromscratch.org/blfs/view/svn/general/libxslt.html)(to build documentation).

[libgcrypt-1.8.1](http://www.linuxfromscratch.org/blfs/view/svn/general/libgcrypt.html)(for MD5 and NONCE instead of internal
code).

# Installation of ObexPushD
Install obexpushd by running the following commands:

    mkdir build &&
    cd build &&
    cmake -DCMAKE_INSTALL_PREFIX=/usr \
           -DCMAKE_BUILD_TYPE=Release \
           .. &&
    make
Now, as the root user:

    make install

# Configuring ObexPushD
## Boot Script
To automatically start the opexpushd daemon when the system is rebooted, install the /etc/rc.d/init.d/
obexpushd bootscript from the bpilfsbootscripts-
20170615 package.

    make install-obexpushd

# Contents
## Installed Programs:
obexpushd, obexpush_atd, obex-folder-listing, file_storage.sh
## Installed Library:
libobex-capability.so libobex-folder-listing.so
