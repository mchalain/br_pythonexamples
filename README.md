# BuildRoot External: Python module examples

This repository contains examples of python modules to use with BuildRoot.
It's a part of an article on https://linuxembedded.fr .

## Installation

You need to download a version of BuildRoot somewhere on your Build Machine.
In this file, the path is */opt/buildroot* and the version is **2021.05.x**.

```bash
$ sudo git clone git://git.buildroot.net/buildroot /opt/buildroot -b 2021.0.5.x
```

This repository is an external module of BuildRoot (a layer for Yocto users).

```bash
$ git clone https://github.com/mchalain/br_pythonexamples
$ cd br_pythonexamples
$ make O=$PWD/output BR2_EXTERNAL=$PWD -c /opt/buildroot raspberrypi4_64_defconfig
$ cd output
$ make menuconfig
 > Toolchain > C Library > glibc
 > Toolchain > Enable Fortran support
 > Toolchain > Enable OpenMP support
 > External options > mymath...
$ make
```
