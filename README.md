# LFS
Linux From Scratch Project 


Linux From Scratch (LFS) is a type of a Linux installation and the name of a book written by Gerard Beekmans.

Linux From Scratch is a way to install a working Linux system by building all components of it manually. This is, naturally, a longer process than installing a pre-compiled Linux distribution. According to the Linux From Scratch site, the advantages to this method are a compact, flexible and secure system and a greater understanding of the internal workings of the Linux-based operating systems.

A clean partition and a working Linux system with a compiler and some essential software libraries are required to build LFS. Instead of installing from an existing Linux system, one can also use a Live CD to build an LFS system.

The project formerly maintained the Linux From Scratch Live CD.[8] LFS Live CD contains all the source packages (in the full version of the Live CD only), the LFS book, automated building tools and (except for the minimal Live CD version) an Xfce GUI environment to work in. The official LFS Live CD is no longer maintained, and cannot be used to build the LFS version7 or later.[8] There are, however, two unofficial builds that can be used to build a 32-bit or 64-bit kernel and userspace respectively for LFS 7.x.[9]

First, a toolchain must be compiled consisting of the tools used to compile LFS, like GCC, glibc, binutils and other necessary utilities. Then, the root directory must be changed, (using chroot), to the toolchain's partition to start building the final system. One of the first packages to compile is glibc; after that, the toolchain's linker must be adjusted to link against the newly built glibc, so that all other packages that will make up the finished system can be linked against it as well. During the chroot phase, bash's hashing feature is turned off and the temporary toolchain's bin directory moved to the end of PATH. This way the newly compiled programs come first in PATH and the new system builds on its own new components.
