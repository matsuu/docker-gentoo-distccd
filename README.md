# dockerfile-gentoo-distccd

Dockerfile for distccd server on gentoo

## Setup

    docker run -d -P --name distccd matsuu/gentoo-distccd
    docker port distccd 3632
    0.0.0.0:49153

## Howto

    export DISTCC_HOSTS="server:49153,lzo,cpp"
    pump make CC=distcc -j4

## References

- [distcc: a fast, free distributed C/C++ compiler](https://code.google.com/p/distcc/)
- [Gentoo Linux](https://www.gentoo.org/)
- [Distcc - Gentoo Wiki](http://wiki.gentoo.org/wiki/Distcc)
