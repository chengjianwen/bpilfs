# Introduction to Ipset
IP sets are a framework inside the Linux kernel, which can be administered by the ipset utility. Depending on the type, an IP set may store IP addresses, networks, (TCP/UDP) port numbers, MAC addresses, interface names or combinations of them in a way, which ensures lightning speed when matching an entry against a set.
# Package Information
* Download(HTTP): http://ipset.netfilter.org/ipset-6.34.tar.bz2
* Download MD5 sum: 51bd03f976a1501fd45e1d71a1e2e6bf
* Download Size: 148 KB
# Installation of Ipset
Install shadowsocks-libev by running the following commands:

    cd ipset-3.34
    ./configure --prefix=/usr --with-kbuild=../linux-rpi-4.9.y &&
    make
Now, as the root user:

    make install
# Contents
## Installed Programs:
ipset
