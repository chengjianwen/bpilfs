# Introduction to Libmbedtls
mbed TLS (formerly known as PolarSSL) makes it trivially easy for developers to include cryptographic and SSL/TLS capabilities in their (embedded) products, facilitating this functionality with a minimal coding footprint.
# Package Information
*	Download (HTTP): https://tls.mbed.org/download/mbedtls-2.5.1-gpl.tgz
*	Download MD5 sum: 313f637f65b5f6d74d45310482a9c84f
* Download Size: 1.9 MB
# Installation of Libmbedtls
Install libmbedtls by running the following commands:

    cd mbedtls-2.5.1
As the root user:

    CFLAGS=-fPIC make DESTDIR=/usr install
# Contents
## Installed Library:
libmbedcrypt.a libmbedtls.a libmbedx509.a
