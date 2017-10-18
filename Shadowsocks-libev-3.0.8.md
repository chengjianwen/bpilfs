# Introduction to Shadowsocks-libev
Shadowsocks-libev is a lightweight secured SOCKS5 proxy for embedded and low-end boxes.
# Package Information
*	Download (HTTP): https://github.com/shadowsocks/shadowsocks-libev/releases/download/v3.0.8/shadowsocks-libev-3.0.8.tar.gz
*	Download MD5 sum: 872386adbda0252c9be895768ca26d79
*	Download Size: 1.81MB
# Shadowsocks-libev Dependencies
## Required
libsodium
libmbedtls
libev
udns
iptables
ipset
# Installation of Shadowsocks-libev
Install shadowsocks-libev by running the following commands:

    cd shadowsocks-libev-3.0.8
    ./configure --prefix=/usr --disable-documentation &&
    make
Now, as the root user:

    make install
# Configuration
打开文件/etc/shadowsocks/config.json，文件内容修改为：

    {
        “server”=“23.106.130.2”,
        “server_port”=63880,
        “local_address”:”0.0.0.0”,
        “local_port”:1080,
        “password”:”summer99”,
        “timeout”:300,
        “mode”:”tcp_and_udp”,
        “method”:”aes-256-cfb”,
        “fast_open”:false,
        “workers”:1
    }
# 设置翻墙功能

    iptables -t nat -N SHADOWSOCKS

    iptables -t nat -A SHADOWSOCKS -d 23.106.130.2 -j RETURN

    iptables -t nat -A SHADOWSOCKS -d 0.0.0.0/8 -j RETURN
    iptables -t nat -A SHADOWSOCKS -d 10.0.0.0/8 -j RETURN
    iptables -t nat -A SHADOWSOCKS -d 127.0.0.0/8 -j RETURN
    iptables -t nat -A SHADOWSOCKS -d 169.254.0.0/16 -j RETURN
    iptables -t nat -A SHADOWSOCKS -d 172.16.0.0/12 -j RETURN
    iptables -t nat -A SHADOWSOCKS -d 192.168.0.0/16 -j RETURN
    iptables -t nat -A SHADOWSOCKS -d 224.0.0.0/4 -j RETURN
    iptables -t nat -A SHADOWSOCKS -d 240.0.0.0/4 -j RETURN

    iptables -t nat -A SHADOWSOCKS ! -p icmp -j REDIRECT --to-ports 1080

    iptables -t nat -A PREROUTING ! -p icmp -j SHADOWSOCKS
    iptables -t nat -A OUTPUT ! -p icmp -j SHADOWSOCKS

    ss-redir -c /etc/shadowsocks/config.json —f /var/run/shadowsocks-redir.pid
    ss-tunnel -c /etc/shadowsocks/config.json -b 0.0.0.0 -l 53 -L “8.8.8.8:53” -f /var/run/shadowsocks-tunnel.pid
# Contents
## Installed Programs:
ss-local ss-tunnel ss-server ss-manager ss-redir ss-nat
## Installed Include Files:
shadowsocks.h
## Installed Library:
libshadowsocks-libev.la
libshadowsocks-libev.a
