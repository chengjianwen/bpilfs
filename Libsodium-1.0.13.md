# Introduction to Libsodium
Sodium is a new, easy-to-use software library for encryption, decryption, signatures, password hashing and more.
# Package Information
*	Download (HTTP): https://download.libsodium.org/libsodium/releases/libsodium-1.0.13.tar.gz
*	Download MD5 sum: f38aac160a4bd05f06f743863e54e499
* Download Size: 1.81 MB
# Installation of Libsodium
Install libsodium by running the following commands:

    cd libsodium
    ./autogen.sh &&
    ./configure --prefix=/usr &&
    make
Now, as the root user:

    make install
# Contents
## Installed Library:
libsodium.la libsodium.a libsodium.so.18.3.0
