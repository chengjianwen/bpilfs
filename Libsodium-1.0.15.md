# Introduction to Libsodium
Sodium is a new, easy-to-use software library for encryption, decryption, signatures, password hashing and more.
# Package Information
*	Download (HTTP): https://download.libsodium.org/libsodium/releases/libsodium-1.0.15.tar.gz
*	Download MD5 sum: 070373e73a0b10bd96f412e1732ebc42
* Download Size: 1.78 MB
# Installation of Libsodium
Install libsodium by running the following commands:

    cd libsodium-1.0.15
    ./autogen.sh &&
    ./configure --prefix=/usr &&
    make
Now, as the root user:

    make install
# Contents
## Installed Library:
libsodium.la libsodium.a libsodium.so.23.0.0
